# CTI-AI-3

<div align="center" style="display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-bottom: 20px;">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue.svg" alt="Version: 1.0.0" />
  <img src="https://img.shields.io/badge/Status-Draft-orange.svg" alt="Status: Draft" />
  <img src="https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg" alt="Last Updated: 23 March 2025" />
  <img src="https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg" alt="License: CC BY-NC-ND 4.0" />
  <img src="https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg" alt="Maintainer: Center for Cyber Intelligence" />
  <img src="https://hits.sh/github.com/centerforcyberintelligence/CTI-AIU.svg?label=Views&color=6e5494" alt="Views" />
</div>

## **Human Oversight Requirement**

### **Control Statement**

Organizations shall require human analyst review and validation of all GenAI-generated outputs used in cyber threat intelligence (CTI) workflows. Under no circumstances shall GenAI outputs be used to support operational decision-making, attribution, intelligence reporting, or dissemination without formal human oversight and accountability.

---

### **Control Objectives**

- Ensure that human analysts remain the final authority in CTI workflows augmented by GenAI.
    
- Preserve analytic integrity by preventing overreliance on unaudited AI-generated content.
    
- Provide organizational safeguards against the risks of hallucination, model bias, and factual distortion.
    
- Strengthen trust in CTI outputs used to inform executive, legal, or tactical actions.
    

---

### **Control Requirements**

Organizations must:

1. **Define Formal Review Workflows**  
    Establish documented procedures for human analyst review, including specific validation steps, approval criteria, and quality gates for GenAI outputs.
    
2. **Document Verification Activities**  
    Record all validation actions taken by human analysts, including corrections, rejections, or approvals of GenAI-generated content.
    
3. **Assign Clear Accountability**  
    Designate specific roles and responsibilities for the oversight of GenAI outputs, ensuring traceability to accountable individuals for each intelligence product.
    
4. **Maintain Approval Records**  
    Preserve records of human review decisions, including reviewer identity, timestamp, approval status, and verification methods for all GenAI content used in intelligence products.
    
5. **Implement Escalation Protocols**  
    Create formal escalation paths for instances where GenAI outputs require additional verification, contain uncertain information, or pose high-risk assessment challenges.
    
6. **Test Oversight Effectiveness**  
    Regularly assess the effectiveness of human oversight procedures through blind testing, accuracy verification, and control validation exercises.

7. **Executive Reporting Requirements**
    Define standardized metrics and reporting formats for executive visibility into GenAI use, effectiveness, and compliance. Establish a cadence for leadership briefings on GenAI deployment status, risk posture, and material changes to model capabilities. Create executive-level dashboards that provide meaningful oversight without requiring technical expertise.

8. **GenAI Incident Response Planning**
    Develop GenAI-specific incident response procedures for handling model failures, output inaccuracies, or manipulation events in intelligence products. These procedures should include containment strategies, notification protocols for affected intelligence consumers, and remediation steps for compromised analysis. Document the criteria for declaring a GenAI incident, escalation thresholds, and post-incident review requirements.

---

### **Assessment Criteria**

To assess conformance with this control, auditors or internal reviewers should:

- Verify the existence of documented human oversight procedures specific to GenAI use in CTI.
    
- Examine intelligence products for evidence of human analyst attribution and approval.
    
- Review logs of verification activities, including rejection rates and correction patterns.
    
- Confirm that AI-generated content is clearly identified in all intelligence outputs.
    
- Evaluate the effectiveness of oversight through testing and performance metrics.
    
- Verify that escalation processes function as designed when questionable content is detected.
    

---

### **Implementation Considerations**

- The level of human oversight should be proportional to the criticality and sensitivity of the intelligence being produced.
    
- Organizations with limited resources can implement basic review checklists, while mature teams may develop multi-stage validation pipelines.
    
- Consider implementing "human-in-the-loop" design patterns at multiple stages of the intelligence lifecycle, not just at the final review.
    
- Balance thorough oversight with operational tempo requirements to avoid creating bottlenecks in time-sensitive intelligence functions.
    

---

### **Cross-References**

- NIST SP 800-53 Rev. 5:
  - AC-5 (Separation of Duties)
  - AU-6 (Audit Record Review, Analysis, and Reporting)
  - CM-3 (Configuration Change Control)
  - PM-14 (Testing, Training, and Monitoring)
  - CA-9 (Internal System Connections)
  - PS-7 (Third-Party Personnel Security)
  - IR-4 (Incident Handling)
  - PM-30 (Supply Chain Risk Management Strategy)

- NIST AI RMF:
  - Govern 3.9 (Human Considerations)
  - Govern 3.3 (AI Risk Management Alignment and Integration)
  - Map 4 (Documentation Procedures)
  - Measure 2 (AI Systems Testing)
  - Manage 2.5 (Human Involvement)
  - Manage 2.2 (AI Transparency)

- ISO/IEC 42001:2023:
  - 5.3 (Organizational roles, responsibilities and authorities)
  - 7.2 (Competence)
  - 7.4 (Communication)
  - 8.1 (Operational planning and control)
  - 9.3 (Management review)

- ISO/IEC 27001:2022:
  - A.5.10 (Information security in project management)
  - A.5.11 (Remote working)
  - A.5.17 (Segregation of duties)
  - A.5.37 (Documented operating procedures)

- ISO/IEC TR 24028:2020:
  - 9.3 (Accountability)
  - 9.4 (Human oversight)

- UNESCO Recommendation on Ethics of AI:
  - Principle 34 (Human autonomy and oversight)
  - Principle 97 (Human determination)

- MITRE ATLAS:
  - Human-in-the-Loop Analysis Methodology
  - Adversarial ML Pattern Analysis

- European AI Act (Proposed):
  - Article 14 (Human oversight)
  - Article 29 (Obligations of users of high-risk AI systems)

- ENISA Guidelines:
  - Governance principle (Accountability and responsibility)
  - Human agency principle (Human autonomy and oversight)

### **Related Controls**
- [CTI-AI-1](./CTI-AI-1.md): Use of Generative AI in CTI
- [CTI-AI-2](./CTI-AI-2.md): Ethical Use Enforcement
- [CTI-AI-4](./CTI-AI-4.md): Model Risk Assessment and Validation
- [CTI-AI-7](./CTI-AI-7.md): Transparency and Community Accountability

### **Additional Resources**
- For a complete overview of all controls, see [Whitepaper.md](./Whitepaper.md)
- For information on contributing enhancements to this control, see [CONTRIBUTE.md](./CONTRIBUTE.md)