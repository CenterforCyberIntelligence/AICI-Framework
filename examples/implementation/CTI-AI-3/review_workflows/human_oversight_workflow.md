![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# Human Oversight Workflow for GenAI in CTI Operations

This document outlines a comprehensive workflow for implementing human oversight of Generative AI outputs in cyber threat intelligence operations, meeting the requirements of CTI-AI-3 (Human Oversight Requirement).

## 1. Overview

The human oversight workflow ensures that all GenAI-generated intelligence content undergoes appropriate review and validation before operational use, with clear accountability and audit trails.

### Workflow Objectives

1. Establish clear review procedures for all GenAI-generated content
2. Define roles and responsibilities for human oversight
3. Create transparent documentation of review decisions
4. Implement escalation paths for uncertain, high-risk, or questionable outputs
5. Enable audit and verification of human review activities

## 2. Implementation Architecture

The following diagram illustrates the end-to-end workflow for human oversight:

```
┌───────────────┐     ┌───────────────┐     ┌───────────────┐     ┌───────────────┐
│  GenAI Input  │     │  GenAI Output │     │ Human Review  │     │ Final Product │
│   (Prompt)    │────▶│  Generation   │────▶│  & Validation │────▶│    Release    │
└───────────────┘     └───────────────┘     └───────────────┘     └───────────────┘
                             │                      ▲                     │
                             │                      │                     │
                             ▼                      │                     ▼
                      ┌───────────────┐     ┌───────────────┐     ┌───────────────┐
                      │ Documentation │     │  Escalation   │     │   Audit &     │
                      │    System     │────▶│   Process     │     │  Compliance   │
                      └───────────────┘     └───────────────┘     └───────────────┘
```

## 3. Role Definitions and Responsibilities

| Role | Responsibilities | Authority |
|------|------------------|-----------|
| **Analyst** | - Crafts GenAI prompts<br>- Performs initial review of outputs<br>- Documents verification steps<br>- Makes modifications as needed | - Reject or accept initial outputs<br>- Request additional model runs<br>- Escalate questionable content |
| **Lead Analyst** | - Reviews complex or sensitive outputs<br>- Approves operational-level intelligence<br>- Provides guidance on verification methods<br>- Ensures documentation compliance | - Approve outputs for operational use<br>- Return for additional verification<br>- Request additional subject matter expertise |
| **Intelligence Manager** | - Reviews strategic intelligence products<br>- Ensures oversight compliance<br>- Approves high-impact assessments<br>- Addresses escalated concerns | - Final approval for high-sensitivity content<br>- Halt release of questionable intelligence<br>- Invoke additional review processes |
| **AI Governance Officer** | - Monitors oversight process compliance<br>- Reviews oversight metrics<br>- Recommends process improvements<br>- Conducts periodic oversight audits | - Conduct compliance reviews<br>- Recommend workflow modifications<br>- Initiate training or awareness activities |

## 4. Verification and Approval Process

### 4.1 General Workflow Steps

1. **Content Generation**
   - Analyst develops prompt for GenAI system
   - System generates initial output
   - Output and original prompt are logged in documentation system

2. **Initial Review**
   - Analyst performs first-level verification of factual accuracy
   - Analyst identifies potential biases, hallucinations, or quality issues
   - Initial review results are documented with specific concerns noted

3. **Verification Activities**
   - Content is verified against trusted external sources
   - Technical claims are validated with appropriate tools
   - Attribution statements are confirmed with multiple sources
   - Any speculative content is clearly identified

4. **Secondary Review**
   - Lead analyst reviews based on intelligence criticality
   - Additional subject matter experts consulted as needed
   - Structured review checklist completed

5. **Approval and Attribution**
   - Appropriate authority approves based on intelligence level
   - Contribution of GenAI is clearly documented in product
   - Human reviewers are identified in metadata
   - Approval is documented in oversight system

6. **Post-Release Monitoring**
   - Feedback channels established for recipients
   - Corrections process defined for identified issues
   - Lessons learned captured for process improvement

### 4.2 Intelligence Criticality Levels and Required Review

| Intelligence Level | Criticality Factors | Required Review |
|-------------------|---------------------|----------------|
| **Level 1: Low** | - Routine monitoring<br>- Low confidence requirements<br>- Limited distribution<br>- Minimal operational impact | - Single analyst verification<br>- Documentation of verification steps<br>- Compliance with standard review checklist |
| **Level 2: Medium** | - Ongoing campaign analysis<br>- Medium confidence requirements<br>- Standard distribution<br>- Moderate operational impact | - Analyst verification<br>- Lead analyst approval<br>- Documented multi-source validation<br>- Technical validation where applicable |
| **Level 3: High** | - Strategic assessments<br>- High confidence requirements<br>- Wide distribution<br>- Significant operational impact | - Analyst verification<br>- Lead analyst review<br>- Manager approval<br>- Subject matter expert consultation<br>- Comprehensive validation documentation |
| **Level 4: Critical** | - Attribution claims<br>- Executive consumption<br>- External/partner sharing<br>- Direct action trigger<br>- Legal/regulatory implications | - Full analytical team review<br>- Multiple expert validations<br>- Senior leadership approval<br>- Legal/compliance review<br>- Full audit trail of verification |

## 5. Documentation Requirements

All GenAI-enabled intelligence products must maintain the following documentation:

### 5.1 Required Metadata

- **Prompt Information**: Full text of original and follow-up prompts
- **Model Information**: Specific model, version, and configuration used
- **Output History**: Unedited initial output and all revisions
- **Verification Actions**: Specific steps taken to verify content
- **Human Reviewers**: Identity and role of all human reviewers
- **References**: Sources used to verify factual claims
- **Approval Decision**: Final determination and approver identity
- **Attribution Statement**: Clear indication of GenAI contribution in product

### 5.2 Documentation System Implementation

The documentation should be maintained in a centralized system that:

1. Provides tamper-evident logging
2. Enforces required metadata fields
3. Maintains version history of all changes
4. Supports structured review workflows
5. Enables audit and compliance verification
6. Integrates with existing CTI platforms when possible

A sample metadata schema is provided below:

```json
{
  "intelligence_id": "CTI-2025-0472",
  "criticality_level": 2,
  "genai_metadata": {
    "model_name": "APPROVED_MODEL_2",
    "model_version": "3.5",
    "prompt_text": "Analyze the following malware sample characteristics and identify potential attribution to known threat actors...",
    "prompt_timestamp": "2025-03-15T14:32:17Z",
    "raw_output_reference": "VAULT://CTI-2025-0472/raw_output.txt"
  },
  "verification": {
    "primary_reviewer": {
      "name": "Jane Smith",
      "role": "Malware Analyst",
      "verification_steps": [
        "Compared code similarities with MITRE ATT&CK database",
        "Validated technical claims with sandbox analysis",
        "Cross-referenced with three trusted external reports"
      ],
      "verification_timestamp": "2025-03-15T15:10:42Z",
      "verification_decision": "VERIFIED_WITH_MODIFICATIONS"
    },
    "secondary_reviewer": {
      "name": "Michael Chen",
      "role": "Lead Threat Analyst",
      "verification_notes": "Modified attribution confidence level from 'high' to 'moderate' based on limited sample size",
      "verification_timestamp": "2025-03-15T16:42:11Z",
      "verification_decision": "APPROVED"
    }
  },
  "external_references": [
    {"source": "MITRE ATT&CK", "reference": "T1055"},
    {"source": "VirusTotal", "reference": "VT-2025-00134"},
    {"source": "ThreatPartner Report", "reference": "TPR-2025-017"}
  ],
  "modification_history": [
    {"field": "attribution_confidence", "from": "high", "to": "moderate", "by": "Michael Chen", "timestamp": "2025-03-15T16:35:22Z"}
  ]
}
```

## 6. Escalation Procedures

### 6.1 Triggers for Escalation

Escalation is required when GenAI outputs:

1. Make high-confidence attribution claims without sufficient evidence
2. Contain potentially fabricated or hallucinated technical details
3. Present ethical concerns or potentially harmful content
4. Contradict established intelligence assessments without explanation
5. Demonstrate potential bias or systematic errors
6. Would trigger significant operational actions if accepted

### 6.2 Escalation Process

1. **Initial Flag**
   - Reviewer identifies escalation trigger
   - Documents specific concerns in oversight system
   - Temporarily halts product development

2. **Lead Review**
   - Lead analyst evaluates escalated concerns
   - Determines additional verification requirements
   - Sets appropriate escalation level

3. **Resolution Options**
   - **Reject**: Output deemed unreliable or problematic
   - **Verify**: Additional validation steps defined and executed
   - **Modify**: Content edited with appropriate caveats and justification
   - **Accept with Disclaimers**: Content used with clear limitations noted
   - **Escalate Further**: Refer to higher authority or specialized review

4. **Documentation**
   - Full escalation history maintained
   - Resolution decisions documented with rationale
   - Lessons captured for process improvement

## 7. Compliance Audit Procedures

### 7.1 Routine Compliance Checks

1. Daily spot checks of Level 1-2 intelligence products
2. Complete review of all Level 3-4 intelligence products
3. Weekly oversight metrics review
4. Monthly sampling of documentation completeness

### 7.2 Comprehensive Audits

1. Quarterly human oversight effectiveness assessment
2. Random sampling across all intelligence levels
3. Documentation completeness verification
4. Verification depth assessment
5. Escalation appropriateness review

### 7.3 Audit Documentation

For each audit, document:
1. Scope and methodology
2. Sample selection criteria
3. Identified compliance gaps
4. Required remediation actions
5. Process improvement recommendations

## 8. Integration with Existing Systems

The human oversight workflow should integrate with:

1. Existing intelligence management platforms
2. Knowledge management systems
3. Compliance and audit frameworks
4. Training and awareness programs
5. Security information and event management (SIEM) systems
6. Document management and version control systems

## 9. Implementation Checklist

- [ ] Define and document oversight roles and responsibilities
- [ ] Establish documentation system with required metadata fields
- [ ] Develop review checklists for each intelligence criticality level
- [ ] Create escalation procedures and communication channels
- [ ] Implement audit and compliance verification process
- [ ] Develop training for all oversight participants
- [ ] Establish metrics to evaluate oversight effectiveness
- [ ] Integrate with existing CTI workflows
- [ ] Conduct tabletop exercise to validate workflow
- [ ] Perform pilot implementation with limited scope
- [ ] Review and refine based on initial implementation
- [ ] Full deployment with compliance monitoring

## 10. Sample Review Checklist

### Factual Verification Checklist

✅ All technical claims verified with trusted sources  
✅ Attribution claims supported by multiple evidence points  
✅ Temporal claims and timelines validated against known events  
✅ Statistical or quantitative claims verified for accuracy  
✅ Technical indicators tested in controlled environment when applicable  
✅ Consistency checked against existing intelligence assessments  
✅ Context and implications validated by subject matter experts  
✅ Confidence levels appropriate to evidence quality and quantity  

### Bias and Quality Checklist

✅ Content checked for political, cultural, or organizational bias  
✅ Language reviewed for unwarranted certainty or hedging  
✅ Assessment of alternate hypotheses included where appropriate  
✅ Limitations and knowledge gaps explicitly acknowledged  
✅ Clear distinction between fact and analysis  
✅ Appropriate qualification of speculative content  
✅ Consistent quality of analysis across the product  

## 11. Training Requirements

All personnel involved in the oversight process must complete:

1. Initial training on oversight procedures
2. Hands-on exercises with verification tools
3. Escalation scenario simulations
4. Model-specific hallucination awareness training
5. Documentation system technical training
6. Quarterly refresher sessions
7. Compliance requirements briefing

---

*This workflow implementation guidance aligns with CTI-AI-3 (Human Oversight Requirement) control requirements and should be customized to reflect your organization's specific needs, scale, and existing CTI processes.* 