![Version: 1.0](https://img.shields.io/badge/Version-1.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# CTI-AI-1
## Use of Generative AI in Cyber Threat Intelligence

### **Control Statement**
Organizations employing Generative AI (GenAI) for cyber threat intelligence (CTI) operations shall establish, document, and maintain policies and procedures to ensure the ethical, secure, and verifiable use of GenAI systems in intelligence generation, analysis, dissemination, and decision support processes. These policies must address the use of GenAI in all lifecycle stages of CTI: collection, processing, analysis, production, and dissemination.

---
### **Control Objectives**
- Ensure GenAI usage aligns with established intelligence tradecraft principles.
- Prevent the unvetted dissemination of AI-generated misinformation or disinformation.
- Maintain clear attribution, provenance, and documentation for all GenAI outputs used in CTI.
- Preserve human accountability in intelligence production and operational decision-making.
- Enable post-incident review and forensic traceability of AI-assisted analysis.

---
### **Control Requirements**
Organizations must:

1. **Develop and Maintain Policies**  
   Define acceptable use policies for GenAI in CTI activities, covering use cases, restrictions, review processes, and accountability mechanisms.
    
2. **Conduct Risk Assessments**  
   Periodically evaluate the risks associated with GenAI systems used in CTI, including model drift, hallucination, bias, and adversarial misuse.
    
3. **Enforce Human Oversight**  
   All GenAI outputs used in threat intelligence products or decisions are required to undergo a formal review by qualified analysts before dissemination or action.
    
4. **Record Provenance Metadata**  
   Store metadata for each GenAI-generated output, including prompt history, model version, timestamp, reviewer identity, and post-processing actions.
    
5. **Implement Technical Controls**  
   Apply technical safeguards to prevent prompt injection, unauthorized model access, and output manipulation.
    
6. **Train Personnel**  
   Ensure CTI professionals are trained on GenAI capabilities, limitations, ethical risks, and proper validation techniques.
    
7. **Audit and Monitor Usage**  
   Continuously monitor GenAI system use and conduct periodic audits to identify unauthorized use, policy violations, or oversight failure points.
    
8. **Maintain Model Documentation**  
   Keep internal documentation of model versions, training data provenance, tuning procedures, and evaluation metrics for each GenAI system deployed in CTI.

---
### **Assessment Criteria**
To assess conformance with this control, auditors or internal reviewers should:

- Verify the existence and currency of a documented GenAI usage policy.
- Confirm that outputs used in intelligence reports are traceable to source prompts and model configurations.
- Review logs for analyst approvals and oversight records.
- Inspect risk assessment reports for GenAI systems.
- Evaluate training completion records for staff using or reviewing GenAI outputs.
- Check for monitoring alerts or audit findings related to GenAI misuse or malfunctions.

### **Implementation Considerations**
- Smaller organizations may adopt lightweight policies and use third-party GenAI platforms with built-in safeguards. At the same time, larger entities may require in-house model evaluation pipelines and custom risk-scoring frameworks.
- Consider integration with existing governance tools (e.g., SIEM, GRC platforms) for audit and monitoring automation.
- Align with procurement processes to ensure new GenAI tools meet control requirements before acquisition or deployment.
- Engage legal and compliance teams early to ensure policy alignment with data protection laws and AI governance standards (e.g., EU AI Act, NIST AI RMF).

### **Cross-References**
- NIST SP 800-53 Rev. 5:
  - PL-1 (Policy and Procedures)
  - AT-2 (Awareness Training)
  - AU-12 (Audit Record Generation)
  - RA-3 (Risk Assessment)
  - CA-7 (Continuous Monitoring)
  - CM-3 (Configuration Change Control)
  - PM-9 (Risk Management Strategy)
- NIST AI RMF:
  - Govern 1 (AI Risk Management Governance)
  - Govern 2 (Accountability)
  - Map 1 (AI System Context)
  - Map 2 (AI Risk Identification)
- ISO/IEC 42001:2023:
  - 6.1 (Actions to address risks and opportunities)
  - 7.2 (Competence)
  - 7.5 (Documented information)
  - 9.1 (Monitoring, measurement, analysis and evaluation)
- ISO/IEC 27001:2022:
  - A.5.1 (Information security policies)
  - A.6.7 (Threat intelligence)
  - A.8.9 (Management of technical vulnerabilities)
- MITRE ATLAS:
  - TTP Identification and Analysis Use Cases
  - Threat Intelligence Extraction Use Cases
- European AI Act (Proposed):
  - Article 9 (Risk management system)
  - Article 13 (Transparency and provision of information)
- CISA Secure AI Framework:
  - Governance Component (Policies and Procedures)
  - Security Component (Monitoring and Response)

### **Related Controls**
- [CTI-AI-2](./CTI-AI-2.md): Ethical Use Enforcement
- [CTI-AI-3](./CTI-AI-3.md): Human Oversight Requirement
- [CTI-AI-7](./CTI-AI-7.md): Transparency and Community Accountability

### **Additional Resources**
- For a complete overview of all controls, see [Whitepaper.md](./Whitepaper.md)
- For information on contributing enhancements to this control, see [CONTRIBUTE.md](./CONTRIBUTE.md)