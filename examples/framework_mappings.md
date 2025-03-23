![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# Framework Mapping Analysis

This document provides comprehensive mapping analysis between CTI-AIU Framework controls and established security and AI governance frameworks. Each table demonstrates how specific portions of referenced frameworks align with and support the objectives of CTI-AI controls.

## CTI-AI-1: Use of Generative AI in Cyber Threat Intelligence

| Framework | Link | Mapped Controls | Relationship to CTI-AI-1 |
|-----------|------|-----------------|--------------------------|
| NIST SP 800-53 Rev. 5 | [NIST](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) | PL-1 (Policy and Procedures) | Directly supports the requirement to establish, document and maintain GenAI usage policies |
| | | AT-2 (Awareness Training) | Aligns with the requirement to train personnel on GenAI capabilities and limitations |
| | | AU-12 (Audit Record Generation) | Addresses the need for audit and monitoring of GenAI system usage |
| | | RA-3 (Risk Assessment) | Maps to conducting risk assessments of GenAI systems used in CTI |
| | | CA-7 (Continuous Monitoring) | Supports continuous monitoring requirements for GenAI systems |
| | | CM-3 (Configuration Change Control) | Relates to maintaining model documentation and version control |
| | | PM-9 (Risk Management Strategy) | Underpins the risk management approach for GenAI in CTI operations |
| NIST AI RMF | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | Govern 1 (AI Risk Management Governance) | Directly addresses organizational governance of AI risk in CTI operations |
| | | Govern 2 (Accountability) | Maps to preserving human accountability in intelligence production |
| | | Map 1 (AI System Context) | Supports understanding GenAI system context within CTI workflows |
| | | Map 2 (AI Risk Identification) | Aligns with risk assessment requirements for GenAI systems |
| ISO/IEC 42001:2023 | [ISO/IEC 42001](https://www.iso.org/standard/81230.html) | 6.1 (Actions to address risks and opportunities) | Supports risk assessment requirement for GenAI in CTI |
| | | 7.2 (Competence) | Maps to personnel training requirements |
| | | 7.5 (Documented information) | Aligns with policy documentation and model documentation requirements |
| | | 9.1 (Monitoring, measurement, analysis and evaluation) | Supports audit and monitoring requirements |
| ISO/IEC 27001:2022 | [ISO/IEC 27001](https://www.iso.org/standard/27001) | A.5.1 (Information security policies) | Provides foundation for GenAI usage policies in security context |
| | | A.6.7 (Threat intelligence) | Directly relates to CTI-specific operations involving GenAI |
| | | A.8.9 (Management of technical vulnerabilities) | Supports risk assessment of GenAI technical vulnerabilities |
| MITRE ATLAS | [MITRE ATLAS](https://atlas.mitre.org/) | TTP Identification and Analysis Use Cases | Relates to GenAI use in threat actor TTPs identification |
| | | Threat Intelligence Extraction Use Cases | Directly maps to GenAI use for intelligence extraction |
| European AI Act (Proposed) | [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | Article 9 (Risk management system) | Aligns with risk assessment requirements |
| | | Article 13 (Transparency and provision of information) | Supports transparency requirements in GenAI usage |
| CISA Secure AI Framework | [CISA Framework](https://www.cisa.gov/topics/technology-security/artificial-intelligence-security) | Governance Component | Directly supports policy and procedure requirements |
| | | Security Component | Addresses technical controls and monitoring requirements |

## CTI-AI-2: Ethical Use Enforcement

| Framework | Link | Mapped Controls | Relationship to CTI-AI-2 |
|-----------|------|-----------------|--------------------------|
| NIST SP 800-53 Rev. 5 | [NIST](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) | PM-1 (Program Management Policy and Procedure) | Supports establishing ethical use framework and policies |
| | | SR-11 (Component Authenticity) | Relates to ensuring authentic and unmanipulated GenAI outputs |
| | | CA-2 (Control Assessments) | Maps to assessments of ethical controls and adversarial testing |
| | | IR-8 (Incident Response Plan) | Aligns with ethical escalation procedures for violations |
| | | SA-8 (Security Engineering Principles) | Supports designing ethical principles into GenAI implementations |
| | | AT-3 (Role-Based Training) | Maps to ethical training for different roles in the CTI workflow |
| | | AC-4 (Information Flow Enforcement) | Relates to output filtering mechanisms |
| | | PL-9 (Central Management) | Supports centralized management of ethical controls |
| NIST AI RMF | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | Govern 3 (Accountability) | Directly supports accountability requirements in ethical framework |
| | | Govern 4 (Organizational Risk Management) | Maps to organization-wide ethical risk governance |
| | | Map 3 (AI Risk Classification) | Supports classifying ethical risks in GenAI systems |
| | | Measure 1 (AI Risk Assessment) | Aligns with adversarial testing for ethical violations |
| | | Manage 1 (AI Risk Response and Documentation) | Maps to documenting ethical review outcomes |
| | | Manage 3 (AI Risk Oversight) | Relates to establishing ethical escalation procedures |
| ISO/IEC 42001:2023 | [ISO/IEC 42001](https://www.iso.org/standard/81230.html) | 6.1.2 (AI-related risk assessment and opportunities) | Supports ethical risk assessment requirements |
| | | 6.2 (AI management system objectives and planning) | Maps to objectives in ethical use framework |
| | | 8.1 (Operational planning and control) | Aligns with implementing ethical controls in operations |
| | | 9.2 (Internal audit) | Supports verification of ethical compliance |
| ISO/IEC 24368:2022 | [ISO/IEC 24368](https://www.iso.org/standard/78507.html) | Clause 5 (Foundational values) | Directly maps to ethical foundations required in GenAI use |
| | | Clause 6 (Trustworthiness) | Supports ensuring trustworthy GenAI outputs |
| | | Clause 9 (Transparency) | Aligns with transparency requirements in ethical framework |
| IEEE EAD | [IEEE EAD](https://ethicsinaction.ieee.org/) | Principle 1 (Human Rights) | Supports protecting human rights in GenAI applications |
| | | Principle 2 (Well-being) | Maps to non-maleficence requirement in ethical framework |
| | | Principle 3 (Data Agency) | Relates to data governance aspects of ethical GenAI use |
| OECD AI Principles | [OECD AI Principles](https://www.oecd.org/digital/artificial-intelligence/) | Principle 1.1 (Inclusive growth, sustainable development and well-being) | Supports broader societal ethical considerations |
| | | Principle 1.2 (Human-centered values and fairness) | Directly maps to fairness requirements in ethical framework |
| | | Principle 1.5 (Transparency and explainability) | Aligns with transparency aspects of ethical controls |
| MITRE ATLAS | [MITRE ATLAS](https://atlas.mitre.org/) | Ethical Analysis Use Cases | Directly supports ethical analysis of GenAI outputs |
| | | Bias Detection and Mitigation Categories | Maps to identifying and addressing bias in GenAI systems |
| European AI Act | [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | Article 10 (Data governance and quality) | Aligns with data quality aspects of ethical use |
| | | Article 15 (Conformity assessment) | Maps to assessments of ethical conformity |
| | | Article 16 (Transparency obligations) | Supports transparency requirements in ethical framework |

## CTI-AI-3: Human Oversight Requirement

| Framework | Link | Mapped Controls | Relationship to CTI-AI-3 |
|-----------|------|-----------------|--------------------------|
| NIST SP 800-53 Rev. 5 | [NIST](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) | AC-5 (Separation of Duties) | Supports defining distinct roles in human oversight workflow |
| | | AU-6 (Audit Record Review, Analysis, and Reporting) | Maps to documenting verification activities |
| | | CM-3 (Configuration Change Control) | Relates to tracking changes made during human review |
| | | PM-14 (Testing, Training, and Monitoring) | Aligns with testing oversight effectiveness requirements |
| | | CA-9 (Internal System Connections) | Supports integrating human review into connected systems |
| | | PS-7 (Third-Party Personnel Security) | Maps to oversight requirements for external GenAI services |
| | | IR-4 (Incident Handling) | Relates to escalation protocols for uncertain content |
| | | PM-30 (Supply Chain Risk Management Strategy) | Addresses oversight of GenAI systems in the supply chain |
| NIST AI RMF | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | Govern 3.9 (Human Considerations) | Directly addresses human-centered design in AI systems |
| | | Govern 3.3 (AI Risk Management Alignment and Integration) | Maps to integrating oversight into risk management |
| | | Map 4 (Documentation Procedures) | Supports documentation of human review processes |
| | | Measure 2 (AI Systems Testing) | Aligns with testing oversight effectiveness |
| | | Manage 2.5 (Human Involvement) | Directly supports human-in-the-loop implementation |
| | | Manage 2.2 (AI Transparency) | Relates to transparency of human oversight activities |
| ISO/IEC 42001:2023 | [ISO/IEC 42001](https://www.iso.org/standard/81230.html) | 5.3 (Organizational roles, responsibilities and authorities) | Maps to assigning clear accountability requirements |
| | | 7.2 (Competence) | Supports ensuring human reviewers have necessary skills |
| | | 7.4 (Communication) | Relates to communication in oversight workflows |
| | | 8.1 (Operational planning and control) | Supports implementing formal review workflows |
| | | 9.3 (Management review) | Maps to oversight assessment at management level |
| ISO/IEC 27001:2022 | [ISO/IEC 27001](https://www.iso.org/standard/27001) | A.5.10 (Information security in project management) | Supports incorporating human oversight into projects |
| | | A.5.11 (Remote working) | Addresses human oversight in distributed environments |
| | | A.5.17 (Segregation of duties) | Directly maps to separation of duties in oversight |
| | | A.5.37 (Documented operating procedures) | Supports documentation of oversight procedures |
| ISO/IEC TR 24028:2020 | [ISO/IEC TR 24028](https://www.iso.org/standard/77608.html) | 9.3 (Accountability) | Maps to clear accountability requirements |
| | | 9.4 (Human oversight) | Directly supports human oversight implementation |
| UNESCO Recommendation | [UNESCO AI Ethics](https://www.unesco.org/en/artificial-intelligence/recommendation-ethics) | Principle 34 (Human autonomy and oversight) | Directly addresses human autonomy in AI systems |
| | | Principle 97 (Human determination) | Supports human decision-making primacy |
| MITRE ATLAS | [MITRE ATLAS](https://atlas.mitre.org/) | Human-in-the-Loop Analysis Methodology | Directly maps to human analysis methodology |
| | | Adversarial ML Pattern Analysis | Supports human review of adversarial patterns |
| European AI Act | [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | Article 14 (Human oversight) | Directly addresses human oversight requirements |
| | | Article 29 (Obligations of users of high-risk AI systems) | Maps to user obligations for oversight |
| ENISA Guidelines | [ENISA AI Guidelines](https://www.enisa.europa.eu/publications/artificial-intelligence-cybersecurity-challenges) | Governance principle (Accountability and responsibility) | Supports accountability in human oversight |
| | | Human agency principle (Human autonomy and oversight) | Directly maps to human autonomy in review processes |

## CTI-AI-4: Model Risk Assessment and Validation

| Framework | Link | Mapped Controls | Relationship to CTI-AI-4 |
|-----------|------|-----------------|--------------------------|
| NIST SP 800-53 Rev. 5 | [NIST](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) | RA-3 (Risk Assessment) | Directly supports developing a GenAI risk framework |
| | | SA-11 (Developer Testing and Evaluation) | Maps to pre-deployment evaluation requirements |
| | | CA-2 (Control Assessments) | Supports assessment of GenAI controls |
| | | SR-8 (Supply Chain Risk Management) | Addresses risks in GenAI supply chain |
| | | SI-7 (Software, Firmware, and Information Integrity) | Relates to integrity of GenAI model components |
| | | CA-7 (Continuous Monitoring) | Maps to continuous monitoring requirements |
| | | PM-9 (Risk Management Strategy) | Supports risk management strategy for GenAI |
| | | PM-28 (Risk Framing) | Relates to framing risk context for GenAI |
| NIST AI RMF | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | Map 1 (AI System Context) | Supports understanding GenAI system context |
| | | Map 2 (AI Risk Identification) | Directly maps to risk identification requirements |
| | | Map 3 (AI Risk Classification) | Supports classifying GenAI risks by impact |
| | | Measure 1 (AI Risk Assessment) | Directly addresses risk assessment methodology |
| | | Measure 2 (AI Systems Testing) | Maps to validation testing requirements |
| | | Measure 4 (AI Documentation) | Supports documentation of assessment procedures |
| | | Manage 1 (AI Risk Response and Documentation) | Maps to risk response requirements |
| | | Manage 4 (Awareness and Training) | Relates to training on risk assessment |
| ISO/IEC 23894:2023 | [ISO/IEC 23894](https://www.iso.org/standard/77304.html) | 6.1 (Actions to address risks and opportunities) | Supports risk framework development |
| | | 6.2 (AI risk identification) | Directly maps to risk identification processes |
| | | 6.3 (AI risk analysis) | Supports analysis of identified risks |
| | | 6.4 (AI risk evaluation) | Maps to risk evaluation methodology |
| | | 7.1 (AI risk treatment) | Relates to threshold-based restrictions |
| | | 8.1 (Monitoring, measurement, analysis and evaluation) | Supports continuous monitoring requirements |
| ISO/IEC 42001:2023 | [ISO/IEC 42001](https://www.iso.org/standard/81230.html) | 6.1 (Actions to address risks and opportunities) | Supports risk assessment framework |
| | | 9.1 (Monitoring, measurement, analysis and evaluation) | Maps to continuous monitoring requirements |
| | | 9.2 (Internal audit) | Supports validation through internal audit |
| | | 10.1 (Nonconformity and corrective action) | Relates to addressing identified risks |
| ISO/IEC TR 24029-1:2021 | [ISO/IEC TR 24029-1](https://www.iso.org/standard/77609.html) | Clause 6 (Reliability assessment and validation) | Directly maps to validation methodology |
| | | Clause 7 (Risks affecting reliability) | Supports identification of reliability risks |
| MITRE ATLAS | [MITRE ATLAS](https://atlas.mitre.org/) | AI Risk Mitigation & Model Assessment Use Cases | Directly relates to model assessment methods |
| | | Risk & Test Orchestration Framework | Supports orchestration of risk testing |
| | | Validation Methods for AI Integrity | Maps to validation requirements for integrity |
| European AI Act | [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | Article 9 (Risk management system) | Directly addresses risk management requirements |
| | | Article 10 (Data and data governance) | Maps to data aspects of model risk |
| | | Article 17 (Quality management system) | Supports quality management of risk processes |
| ENISA Guidelines | [ENISA AI Guidelines](https://www.enisa.europa.eu/publications/artificial-intelligence-cybersecurity-challenges) | Resilience principle (Accuracy, robustness, and security) | Maps to resilience aspects of risk assessment |
| | | Accuracy principle (Performance indicators and accuracy metrics) | Supports validation through performance metrics |

## CTI-AI-5: Data Integrity Controls

| Framework | Link | Mapped Controls | Relationship to CTI-AI-5 |
|-----------|------|-----------------|--------------------------|
| NIST SP 800-53 Rev. 5 | [NIST](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) | SI-7 (Software, Firmware, and Information Integrity) | Directly addresses integrity of input data |
| | | AU-9 (Protection of Audit Information) | Supports protection of data provenance records |
| | | SA-8 (Security Engineering Principles) | Relates to designing integrity into data workflows |
| | | SR-3 (Supply Chain Information Integrity) | Maps to integrity of data from external sources |
| | | SI-10 (Information Input Validation) | Directly addresses input validation requirements |
| | | SC-8 (Transmission Confidentiality and Integrity) | Supports integrity during data transmission |
| | | CM-14 (Signed Components) | Maps to cryptographic verification of data |
| | | SI-4 (System Monitoring) | Supports monitoring for data integrity issues |
| NIST AI RMF | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | Map 4 (Documentation Procedures) | Maps to documenting data lineage |
| | | Map 2.2 (Data Collection) | Directly addresses data collection controls |
| | | Measure 1.2 (Data Quality) | Maps to data quality validation requirements |
| | | Measure 2.1 (AI Performance Testing) | Supports testing with validated data |
| | | Manage 2.2 (AI Transparency) | Relates to transparency of data usage |
| | | Manage 3.3 (Incident Response) | Maps to responding to data poisoning |
| ISO/IEC 42001:2023 | [ISO/IEC 42001](https://www.iso.org/standard/81230.html) | 7.5 (Documented information) | Supports data documentation requirements |
| | | 8.3 (Design and development of AI systems) | Maps to data integrity in design phase |
| | | 8.5 (Control of AI system components from external providers) | Addresses integrity of external data |
| | | 8.6 (AI system validation) | Supports validation of data inputs |
| ISO/IEC 27001:2022 | [ISO/IEC 27001](https://www.iso.org/standard/27001) | A.5.33 (Protection of records) | Maps to provenance tracking requirements |
| | | A.8.9 (Management of technical vulnerabilities) | Supports managing data vulnerabilities |
| | | A.8.10 (Information systems audit considerations) | Maps to auditing data integrity |
| | | A.8.11 (Information systems test management) | Supports testing data controls |
| | | A.12.2.1 (Controls Against Malware) | Relates to protection against data poisoning |
| | | A.8.2.1 (Classification of Information) | Maps to classification of trusted sources |
| ISO/IEC TR 24027:2021 | [ISO/IEC TR 24027](https://www.iso.org/standard/77607.html) | 5.2 (Data provenance) | Directly supports data provenance requirements |
| | | 5.4 (Data preparation) | Maps to data validation processes |
| | | 6.1 (Bias identification and measurement) | Supports identifying bias in data |
| CISA Guidelines | [CISA Guidelines](https://www.cisa.gov/topics/technology-security/artificial-intelligence-security) | Data 1.1 (Maintain data integrity) | Directly addresses data integrity requirements |
| | | Data 1.2 (Document all data sources) | Maps to documentation of data sources |
| | | Data 1.3 (Track data provenance) | Directly supports provenance tracking |
| | | Testing 2.1 (Establish repeatable testing methodologies) | Maps to consistent data validation |
| MITRE ATLAS | [MITRE ATLAS](https://atlas.mitre.org/) | Data Poisoning Detection and Prevention | Directly addresses data poisoning controls |
| | | Training Data Verification Techniques | Maps to data verification processes |
| | | Source Validation Methodologies | Supports validation of data sources |
| European AI Act | [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | Article 10 (Data and data governance) | Directly maps to data governance requirements |
| | | Article 12 (Record-keeping) | Supports data provenance documentation |
| | | Article 15 (Conformity assessment) | Maps to validation of data controls |
| ENISA Guidelines | [ENISA AI Guidelines](https://www.enisa.europa.eu/publications/artificial-intelligence-cybersecurity-challenges) | Data Governance principle | Directly addresses data governance requirements |
| | | Security principle | Maps to security aspects of data integrity |

## CTI-AI-6: Red Teaming and Model Evaluation

| Framework | Link | Mapped Controls | Relationship to CTI-AI-6 |
|-----------|------|-----------------|--------------------------|
| NIST SP 800-53 Rev. 5 | [NIST](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) | CA-2 (Control Assessments) | Supports assessment through red teaming |
| | | CA-8 (Penetration Testing) | Directly maps to adversarial testing requirements |
| | | RA-5 (Vulnerability Monitoring and Scanning) | Supports identifying vulnerabilities through testing |
| | | SA-11 (Developer Testing and Evaluation) | Maps to testing in development phase |
| | | SA-15 (Development Process, Standards, and Tools) | Relates to integrating testing into development |
| | | SI-2 (Flaw Remediation) | Supports remediation of identified flaws |
| | | CM-4 (Impact Analyses) | Maps to analyzing impact of discovered issues |
| | | PM-15 (Security and Privacy Groups and Associations) | Supports external evaluator engagement |
| NIST AI RMF | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | Measure 1.2 (Fairness Evaluation) | Maps to evaluating fairness in models |
| | | Measure 2.1 (AI System Performance) | Supports performance evaluation |
| | | Measure 2.2 (Adversarial Testing) | Directly addresses adversarial testing |
| | | Measure 3.2 (Red Team Testing) | Explicitly supports red teaming requirements |
| | | Measure 3.3 (Independent Verification) | Maps to external evaluator requirements |
| | | Govern 3.3 (External Evaluation) | Supports external evaluation processes |
| | | Map 1.5 (Evaluation Process) | Maps to establishing evaluation processes |
| ISO/IEC 42001:2023 | [ISO/IEC 42001](https://www.iso.org/standard/81230.html) | 9.1 (Monitoring, measurement, analysis, and evaluation) | Supports measurement of testing results |
| | | 9.2 (Internal audit) | Maps to internal red team activities |
| | | 9.3 (Management review) | Relates to review of test findings |
| | | 10.1 (Continual improvement) | Supports improvement based on findings |
| | | 10.2 (Nonconformity and corrective action) | Maps to addressing identified issues |
| ISO/IEC TR 24029-1:2021 | [ISO/IEC TR 24029-1](https://www.iso.org/standard/77609.html) | Assessments of the robustness of neural networks | Directly maps to robustness testing |
| | | Formal verification methods for autonomous systems | Supports verification methodologies |
| | | Security vulnerability testing | Maps to security testing requirements |
| ISO/IEC 23894:2023 | [ISO/IEC 23894](https://www.iso.org/standard/77304.html) | Risk assessment procedures | Supports risk-based testing approaches |
| | | Testing procedures for AI systems | Directly maps to testing methodology |
| MITRE ATLAS | [MITRE ATLAS](https://atlas.mitre.org/) | ML Testing Techniques and Tools | Directly supports testing techniques |
| | | Adversarial ML Tactics and Techniques | Maps to adversarial testing requirements |
| | | Model Security Assessment | Supports security assessment methodology |
| | | Red Teaming Methodologies | Directly addresses red teaming practices |
| | | Evasion Attack Simulation | Maps to specific attack simulation scenarios |
| OWASP MLSVS | [OWASP MLSVS](https://owasp.org/www-project-machine-learning-security-verification-standard/) | Section 7 (Model Security Verification Requirements) | Maps to model security verification |
| | | Section 8 (Model Operation Requirements) | Supports operational testing |
| | | Section 9 (Monitoring and Logging Requirements) | Relates to monitoring test outcomes |
| European AI Act | [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | Article 9 (Risk management system) | Supports risk-based testing approach |
| | | Article 15 (Conformity assessment) | Maps to assessment requirements |
| | | Article 17 (Quality management system) | Supports quality aspects of testing |
| | | Article 61 (Post-market monitoring) | Maps to continuous testing requirements |
| ENISA Guidelines | [ENISA AI Guidelines](https://www.enisa.europa.eu/publications/artificial-intelligence-cybersecurity-challenges) | Resilience principle | Supports testing for resilience |
| | | Security principle | Maps to security-focused testing |
| | | Accountability principle (Red Team Testing) | Directly addresses red teaming practices |

## CTI-AI-7: Transparency and Community Accountability

| Framework | Link | Mapped Controls | Relationship to CTI-AI-7 |
|-----------|------|-----------------|--------------------------|
| NIST SP 800-53 Rev. 5 | [NIST](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) | AC-21 (Information Sharing) | Directly supports information sharing requirements |
| | | PM-15 (Security and Privacy Groups and Associations) | Maps to community participation requirements |
| | | PM-28 (Risk Framing) | Supports transparent risk communication |
| | | SA-9 (External System Services) | Relates to transparency with external services |
| | | PM-25 (Minimization of PII) | Maps to privacy aspects in sharing |
| | | PM-16 (Threat Awareness Program) | Supports threat awareness through sharing |
| | | PM-24 (Data Transparency) | Directly addresses data transparency |
| | | IR-4 (Incident Handling) | Maps to transparency in incident response |
| NIST AI RMF | [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) | Govern 1.3 (Accountability) | Directly supports accountability requirements |
| | | Govern 2.1 (Public Transparency) | Explicitly addresses public transparency |
| | | Govern 2.3 (Shared Responsibility) | Maps to community accountability |
| | | Govern 3.1 (Community Engagement) | Directly supports community engagement |
| | | Govern 3.3 (External Evaluation) | Maps to external review requirements |
| | | Manage 2.1 (Explainability) | Supports explainability of GenAI outputs |
| | | Manage 2.2 (AI Transparency) | Directly addresses AI transparency |
| | | Manage 3.1 (Knowledge Management) | Maps to sharing knowledge and lessons learned |
| ISO/IEC 42001:2023 | [ISO/IEC 42001](https://www.iso.org/standard/81230.html) | 7.4 (Communication) | Supports communication requirements |
| | | 9.1.3 (Analysis and evaluation) | Maps to sharing analysis results |
| | | 10.1 (Continual improvement) | Supports community improvement |
| | | 10.2 (Nonconformity and corrective action) | Maps to transparency about issues |
| | | 10.3 (Continual improvement of AI management system) | Supports system improvements through sharing |
| ISO/IEC 38507:2022 | [ISO/IEC 38507](https://www.iso.org/standard/56641.html) | Governance implications of AI | Maps to governance transparency |
| | | Transparency and explainability requirements | Directly addresses transparency requirements |
| | | Stakeholder engagement | Supports community engagement |
| OECD AI Principles | [OECD AI Principles](https://www.oecd.org/digital/artificial-intelligence/) | Open publication of research findings | Directly supports sharing research |
| | | Cross-sectoral information sharing | Maps to information sharing requirements |
| | | Transparency in algorithmic decision making | Supports transparency in GenAI decisions |
| | | Public engagement | Maps to community engagement |
| MITRE ATLAS | [MITRE ATLAS](https://atlas.mitre.org/) | Collaborative Defense Methodologies | Directly supports collaborative defense |
| | | Threat Information Sharing | Maps to sharing threat information |
| | | Community-based Detection Strategies | Supports community detection approaches |
| European AI Act | [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | Article 13 (Transparency and provision of information) | Directly addresses transparency requirements |
| | | Article 50 (AI Regulatory Sandboxes) | Supports collaborative testing |
| | | Article 53 (Measures for small-scale providers) | Maps to accessibility for smaller organizations |
| | | Article 14 (Human oversight) | Relates to transparency of human involvement |
| | | Article 60 (EU database for high-risk AI systems) | Supports information sharing through databases |
| ENISA Guidelines | [ENISA AI Guidelines](https://www.enisa.europa.eu/publications/artificial-intelligence-cybersecurity-challenges) | Transparency principle | Directly addresses transparency requirements |
| | | Accountability principle | Maps to accountability requirements |
| | | Security principle (Information Sharing) | Supports information sharing practices |
| WEF Responsible Use | [WEF AI Guidelines](https://www.weforum.org/communities/gfc-on-ai-for-humanity) | Shared learnings on AI safety | Directly maps to sharing lessons learned |
| | | Collaborative improvement frameworks | Supports collaborative improvement |
| | | Open peer review processes | Maps to external review requirements | 