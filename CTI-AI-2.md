![Version: 1.0](https://img.shields.io/badge/Version-1.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# CTI-AI-2
## Ethical Use Enforcement

### **Control Statement** 
Organizations shall embed ethical constraints within all Generative AI (GenAI) workflows supporting cyber threat intelligence (CTI). These constraints must prevent the production, reliance, or dissemination of outputs that violate fundamental ethical standards, propagate misinformation, reflect systemic bias, or otherwise compromise analytic objectivity and mission integrity.

---
### **Control Objectives**

- Prevent unethical use of GenAI in intelligence generation, processing, or reporting.
- Safeguard against harm caused by disinformation, stereotyping, or manipulated outputs.
- Promote the use of GenAI to reinforce the trustworthiness and accuracy of CTI products.
- Ensure outputs are consistent with organizational values and global ethical frameworks for AI usage.

---
### **Control Requirements**

Organizations must:

1. **Define an Ethical Use Framework**  
    Establish a documented ethical use policy specific to GenAI applications in CTI. This framework should align with non-maleficence, transparency, accountability, and fairness.
2. **Integrate Prompt-Level Safeguards**  
    Deploy technical controls to restrict prompts that may elicit unethical, biased, or misleading outputs. Include mechanisms for detecting manipulative or adversarial prompt design.
3. **Conduct Adversarial Testing**  
    Adversarial testing (e.g., red teaming, prompt stress testing) should be regularly performed to evaluate the ethical integrity of GenAI outputs under realistic and edge-case scenarios.
4. **Establish Ethical Escalation Procedures**  
    Create pathways for intelligence analysts, engineers, or auditors to report and escalate GenAI outputs that violate ethical norms. This should include formal review boards or ethics officers.
5. **Document Ethical Review Outcomes**  
    Maintain detailed records of flagged content, ethical reviews, decision outcomes, and any retraining or configuration adjustments made in response to violations.
6. **Engage Stakeholders in Governance**  
    Multidisciplinary teams—spanning legal, compliance, operational, and technical stakeholders—should be included in an ongoing review of GenAI policies and ethical evaluation protocols.
7. **Implement Output Filtering Mechanisms**  
    Apply post-generation filtering or moderation pipelines to detect and remove outputs containing hallucinated claims, disinformation, protected PII, or offensive language.

---
### **Assessment Criteria**

To assess conformance with this control:
- Confirm the existence of an approved, accessible ethical use framework for GenAI in CTI.
- Review logs or test cases from adversarial testing exercises and assess the coverage of ethical edge cases.
- Inspect filtering mechanisms for implementation efficacy and false positive/negative rates.
- Verify documentation of ethical review incidents and remediation steps.
- Confirm cross-functional participation in ethical oversight governance activities.

---
### **Implementation Considerations**

- Smaller organizations can rely on trusted third-party GenAI platforms with embedded content filtering and moderation features but must still perform independent ethical reviews.
- Larger organizations may benefit from dedicated AI ethics boards or internal GenAI councils to adjudicate complex edge cases and coordinate remediation strategies.
- Ethics reviews should be integrated into analytic validation workflows and not siloed from day-to-day operations.
- Consider leveraging public taxonomies of AI harms and biases (e.g., the AI Incident Database, and the Partnership on AI) to inform test cases and ethical training data.

---
### **Cross-References**

- NIST SP 800-53 Rev. 5:
  - PM-1 (Program Management Policy and Procedure)
  - SR-11 (Component Authenticity)
  - CA-2 (Control Assessments)
  - IR-8 (Incident Response Plan)
  - SA-8 (Security Engineering Principles)
  - AT-3 (Role-Based Training)
  - AC-4 (Information Flow Enforcement)
  - PL-9 (Central Management)

- NIST AI RMF:
  - Govern 3 (Accountability)
  - Govern 4 (Organizational Risk Management)
  - Map 3 (AI Risk Classification)
  - Measure 1 (AI Risk Assessment)
  - Manage 1 (AI Risk Response and Documentation)
  - Manage 3 (AI Risk Oversight)

- ISO/IEC 42001:2023:
  - 6.1.2 (AI-related risk assessment and opportunities)
  - 6.2 (AI management system objectives and planning)
  - 8.1 (Operational planning and control)
  - 9.2 (Internal audit)

- ISO/IEC 24368:2022 (AI Ethics):
  - Clause 5 (Foundational values)
  - Clause 6 (Trustworthiness)
  - Clause 9 (Transparency)

- IEEE Ethically Aligned Design (EAD):
  - Principle 1 (Human Rights)
  - Principle 2 (Well-being)
  - Principle 3 (Data Agency)

- OECD AI Principles:
  - Principle 1.1 (Inclusive growth, sustainable development and well-being)
  - Principle 1.2 (Human-centered values and fairness)
  - Principle 1.5 (Transparency and explainability)

- MITRE ATLAS:
  - Ethical Analysis Use Cases
  - Bias Detection and Mitigation Categories

- European AI Act (Proposed):
  - Article 10 (Data governance and quality)
  - Article 15 (Conformity assessment)
  - Article 16 (Transparency obligations)

### **Related Controls**
- [CTI-AI-1](./CTI-AI-1.md): Use of Generative AI in CTI
- [CTI-AI-3](./CTI-AI-3.md): Human Oversight Requirement
- [CTI-AI-6](./CTI-AI-6.md): Red Teaming and Model Evaluation
- [CTI-AI-7](./CTI-AI-7.md): Transparency and Community Accountability

### **Additional Resources**
- For a complete overview of all controls, see [Whitepaper.md](./Whitepaper.md)
- For information on contributing enhancements to this control, see [CONTRIBUTE.md](./CONTRIBUTE.md)

---