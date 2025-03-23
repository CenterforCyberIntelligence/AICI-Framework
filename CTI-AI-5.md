![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# CTI-AI-5
## **Data Integrity Controls**

### **Control Statement**

Organizations shall implement data integrity controls for all datasets and prompts used to train, fine-tune, or interact with Generative AI (GenAI) systems supporting cyber threat intelligence (CTI) functions. Input data must be validated to ensure it is accurate, relevant, complete, and free from tampering, bias, or adversarial manipulation. No GenAI system shall be deployed or prompted using unverifiable or untrusted data sources.

---

### **Control Objectives**

- Ensure the fidelity, authenticity, and contextual relevance of input data used in GenAI-enabled CTI workflows.
    
- Prevent the ingestion of malicious, outdated, or misleading data into GenAI systems.
    
- Protect against data poisoning attacks and manipulation of GenAI outputs through compromised input streams.
    
- Maintain alignment between GenAI system outputs and validated intelligence requirements and sources.
    

---

### **Control Requirements**

Organizations must:

1. **Establish a Data Validation Policy**  
    Develop and enforce a policy for validating all data inputs into GenAI systems. This includes source validation, content review, version control, and curation processes.
    
2. **Define Trusted Data Sources**  
    Maintain a list of pre-approved data repositories and knowledge bases that meet organizational standards for integrity, relevance, and reliability. Disallow prompt engineering or model fine-tuning with data from unvetted or anonymous sources.
    
3. **Verify Prompt Inputs in Real Time**  
    Implement controls to verify the validity and contextual appropriateness of user prompts prior to execution. Flag or block prompts that include unverifiable claims, non-attributable quotes, or adversarially crafted input.
    
4. **Implement Provenance Tracking**  
    Use cryptographic or metadata-based methods to track the origin, version, and modification history of all input data used for training, fine-tuning, or prompting.
    
5. **Detect and Respond to Data Poisoning**  
    Monitor for indicators of adversarial data manipulation or poisoning campaigns. Include integrity checks, anomaly detection, and sandboxing for suspicious data streams.
    
6. **Align Input Data with Intelligence Objectives**  
    Ensure that all data used in GenAI workflows directly supports Priority Intelligence Requirements (PIRs), analytic questions, or operational CTI needs. Discard irrelevant or tangential inputs.
    
7. **Restrict Use of Synthetic Data**  
    Clearly identify and limit the use of synthetic or AI-generated data in training or prompt inputs, unless explicitly tested and validated for accuracy and bias neutrality.
    

---

### **Assessment Criteria**

To assess conformance with this control:

- Review the data validation policy and confirm alignment with intelligence requirements and cybersecurity best practices.
    
- Verify that prompt inputs and data sources are screened for quality and authenticity.
    
- Inspect provenance metadata for training and prompting datasets.
    
- Evaluate system monitoring capabilities for detecting anomalous or malicious input behavior.
    
- Confirm that synthetic data use is documented, justified, and validated for impact on output fidelity.
    

---

### **Implementation Considerations**

- In environments with high prompt variability (e.g., interactive analyst systems), implement pre-prompt validation layers and guided prompt templates.
    
- For custom-trained models, implement data review boards or third-party audits during dataset construction.
    
- Integrate integrity checks with CI/CD pipelines used for retraining or updating GenAI systems.
    
- Input data controls should align with broader data governance and lifecycle management strategies used across CTI teams.
    

---

### **Cross-References**

- NIST SP 800-53 Rev. 5:
  - SI-7 (Software, Firmware, and Information Integrity)
  - AU-9 (Protection of Audit Information)
  - SA-8 (Security Engineering Principles)
  - SR-3 (Supply Chain Information Integrity)
  - SI-10 (Information Input Validation)
  - SC-8 (Transmission Confidentiality and Integrity)
  - CM-14 (Signed Components)
  - SI-4 (System Monitoring)

- NIST AI RMF:
  - Map 4 (Documentation Procedures)
  - Map 2.2 (Data Collection)
  - Measure 1.2 (Data Quality)
  - Measure 2.1 (AI Performance Testing)
  - Manage 2.2 (AI Transparency)
  - Manage 3.3 (Incident Response)

- ISO/IEC 42001:2023:
  - 7.5 (Documented information)
  - 8.3 (Design and development of AI systems)
  - 8.5 (Control of AI system components from external providers)
  - 8.6 (AI system validation)

- ISO/IEC 27001:2022:
  - A.5.33 (Protection of records)
  - A.8.9 (Management of technical vulnerabilities)
  - A.8.10 (Information systems audit considerations)
  - A.8.11 (Information systems test management)
  - A.12.2.1 (Controls Against Malware)
  - A.8.2.1 (Classification of Information)

- ISO/IEC TR 24027:2021 (Bias in AI systems):
  - 5.2 (Data provenance)
  - 5.4 (Data preparation)
  - 6.1 (Bias identification and measurement)

- CISA Secure AI Development Guidelines:
  - Data 1.1 (Maintain data integrity across all stages of the AI system lifecycle)
  - Data 1.2 (Document all data sources, processing, and usage)
  - Data 1.3 (Track data provenance and chain-of-custody)
  - Testing 2.1 (Establish repeatable testing methodologies)

- MITRE ATLAS:
  - Data Poisoning Detection and Prevention
  - Training Data Verification Techniques
  - Source Validation Methodologies

- European AI Act (Proposed):
  - Article 10 (Data and data governance)
  - Article 12 (Record-keeping)
  - Article 15 (Conformity assessment)

- ENISA Guidelines:
  - Data Governance principle (Data quality and integrity)
  - Security principle (State-of-the-art protection mechanisms)

### **Related Controls**
- [CTI-AI-1](./CTI-AI-1.md): Use of Generative AI in CTI
- [CTI-AI-2](./CTI-AI-2.md): Ethical Use Enforcement
- [CTI-AI-4](./CTI-AI-4.md): Model Risk Assessment and Validation
- [CTI-AI-6](./CTI-AI-6.md): Red Teaming and Model Evaluation

### **Additional Resources**
- For a complete overview of all controls, see [Whitepaper.md](./Whitepaper.md)
- For information on contributing enhancements to this control, see [CONTRIBUTE.md](./CONTRIBUTE.md)