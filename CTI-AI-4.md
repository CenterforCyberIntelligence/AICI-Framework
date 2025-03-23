![Version: 1.0](https://img.shields.io/badge/Version-1.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# CTI-AI-4
## **Model Risk Assessment and Validation**

### **Control Statement**

Organizations shall conduct structured, periodic risk assessments of all Generative AI (GenAI) models used in cyber threat intelligence (CTI) workflows. These assessments must evaluate the operational, technical, and ethical risks associated with the models' use and determine their fitness for purpose in specific CTI tasks. Validation activities must accompany risk assessments to ensure that outputs are consistent, accurate, and aligned with mission requirements.

---

### **Control Objectives**

- Identify and mitigate systemic risks inherent to GenAI model behavior, including hallucination, bias, and drift.
    
- Ensure that models used in CTI generate outputs that are reliable, verifiable, and operationally relevant.
    
- Promote continuous evaluation of GenAI systems to prevent misuse, degradation, or unintended outcomes.
    
- Establish formal evidence for trustworthiness of GenAI systems prior to and during deployment in intelligence operations.
    

---

### **Control Requirements**

Organizations must:

1. **Develop a GenAI Risk Framework**  
    Define and document a structured framework for assessing GenAI risks in CTI contexts. The framework must include categories such as factual accuracy, adversarial vulnerability, reproducibility, model drift, data poisoning, and compliance risk.
    
2. **Conduct Pre-Deployment Evaluation**  
    Perform a baseline risk and validation assessment before any GenAI model is deployed in CTI workflows. This assessment must be completed by a multidisciplinary team with representation from technical, analytic, and compliance functions.
    
3. **Implement Continuous Monitoring**  
    Establish a schedule and methodology for ongoing risk evaluations throughout the model's lifecycle. This includes periodic revalidation in response to significant changes in model architecture, training data, or use case.
    
4. **Document Evaluation Procedures and Results**  
    Maintain records of all assessments, including methods used, scenarios tested, risk findings, mitigation plans, and approval decisions.
    
5. **Use Scenario-Based Testing**  
    Simulate real-world CTI use cases to test model performance under representative conditions. Include edge-case prompts and red team-generated adversarial queries in evaluations.
    
6. **Assess Alignment with Intelligence Objectives**  
    Validate that GenAI systems produce outputs that meet operational intelligence standards such as accuracy, relevance, timeliness, and analytic integrity.
    
7. **Implement Threshold-Based Use Restrictions**  
    Define quantitative thresholds for acceptable model risk levels. Restrict or prohibit use in CTI workflows when these thresholds are exceeded until remediation is complete.
    

---

### **Assessment Criteria**

To assess conformance with this control:

- Review the documented GenAI risk assessment framework and confirm alignment with CTI mission objectives.
    
- Verify pre-deployment validation records for each GenAI system in use.
    
- Inspect logs of periodic risk assessments and determine whether evaluations were conducted on schedule.
    
- Confirm inclusion of scenario-based and adversarial testing in risk assessments.
    
- Evaluate whether restrictions were applied when risk thresholds were breached.
    

---

### **Implementation Considerations**

- Risk frameworks should be adapted to the level of model customization—off-the-shelf GenAI services will require different risk criteria than in-house fine-tuned or domain-specific models.
    
- Smaller organizations may leverage external assessments or third-party certifications to supplement internal validation capabilities.
    
- Considerations should be given to shared models used across multiple CTI functions, where risks can compound across integrated workflows.
    
- Incorporate threat modeling to assess external attack surfaces on GenAI systems (e.g., prompt injection, data leakage).
    

---

### **Cross-References**

- NIST SP 800-53 Rev. 5:
  - RA-3 (Risk Assessment)
  - SA-11 (Developer Testing and Evaluation)
  - CA-2 (Control Assessments)
  - SR-8 (Supply Chain Risk Management)
  - SI-7 (Software, Firmware, and Information Integrity)
  - CA-7 (Continuous Monitoring)
  - PM-9 (Risk Management Strategy)
  - PM-28 (Risk Framing)

- NIST AI RMF:
  - Map 1 (AI System Context)
  - Map 2 (AI Risk Identification)
  - Map 3 (AI Risk Classification)
  - Measure 1 (AI Risk Assessment)
  - Measure 2 (AI Systems Testing)
  - Measure 4 (AI Documentation)
  - Manage 1 (AI Risk Response and Documentation)
  - Manage 4 (Awareness and Training)

- ISO/IEC 23894:2023 (Risk Management for AI):
  - 6.1 (Actions to address risks and opportunities)
  - 6.2 (AI risk identification)
  - 6.3 (AI risk analysis)
  - 6.4 (AI risk evaluation)
  - 7.1 (AI risk treatment)
  - 8.1 (Monitoring, measurement, analysis and evaluation)

- ISO/IEC 42001:2023:
  - 6.1 (Actions to address risks and opportunities)
  - 9.1 (Monitoring, measurement, analysis and evaluation)
  - 9.2 (Internal audit)
  - 10.1 (Nonconformity and corrective action)

- ISO/IEC TR 24029-1:2021 (AI Reliability):
  - Clause 6 (Reliability assessment and validation)
  - Clause 7 (Risks affecting reliability)

- MITRE ATLAS:
  - AI Risk Mitigation & Model Assessment Use Cases
  - Risk & Test Orchestration Framework
  - Validation Methods for AI Integrity

- European AI Act (Proposed):
  - Article 9 (Risk management system)
  - Article 10 (Data and data governance)
  - Article 17 (Quality management system)

- ENISA Guidelines:
  - Resilience principle (Accuracy, robustness, and security)
  - Accuracy principle (Performance indicators and accuracy metrics)

### **Related Controls**
- [CTI-AI-1](./CTI-AI-1.md): Use of Generative AI in CTI
- [CTI-AI-3](./CTI-AI-3.md): Human Oversight Requirement
- [CTI-AI-5](./CTI-AI-5.md): Data Integrity Controls
- [CTI-AI-6](./CTI-AI-6.md): Red Teaming and Model Evaluation

### **Additional Resources**
- For a complete overview of all controls, see [Whitepaper.md](./Whitepaper.md)
- For information on contributing enhancements to this control, see [CONTRIBUTE.md](./CONTRIBUTE.md)