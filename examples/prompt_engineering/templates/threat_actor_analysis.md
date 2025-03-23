![Version: 1.0](https://img.shields.io/badge/Version-1.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-orange.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# Threat Actor Analysis Prompt Template

This template provides a structured approach for using GenAI to analyze threat actor behavior, patterns, and attribution while adhering to CTI-AIU control requirements. The template is designed to minimize hallucination risk, enforce human verification, and maintain ethical boundaries.

## Template Structure

```
[SYSTEM CONTEXT]
You are assisting a cyber threat intelligence analyst in examining potential attribution and behavioral patterns for a threat actor. Adhere to the following constraints:
1. Distinguish clearly between confirmed facts, analytical judgments, and speculative assessments
2. Indicate confidence levels (low/medium/high) for all analytical statements
3. Explicitly identify information gaps and limitations in the analysis
4. Request additional information when evidence is insufficient for attribution
5. Avoid making definitive attribution claims without multiple evidence points
6. Format your response in the requested structured format
7. Provide alternative hypotheses when appropriate
8. Do not include any harmful TTPs or operational guidance that could enable offensive actions
9. Only reference TTPs from established frameworks like MITRE ATT&CK, using their identifiers
10. Attach confidence scores to all attributions (1-5 scale)

[INTELLIGENCE CONTEXT]
The following information represents observed technical indicators, behaviors, and contextual details about the threat activity:

{Insert factual observations, known TTPs, indicators, victimology, and contextual information here}

[ANALYSIS REQUEST]
Based solely on the provided information and your knowledge of historical threat actors current as of your training data, analyze:

1. Potential attribution to known threat actors based on TTPs, with confidence scores
2. Behavioral patterns and consistency with known operations
3. Capability assessment with supporting evidence
4. Motivation assessment with supporting evidence
5. Potential alternative attributions with rationale
6. Critical information gaps that would strengthen or refute attribution

Format your analysis using the following structure:
```

## Example Usage

```
[SYSTEM CONTEXT]
You are assisting a cyber threat intelligence analyst in examining potential attribution and behavioral patterns for a threat actor. Adhere to the following constraints:
1. Distinguish clearly between confirmed facts, analytical judgments, and speculative assessments
2. Indicate confidence levels (low/medium/high) for all analytical statements
3. Explicitly identify information gaps and limitations in the analysis
4. Request additional information when evidence is insufficient for attribution
5. Avoid making definitive attribution claims without multiple evidence points
6. Format your response in the requested structured format
7. Provide alternative hypotheses when appropriate
8. Do not include any harmful TTPs or operational guidance that could enable offensive actions
9. Only reference TTPs from established frameworks like MITRE ATT&CK, using their identifiers
10. Attach confidence scores to all attributions (1-5 scale)

[INTELLIGENCE CONTEXT]
The following information represents observed technical indicators, behaviors, and contextual details about the threat activity:

- Target: Financial services organizations in Southeast Asia
- Initial Access: Spear-phishing emails with malicious Excel documents claiming to be financial reports
- Excel documents contain macros that use DLL side-loading technique
- C2 infrastructure uses HTTPS communications with TLS certificates mimicking Microsoft domains
- Active hours of operation primarily align with UTC+8 timezone (East Asia)
- Dwell time on compromised networks averages 45-60 days
- Exfiltration observed via encrypted ZIP files to legitimate cloud storage platforms
- No data destruction or ransomware deployment observed
- Use of legitimate system administration tools for lateral movement
- Observed IOCs:
  * C2 domains: financereport-secure[.]com, asia-ms-update[.]com
  * Malware hash: 7e91f4238348ce6d18eadcd10d1c28459f7983f1715c4b2165dedca5c356acf2
  * User-Agent string: Mozilla/5.0 (Windows NT 10.0; Win64; x64) MSIE/18.0

[ANALYSIS REQUEST]
Based solely on the provided information and your knowledge of historical threat actors current as of your training data, analyze:

1. Potential attribution to known threat actors based on TTPs, with confidence scores
2. Behavioral patterns and consistency with known operations
3. Capability assessment with supporting evidence
4. Motivation assessment with supporting evidence
5. Potential alternative attributions with rationale
6. Critical information gaps that would strengthen or refute attribution

Format your analysis using the following structure:
```

## Expected Response Format

The response should follow this structured format:

```
## Threat Actor Analysis

### 1. Attribution Assessment

**Primary Attribution Hypothesis**:
- Likely Actor: [Actor Name] (Confidence Score: [1-5])
- Supporting Evidence:
  * [TTP match 1] - [MITRE ID if applicable]
  * [TTP match 2] - [MITRE ID if applicable]
  * [Infrastructure similarity]
  * [Targeting consistency]
- Confidence Level: [Low/Medium/High]
- Rationale: [Analytical reasoning]

### 2. Behavioral Pattern Analysis

**Observed Patterns**:
- [Pattern 1]
- [Pattern 2]
- [Pattern 3]

**Consistency with Known Operations**:
- Consistent elements: [List]
- Inconsistent elements: [List]
- Analysis: [Reasoning]

### 3. Capability Assessment

**Technical Sophistication**: [Low/Medium/High]
- Evidence:
  * [Evidence point 1]
  * [Evidence point 2]

**Operational Discipline**: [Low/Medium/High]
- Evidence:
  * [Evidence point 1]
  * [Evidence point 2]

### 4. Motivation Assessment

**Primary Assessed Motivation**: [Espionage/Financial/Disruption/Hacktivism]
- Supporting Evidence:
  * [Evidence point 1]
  * [Evidence point 2]
- Confidence Level: [Low/Medium/High]

### 5. Alternative Hypotheses

**Alternative 1**: [Actor Name] (Confidence Score: [1-5])
- Supporting Factors: [List]
- Contradicting Factors: [List]

**Alternative 2**: [Actor Name] (Confidence Score: [1-5])
- Supporting Factors: [List]
- Contradicting Factors: [List]

### 6. Information Gaps

**Critical Missing Information**:
- [Gap 1]
- [Gap 2]
- [Gap 3]

**Recommended Collection Requirements**:
- [Requirement 1]
- [Requirement 2]
```

## Human Verification Requirements

After receiving the GenAI analysis, the following verification steps must be performed:

1. Cross-reference all attributed TTPs with authoritative sources on the suggested threat actors
2. Verify timeline consistency with known threat actor activities
3. Check for any factual errors or unsupported claims
4. Validate infrastructure similarities using independent technical analysis
5. Compare with previous intelligence reports on similar activity
6. Ensure all confidence assessments are appropriate to the evidence quality
7. Confirm that information gaps are accurately identified

## Security Considerations

This template incorporates several CTI-AIU control requirements:

- **CTI-AI-2** (Ethical Use): Constraints prevent harmful content generation
- **CTI-AI-3** (Human Oversight): Format facilitates verification and review
- **CTI-AI-4** (Risk Assessment): Confidence scoring minimizes impact of hallucinations
- **CTI-AI-5** (Data Integrity): Clear separation of provided facts from analysis
- **CTI-AI-7** (Transparency): Attribution clearly tied to specific evidence

---

*This template aligns with CTI-AI controls requirements and should be customized to reflect your organization's specific threat intelligence requirements, tools, and processes.* 