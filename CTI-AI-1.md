![Version: 1.0.1](https://img.shields.io/badge/Version-1.0.1-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# CTI-AI-1
## Use of Generative AI in Cyber Threat Intelligence

### **Control Statement**
Organizations employing Generative AI (GenAI) for cyber threat intelligence (CTI) operations shall establish, document, and maintain policies and procedures to ensure the ethical, secure, and verifiable use of GenAI systems in intelligence planning, collection, processing, analysis, production, and dissemination. These policies must address GenAI use in both routine and crisis intelligence operations, with special attention to high-consequence analysis.

---
### **Control Objectives**
- Ensure GenAI usage aligns with established intelligence tradecraft principles.
- Prevent the unvetted dissemination of AI-generated misinformation or disinformation.
- Maintain clear attribution, provenance, and documentation for all GenAI outputs used in CTI.
- Preserve human accountability in intelligence production and operational decision-making.
- Enable post-incident review and forensic traceability of AI-assisted analysis.
- Enable consistent and repeatable validation procedures across different GenAI systems and models.
- Establish clear boundaries for acceptable use cases versus prohibited applications.
- Promote continuous improvement through structured feedback mechanisms.

---
### **Control Requirements**
Organizations must:

### CTI-AI-1.1 Develop and Maintain Policies
   Define acceptable use policies for GenAI in CTI activities, covering use cases, restrictions, review processes, and accountability mechanisms. Review and update acceptable use policies annually or after significant changes to GenAI capabilities or organizational mission.

   Policies must include clear stakeholder roles and responsibilities across CTI functions, designating specific authority for approving GenAI deployments, and establishing change management procedures for model updates, retraining, and configuration modifications. Policies should address standard operating conditions and crisis response scenarios where expedited GenAI use might be necessary, with appropriate compensating controls for such situations. Create a centralized policy repository where analysts can access current GenAI usage guidelines, approved use cases, and prohibited applications.

#### CTI-AI-1.1a Classified and Sensitive Environment Considerations
   Establish specific controls for GenAI use in classified or sensitive intelligence environments, including air-gapped systems, compartmented information handling, and special access programs. Detail additional safeguards are required when GenAI processes classified information, including enhanced monitoring, specialized training, and extended data retention for accountability.

#### CTI-AI-1.1b Cross-Border and Multi-Jurisdictional Considerations
   Address jurisdictional constraints on GenAI operations in cross-border intelligence sharing and multinational environments. Document compliance approaches for varied regulatory requirements across operational regions. Implement controls to ensure GenAI use adheres to the most restrictive applicable regulations when operating across multiple jurisdictions.
    
### CTI-AI-1.3 Record Provenance Metadata
   Store metadata for each GenAI-generated output, including prompt history, model version, timestamp, reviewer identity, and post-processing actions; establish retention requirements for prompt/output pairs that align with intelligence product lifecycles.

   Provenance records should maintain chain-of-custody documentation for each GenAI interaction, including model configuration parameters, modification history of prompts, version control information, and complete prompt-response pairs. Implement cryptographic verification mechanisms to prevent tampering with provenance records. Design metadata schemas that facilitate the reproducibility of GenAI outputs while maintaining appropriate access controls. Establish a metadata taxonomy that supports intelligence product lifecycle requirements, including provisions for data minimization and retention alignment with organizational data governance policies.
    
### CTI-AI-1.4 Implement Technical Controls
   Apply technical safeguards to prevent prompt injection, unauthorized model access, and output manipulation.

   Technical safeguards should include role-based access controls for GenAI systems, segregation of duties between prompt engineering and output approval, and system-enforced approval workflows before dissemination. Deploy monitoring capabilities to detect anomalous usage patterns that might indicate misuse or compromise. Implement technical guardrails that enforce organizational policies through automation rather than relying solely on procedural controls. Consider architectural approaches that logically separate GenAI systems handling different intelligence classification levels or sensitivity categories.
    
### CTI-AI-1.5 Train Personnel
   Ensure CTI professionals are trained on GenAI capabilities, limitations, ethical risks, and proper validation techniques.

   Training programs should include hands-on practical exercises using realistic CTI scenarios, assessment of analyst competency in recognizing GenAI limitations, and regular refresher training reflecting evolving capabilities and threats. Create specialized training tracks for intelligence roles - from collection specialists to strategic analysts to executive briefers. Training should include incident response procedures specific to GenAI failures or manipulation events. Develop a formal certification process for analysts authorized to use or review GenAI outputs in operational intelligence production.
    
### CTI-AI-1.6 Audit and Monitor Usage
   Continuously monitor GenAI system use and conduct periodic audits to identify unauthorized use, policy violations, or oversight failure points.

   Establish continuous monitoring controls that track routine usage patterns and anomalous activities, with automated alerting for policy violations or suspicious behavior. Implement periodic compliance audits that test adherence to established GenAI use policies, reporting findings to appropriate governance bodies. Develop metrics that measure the effectiveness of controls, not just their implementation. Create cross-functional oversight committees with legal, privacy, security, and intelligence representatives to review audit findings and recommend improvements.
    
### CTI-AI-1.7 Maintain Model Documentation
   Keep internal documentation of model versions, training data provenance, tuning procedures, and evaluation metrics for each GenAI system deployed in CTI.

   Documentation should include model selection criteria, evaluation methodologies, performance metrics specific to CTI use cases, and technical specifications of deployed models. Maintain records of model limitations, known vulnerabilities, and operational constraints—document model dependencies, including software libraries, external data sources, and integration points with other systems. Create knowledge repositories that preserve historical performance data, enabling trend analysis and continuous improvement of model selection and implementation.

### CTI-AI-1.8 Define Prohibited Use Cases
   Document specific CTI functions, decisions, or outputs that must not rely on GenAI without extraordinary review and authorization.

   Explicitly document intelligence functions where GenAI should never be the sole source for analysis or decision support, such as high-confidence attribution, strategic warning, or escalation decisions. Establish a formal exception process for temporarily allowing restricted use cases under exceptional circumstances, including required approvals, compensating controls, and post-use review. Create clear criteria that define when GenAI outputs must be independently verified through multiple human analysts or alternative intelligence sources. Develop a classification scheme for intelligence products that indicates reliability based on the degree of GenAI involvement in their production.

### CTI-AI-1.9 Knowledge Management and Succession Planning
   Establish processes to capture organizational knowledge related to GenAI implementation, including successful prompt patterns, model-specific considerations, and integration techniques. Implement knowledge transfer protocols to maintain operational continuity during personnel transitions. Create a central repository of lessons learned, procedural documentation, and technical guidance accessible to authorized CTI personnel.

---
### **Assessment Criteria**
To assess conformance with this control, auditors or internal reviewers should:

- Conduct tabletop exercises simulating GenAI-related incidents or failures.
- Review documentation of rejected or heavily modified GenAI outputs to assess system limitations.
- Verify the existence of technical controls preventing unauthorized model access.
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
  - 9.1 (Monitoring, measurement, analysis, and evaluation)
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
