![Version: 1.0](https://img.shields.io/badge/Version-1.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# Data Provenance Tracking Implementation for GenAI in CTI

This document describes a comprehensive implementation approach for tracking data provenance throughout the GenAI-enhanced CTI lifecycle, adhering to CTI-AI-5 (Data Integrity Controls) requirements. The implementation ensures that all data sources used in GenAI prompts or fine-tuning are verified, tracked, and documented.

## 1. System Architecture

The provenance tracking architecture integrates with existing CTI workflows and platforms to provide end-to-end data lineage:

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Data Sources │     │ Ingestion    │     │  Provenance  │     │ GenAI        │
│ & Collection │────▶│ & Validation │────▶│  Registry    │────▶│ Integration  │
└──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
                                                │                      │
                                                │                      │
                                                ▼                      ▼
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│ Intelligence │     │ Verification │     │ Analysis     │     │ Output       │
│ Products     │◀────│ & Approval   │◀────│ Workspace    │◀────│ Generation   │
└──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
```

## 2. Data Source Classification Schema

All data sources are classified according to:

| Attribute | Description | Values |
|-----------|-------------|--------|
| **Source Type** | Category of information provider | Primary, Secondary, Community, Open Source, Proprietary, Vendor |
| **Verification Level** | Degree of verification performed | Unverified, Partially Verified, Fully Verified, Corroborated |
| **Timeliness** | Currency and relevance | Real-time, Recent (< 7 days), Current (< 30 days), Historical |
| **Reliability** | Historical accuracy rating | A (Always reliable), B (Usually reliable), C (Sometimes reliable), D (Not usually reliable), E (Unreliable), F (Cannot be judged) |
| **Confidence** | Assessed accuracy of specific information | 1 (Confirmed), 2 (Probably True), 3 (Possibly True), 4 (Doubtful), 5 (Improbable), 6 (Cannot be judged) |
| **Security Classification** | Access and handling requirements | Unclassified, Confidential, Restricted, Partner Sharable, Internal Only |
| **Update Frequency** | How often the source updates | Continuous, Daily, Weekly, Monthly, Quarterly, Static |

## 3. Implementation Components

### 3.1 Provenance Metadata Registry

The central repository for all data provenance information:

```json
{
  "source_id": "SRC-2025-0472",
  "source_name": "VirusTotal Intelligence",
  "source_type": "Vendor",
  "source_uri": "https://virustotal.com/intelligence/hash/7e91f4238348ce6d18eadcd10d1c28459f7983f1715c4b2165dedca5c356acf2",
  "collection_timestamp": "2025-03-15T13:42:17Z",
  "collection_method": "API",
  "collector": {
    "user_id": "analyst32",
    "role": "Malware Analyst"
  },
  "classification": {
    "verification_level": "Partially Verified",
    "timeliness": "Recent",
    "reliability": "B",
    "confidence": "2",
    "security_classification": "Internal Only",
    "update_frequency": "Continuous"
  },
  "validation": {
    "status": "Valid",
    "validation_timestamp": "2025-03-15T14:10:42Z",
    "validator": {
      "user_id": "analyst17",
      "role": "Senior Threat Analyst"
    },
    "validation_method": "Cross-reference with sandbox analysis",
    "validation_notes": "Hash matches sample analyzed in internal sandbox."
  },
  "related_sources": [
    "SRC-2025-0471",
    "SRC-2025-0473"
  ],
  "usage_restrictions": [
    "Not for external sharing",
    "Attribution requires management approval"
  ],
  "expiration": {
    "expiration_date": "2025-06-15T00:00:00Z",
    "revalidation_required": true
  }
}
```

### 3.2 Source Verification Workflows

Standard workflows for validating different types of data sources:

#### IOC Verification Workflow

1. **Initial Receipt**
   - Log source metadata
   - Assign initial classification
   - Check for duplicates

2. **Technical Validation**
   - Verify format and structure
   - Test for syntax errors
   - Validate against schemas

3. **Contextual Validation**
   - Cross-reference with known intelligence
   - Check for inconsistencies with existing data
   - Assess temporal relevance

4. **Corroboration**
   - Check against independent sources
   - Minimum 2 sources for critical indicators
   - Document corroboration results

5. **Classification**
   - Assign final reliability and confidence
   - Document verification steps
   - Set expiration/review date

#### Document/Report Verification Workflow

1. **Source Assessment**
   - Evaluate author/organization credibility
   - Check publishing history and reputation
   - Verify attribution chain

2. **Content Verification**
   - Cross-check technical claims
   - Validate referenced materials
   - Compare with independent reporting

3. **Bias Evaluation**
   - Assess for political, commercial, or attribution bias
   - Document potential conflicts of interest
   - Note analytical limitations

4. **Classification Assignment**
   - Assign reliability and confidence ratings
   - Document verification limitations
   - Set expiration/review date

### 3.3 GenAI Integration Controls

Mechanisms for enforcing provenance requirements in GenAI:

#### Prompt Provenance Injection

All GenAI prompts include provenance metadata:

```
[PROMPT]
Analyze the following malware behaviors for attribution. The data comes from sources with the following provenance:

Source 1: SRC-2025-0472
- Type: Vendor (VirusTotal)
- Reliability: B (Usually reliable)
- Confidence: 2 (Probably true)
- Verification: Partially verified through sandbox analysis

Source 2: SRC-2025-0473
- Type: Community (Malware Bazaar)
- Reliability: C (Sometimes reliable)
- Confidence: 3 (Possibly true)
- Verification: Unverified direct submission

Analysis should weight conclusions accordingly and highlight where source limitations affect confidence.

[TECHNICAL DETAILS]
{technical_details_from_sources}
```

#### Provenance Chain Maintenance

The system maintains unbroken provenance chains through:

1. **Source Linkage**: All GenAI outputs reference input sources
2. **Transformation Tracking**: Changes made to data during processing are logged
3. **Confidence Inheritance**: Outputs cannot have higher confidence than their inputs
4. **Verification Gateways**: Data must pass verification before entering analysis workflows
5. **Expiration Enforcement**: Expired or outdated data is flagged and requires revalidation

## 4. Verification Evidence Collection

For each data source, the system captures evidence of verification:

### 4.1 Technical Evidence

- Hash comparisons
- Sandbox analysis results
- Signature validations
- Format validations
- Schema compliance checks

### 4.2 Contextual Evidence

- Cross-reference records
- Timeline validations
- Geographic consistency
- Actor behavior consistency
- Capability alignment

### 4.3 Corroboration Evidence

- Independent source records
- Confidence comparison matrix
- Contradiction assessments
- Alternative hypothesis documentation
- Source independence verification

## 5. Integration with CTI Platforms

### 5.1 API Specifications

RESTful API for provenance tracking:

```yaml
openapi: 3.0.0
info:
  title: CTI Data Provenance API
  version: 1.0.0
paths:
  /sources:
    post:
      summary: Register a new data source
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Source'
      responses:
        '201':
          description: Source registered
  /sources/{source_id}/validate:
    post:
      summary: Record validation of a source
      parameters:
        - name: source_id
          in: path
          required: true
          schema:
            type: string
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Validation'
      responses:
        '200':
          description: Validation recorded
  /genai/prompts:
    post:
      summary: Register a GenAI prompt with source references
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Prompt'
      responses:
        '201':
          description: Prompt registered
components:
  schemas:
    Source:
      type: object
      properties:
        source_name:
          type: string
        source_type:
          type: string
          enum: [Primary, Secondary, Community, OpenSource, Proprietary, Vendor]
    Validation:
      type: object
      properties:
        status:
          type: string
          enum: [Valid, Invalid, Uncertain]
        validation_method:
          type: string
    Prompt:
      type: object
      properties:
        text:
          type: string
        source_references:
          type: array
          items:
            type: string
```

### 5.2 MISP Integration

For MISP-based CTI platforms:

```python
# Example Python script for MISP integration
import pymisp
from provenance_tracker import ProvenanceRegistry

# Initialize connections
misp = pymisp.PyMISP(MISP_URL, MISP_KEY, MISP_VERIFYCERT)
registry = ProvenanceRegistry(REGISTRY_URL, API_KEY)

def import_misp_event_with_provenance(event_id):
    """Import MISP event with provenance tracking"""
    # Fetch event
    event = misp.get_event(event_id)
    
    # Register source in provenance registry
    source_metadata = {
        "source_name": f"MISP Event {event_id}",
        "source_type": "Community",
        "source_uri": f"{MISP_URL}/events/view/{event_id}",
        "collection_timestamp": event['Event']['date'],
        "classification": {
            "verification_level": "Unverified",
            "timeliness": "Recent" if is_recent(event['Event']['date']) else "Historical",
            "reliability": get_org_reliability(event['Event']['Orgc']['name']),
            "confidence": event['Event'].get('attribute_count', 0) > 10 ? "3" : "4",
            "security_classification": get_tlp_classification(event['Event']),
            "update_frequency": "Static"
        }
    }
    
    source_id = registry.register_source(source_metadata)
    
    # Process attributes with provenance
    for attribute in event['Event']['Attribute']:
        attribute_provenance = {
            "parent_source": source_id,
            "attribute_id": attribute['uuid'],
            "attribute_type": attribute['type'],
            "attribute_value": attribute['value']
        }
        
        registry.register_attribute(attribute_provenance)
    
    return source_id
```

### 5.3 STIX Integration

For STIX-based CTI platforms:

```python
# Example Python script for STIX integration
from stix2 import TAXIICollectionSource, Filter
from taxii2client.v20 import Collection
from provenance_tracker import ProvenanceRegistry

# Initialize connections
collection = Collection(COLLECTION_URL, user=USER, password=PASSWORD)
tc_source = TAXIICollectionSource(collection)
registry = ProvenanceRegistry(REGISTRY_URL, API_KEY)

def import_stix_with_provenance(stix_filter):
    """Import STIX objects with provenance tracking"""
    # Filter and retrieve STIX objects
    filt = Filter("type", "=", stix_filter)
    stix_objects = tc_source.query(filt)
    
    # Register TAXII source
    source_metadata = {
        "source_name": collection.title,
        "source_type": "Community",
        "source_uri": COLLECTION_URL,
        "collection_timestamp": datetime.now().isoformat(),
        "classification": {
            "verification_level": "Unverified",
            "timeliness": "Current",
            "reliability": get_taxii_reliability(collection),
            "confidence": "3",
            "security_classification": get_taxii_classification(collection),
            "update_frequency": "Daily"
        }
    }
    
    source_id = registry.register_source(source_metadata)
    
    # Process STIX objects with provenance
    for obj in stix_objects:
        object_provenance = {
            "parent_source": source_id,
            "stix_id": obj['id'],
            "stix_type": obj['type'],
            "created": obj.get('created', ''),
            "modified": obj.get('modified', '')
        }
        
        registry.register_stix_object(object_provenance)
    
    return source_id
```

## 6. Implementation Checklist

- [ ] Define and document data source classification schema
- [ ] Implement provenance metadata registry
- [ ] Develop source verification workflows
- [ ] Create API for provenance tracking
- [ ] Implement GenAI prompt provenance controls
- [ ] Integrate with existing CTI platforms
- [ ] Develop provenance chain maintenance
- [ ] Implement verification evidence collection
- [ ] Create expiration and revalidation system
- [ ] Establish audit mechanisms
- [ ] Train staff on provenance requirements
- [ ] Document provenance procedures

## 7. Compliance with CTI-AI-5 Requirements

| CTI-AI-5 Requirement | Implementation Component |
|----------------------|--------------------------|
| Establish source verification protocols | Source verification workflows (Section 3.2) |
| Track data provenance through lifecycle | Provenance chain maintenance (Section 3.3.2) |
| Verify timeliness and accuracy | Data source classification schema (Section 2) |
| Implement controls to prevent tampering | Provenance metadata registry (Section 3.1) |
| Document origin and verification status | Verification evidence collection (Section 4) |
| Regularly audit prompt content | Provenance chain maintenance (Section 3.3.2) |

## 8. Example Data Flow

```
1. Malware sample received from VirusTotal API
   → Source registered (SRC-2025-0472)
   → Initial classification: Vendor, Partially Verified, Recent, Reliability B

2. Sample submitted to internal sandbox for validation
   → Validation results recorded
   → Classification updated: Verification level → Fully Verified

3. OSINT report with additional context discovered
   → Source registered (SRC-2025-0473)
   → Initial classification: Open Source, Unverified, Recent, Reliability C
   → Cross-referenced with SRC-2025-0472

4. Analyst creates GenAI prompt incorporating both sources
   → Prompt registered with provenance metadata
   → System enforces confidence inheritance (cannot exceed source confidence)

5. GenAI generates threat actor analysis based on prompt
   → Output includes source references and confidence indicators
   → Provenance chain maintained from original sources

6. Analyst reviews and verifies GenAI output
   → Verification results recorded
   → Final product includes full provenance trail
```

---

*This implementation example aligns with CTI-AI-5 (Data Integrity Controls) control requirements and should be customized to reflect your organization's specific infrastructure, tools, and existing CTI processes.* 