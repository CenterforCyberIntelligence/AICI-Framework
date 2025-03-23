# CTI-AIU Control Framework Documentation Standards

<div align="center" style="display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-bottom: 20px;">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue.svg" alt="Version: 1.0.0" />
  <img src="https://img.shields.io/badge/Status-Final-purple.svg" alt="Status: Final" />
  <img src="https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg" alt="Last Updated: 23 March 2025" />
  <img src="https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg" alt="License: CC BY-NC-ND 4.0" />
  <img src="https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg" alt="Maintainer: Center for Cyber Intelligence" />
  <img src="https://hits.sh/github.com/centerforcyberintelligence/CTI-AIU.svg?label=Views&color=6e5494" alt="Views" />
</div>


This document defines the standardized formatting and reference patterns to be used across all CTI-AIU Control Framework documentation, ensuring consistency and proper navigation between documents.

## Document Format

- All documentation must be written in Markdown (.md)
- Use consistent heading structure:
  - Level 1 (`#`) for document title
  - Level 2 (`##`) for major sections
  - Level 3 (`###`) for subsections
  - Level 4 (`####`) for minor sections
- Include a horizontal rule (`---`) between major sections for readability

## Link and Reference Standards

### Internal References

- **Control References**: Always use Markdown links with relative paths
  ```markdown
  [CTI-AI-1](./CTI-AI-1.md)
  ```
  
- **Framework Document References**: Use consistent naming and relative paths
  ```markdown
  [Whitepaper.md](./Whitepaper.md)
  [CONTRIBUTE.md](./CONTRIBUTE.md)
  [LICENSE.md](./LICENSE.md)
  ```

- **Example References**: Link to implementation examples where appropriate
  ```markdown
  [Acceptable Use Policy Template](./examples/implementation/CTI-AI-1/policy_templates/acceptable_use_policy.md)
  [Human Oversight Workflow](./examples/implementation/CTI-AI-3/review_workflows/human_oversight_workflow.md)
  ```

- **Never use wiki-style links** (`[[CTI-AI-1]]`) as these are not supported in standard Markdown

### External References

- **Standard References**: Include the standard name and number
  ```markdown
  NIST SP 800-53 Rev. 5: AC-2
  ISO/IEC 42001
  MITRE ATLAS
  ```

- **External Website Links**: Include descriptive text and full URL
  ```markdown
  [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
  ```

## Document Structure Standards

- **Control Documents**: Must include these sections in order:
  1. Control Statement
  2. Control Objectives
  3. Control Requirements
  4. Assessment Criteria
  5. Implementation Considerations
  6. Cross-References
  7. Related Controls
  8. Additional Resources

- **Reference Sections**: Use bullet points for all references
- **Standard Footer**: All control documents should include the same standardized footer:
  ```markdown
  ### **Additional Resources**
  - For a complete overview of all controls, see [Whitepaper.md](./Whitepaper.md)
  - For information on contributing enhancements to this control, see [CONTRIBUTE.md](./CONTRIBUTE.md)
  ```

## Control Document Template

```markdown
![Version: 1.0](https://img.shields.io/badge/Version-1.0-blue.svg)
![Status: Draft](https://img.shields.io/badge/Status-Draft-yellow.svg)
![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-green.svg)
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-red.svg)
![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)

# CTI-AI-*
## [Control Title]

### **Control Statement**
[A concise statement defining what the control requires organizations to do]

---
### **Control Objectives**
- [Objective 1]
- [Objective 2]
- [Objective 3]
- [Objective 4]

---
### **Control Requirements**
Organizations must:

1. **[Requirement 1]**  
   [Description of requirement 1]
    
2. **[Requirement 2]**  
   [Description of requirement 2]
    
3. **[Requirement 3]**  
   [Description of requirement 3]
    
4. **[Requirement 4]**  
   [Description of requirement 4]
    
5. **[Requirement 5]**  
   [Description of requirement 5]

---
### **Assessment Criteria**
To assess conformance with this control:

- [Assessment criterion 1]
- [Assessment criterion 2]
- [Assessment criterion 3]
- [Assessment criterion 4]
- [Assessment criterion 5]

### **Implementation Considerations**
- [Implementation consideration 1]
- [Implementation consideration 2]
- [Implementation consideration 3]
- [Implementation consideration 4]

### **Cross-References**
- NIST SP 800-53 Rev. 5:
  - [Control reference 1]
  - [Control reference 2]
- NIST AI RMF:
  - [Function/Category reference]
- ISO/IEC 42001:
  - [Control reference]
- MITRE ATLAS:
  - [Framework reference]

### **Related Controls**
- [CTI-AI-X](./CTI-AI-X.md): [Control name]
- [CTI-AI-Y](./CTI-AI-Y.md): [Control name]
- [CTI-AI-Z](./CTI-AI-Z.md): [Control name]

### **Additional Resources**
- For a complete overview of all controls, see [Whitepaper.md](./Whitepaper.md)
- For information on contributing enhancements to this control, see [CONTRIBUTE.md](./CONTRIBUTE.md)
```

## Appendices

- All appendices should be clearly delineated in the Whitepaper.md using Level 3 headings
- When appropriate, consider moving detailed appendices to separate files with clear cross-referencing

## Version Control

- Include version badges at the top of each document:
  ```markdown
  ![Version: 1.0](https://img.shields.io/badge/Version-1.0-blue.svg)
  ![Status: Draft](https://img.shields.io/badge/Status-Draft-yellow.svg)
  ![Last Updated: 23 March 2025](https://img.shields.io/badge/Last_Updated-23_March_2025-green.svg)
  ![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)
  ![Maintainer: Center for Cyber Intelligence](https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-red.svg)
  ![Views](https://img.shields.io/github/watchers/centerforcyberintelligence/CTI-AIU?label=Views&style=social)
  ```

Following these standards will ensure documentation consistency, proper cross-referencing, and improved navigability across the CTI-AIU Control Framework. 