![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# CTI-AI-6
## **Red Teaming and Model Evaluation**

### **Control Statement**

Organizations shall conduct regular red teaming exercises and independent model evaluations to assess the security, resilience, and fidelity of Generative AI (GenAI) systems used in cyber threat intelligence (CTI). These exercises must simulate realistic adversarial scenarios and stress conditions, and their outcomes must inform mitigation strategies, configuration changes, or deployment restrictions.

---

### **Control Objectives**

- Identify vulnerabilities and limitations in GenAI systems before they are exploited or cause analytic failure.
    
- Simulate adversarial use cases and detect susceptibilities to prompt injection, data leakage, hallucination, or manipulation.
    
- Validate the robustness of GenAI systems under operational and edge-case conditions.
    
- Inform continuous improvement of models, policies, and oversight mechanisms based on empirical evidence.
    

---

### **Control Requirements**

Organizations must:

1. **Establish a Red Teaming Program**  
    Define a structured program for adversarial testing of GenAI systems. This includes assigning dedicated red team roles, documenting attack vectors, and conducting controlled evaluation exercises.
    
2. **Design Threat-Relevant Scenarios**  
    Develop red team scenarios that reflect plausible CTI misuse cases, including misinformation injection, geopolitical misclassification, foreign-language misrepresentation, or social engineering facilitation.
    
3. **Test for Model Exploitability**  
    Evaluate susceptibility to known model-level attacks, such as prompt injection, jailbreaking, latent bias exploitation, and context manipulation.
    
4. **Assess Hallucination Rates and Impact**  
    Measure and document hallucination frequency and severity across representative prompts. Include hallucination testing as part of the model release and update cycle.
    
5. **Use External Evaluators When Necessary**  
    For high-risk deployments or mission-critical GenAI applications, engage independent evaluators or third-party auditors with expertise in adversarial AI testing and red team operations.
    
6. **Document Findings and Mitigations**  
    Maintain detailed records of all red teaming activities, including test conditions, model behavior observations, vulnerabilities identified, and actions taken in response.
    
7. **Integrate Red Teaming into Model Lifecycle**  
    Require that red team evaluations be conducted prior to production use, after significant model updates, and on a recurring basis determined by the organization's risk appetite.

8. **Integration with Threat Modeling**
    Incorporate GenAI capabilities and limitations into threat modeling processes, ensuring intelligence analysts understand both the benefits and constraints when developing threat scenarios. Document how GenAI outputs should be incorporated into different threat modeling methodologies. Define verification steps for GenAI-generated threat scenarios before inclusion in risk assessments.
    

---

### **Assessment Criteria**

To assess conformance with this control:

- Review the documented red teaming program and verify its integration with the model evaluation lifecycle.
    
- Confirm that scenario design aligns with real-world threat intelligence operations.
    
- Inspect test reports showing model responses to adversarial inputs and edge cases.
    
- Assess whether red team findings have resulted in documented mitigations or policy changes.
    
- Verify involvement of qualified internal or external evaluators with domain-specific knowledge.
    

---

### **Implementation Considerations**

- Red team exercises should simulate both internal misuse (e.g., improper prompt construction) and external threats (e.g., manipulated open-source inputs).
    
- Ensure that evaluation tools include both manual testing and automated tools capable of generating adversarial examples.
    
- In joint CTI environments (e.g., ISACs, government coalitions), consider shared red teaming scenarios and distributed evaluation teams.
    
- Red teaming should not be limited to technical testing—test for cognitive bias induction, influence operations, and narrative framing errors introduced by GenAI.
    

---

### **Cross-References**

- NIST SP 800-53 Rev. 5:
  - CA-2 (Control Assessments)
  - CA-8 (Penetration Testing)
  - RA-5 (Vulnerability Monitoring and Scanning)
  - SA-11 (Developer Testing and Evaluation)
  - SA-15 (Development Process, Standards, and Tools)
  - SI-2 (Flaw Remediation)
  - CM-4 (Impact Analyses)
  - PM-15 (Security and Privacy Groups and Associations)

- NIST AI RMF:
  - Measure 1.2 (Fairness Evaluation)
  - Measure 2.1 (AI System Performance)
  - Measure 2.2 (Adversarial Testing)
  - Measure 3.2 (Red Team Testing)
  - Measure 3.3 (Independent Verification)
  - Govern 3.3 (External Evaluation)
  - Map 1.5 (Evaluation Process)

- ISO/IEC 42001:2023:
  - 9.1 (Monitoring, measurement, analysis, and evaluation)
  - 9.2 (Internal audit)
  - 9.3 (Management review)
  - 10.1 (Continual improvement)
  - 10.2 (Nonconformity and corrective action)

- ISO/IEC TR 24029-1:2021:
  - Assessments of the robustness of neural networks
  - Formal verification methods for autonomous systems
  - Security vulnerability testing

- ISO/IEC 23894:2023:
  - Risk assessment procedures
  - Testing procedures for AI systems

- MITRE ATLAS:
  - ML Testing Techniques and Tools
  - Adversarial ML Tactics and Techniques
  - Model Security Assessment
  - Red Teaming Methodologies
  - Evasion Attack Simulation

- OWASP Machine Learning Security Verification Standard:
  - Section 7 (Model Security Verification Requirements)
  - Section 8 (Model Operation Requirements)
  - Section 9 (Monitoring and Logging Requirements)

- European AI Act (Proposed):
  - Article 9 (Risk management system)
  - Article 15 (Conformity assessment)
  - Article 17 (Quality management system)
  - Article 61 (Post-market monitoring)

- ENISA Guidelines for Securing AI:
  - Resilience principle (Robustness and Redundancy)
  - Security principle (Threat Modeling)
  - Accountability principle (Red Team Testing)

### **Related Controls**
- [CTI-AI-1](./CTI-AI-1.md): Use of Generative AI in CTI
- [CTI-AI-2](./CTI-AI-2.md): Ethical Use Enforcement
- [CTI-AI-4](./CTI-AI-4.md): Model Risk Assessment and Validation
- [CTI-AI-5](./CTI-AI-5.md): Data Integrity Controls

### **Additional Resources**
- For a complete overview of all controls, see [Whitepaper.md](./Whitepaper.md)
- For information on contributing enhancements to this control, see [CONTRIBUTE.md](./CONTRIBUTE.md)