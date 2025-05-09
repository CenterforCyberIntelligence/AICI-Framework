# CTI-AIU | Control Framework for GenAI in Cyber Threat Intelligence

<div align="center" style="display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-bottom: 20px;">
  <img src="https://img.shields.io/badge/Version-1.0.1-blue.svg" alt="Version: 1.0.1" />
  <img src="https://img.shields.io/badge/Status-Draft-orange.svg" alt="Status: Draft" />
  <img src="https://img.shields.io/badge/Last_Updated-23_March_2025-teal.svg" alt="Last Updated: 23 March 2025" />
  <img src="https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg" alt="License: CC BY-NC-ND 4.0" />
  <img src="https://img.shields.io/badge/Maintainer-Center_for_Cyber_Intelligence-darkblue.svg" alt="Maintainer: Center for Cyber Intelligence" />
  <img src="https://hits.sh/github.com/centerforcyberintelligence/CTI-AIU.svg?label=Views&color=6e5494" alt="Views" />
</div>

<div align="center">
  <a href="https://github.com/centerforcyberintelligence/CTI-AIU">
    <img src="https://img.shields.io/badge/AI_Collaboration-OpenAI_＆_Claude-8A2BE2?style=for-the-badge&logo=openai&logoColor=white&labelColor=123456" alt="AI Co-Development" />
  </a>
</div>

## 📋 Framework Overview

The Artificial Intelligence for Cyber Intelligence (AICI) Framework is a comprehensive, community-driven standard for the responsible integration of Generative AI (GenAI) into Cyber Threat Intelligence (CTI) operations. Developed through open collaboration among industry experts, this framework establishes structured controls that transform GenAI from a potential liability into a strategic intelligence asset. By addressing unique challenges such as model hallucination, data integrity, and ethical usage, the framework enables organizations to leverage advanced AI capabilities while preserving the accuracy, objectivity, and reliability essential to effective intelligence tradecraft. The CTI-AIU control family provides actionable governance measures, technical safeguards, and operational procedures specifically tailored for GenAI applications across the intelligence lifecycle—from collection and analysis to dissemination and feedback. 

The framework offers a maturity-based implementation approach, allowing organizations of all sizes to adopt controls appropriate to their resources and requirements while establishing a clear pathway toward advanced capability integration.

### Core Controls:

- [CTI-AI-1](./CTI-AI-1.md): Use of Generative AI in CTI
- [CTI-AI-2](./CTI-AI-2.md): Ethical Use Enforcement
- [CTI-AI-3](./CTI-AI-3.md): Human Oversight Requirement
- [CTI-AI-4](./CTI-AI-4.md): Model Risk Assessment and Validation
- [CTI-AI-5](./CTI-AI-5.md): Data Integrity Controls
- [CTI-AI-6](./CTI-AI-6.md): Red Teaming and Model Evaluation
- [CTI-AI-7](./CTI-AI-7.md): Transparency and Community Accountability

## 📁 Repository Structure

```
CTI-AIU/
├── CTI-AI-*.md                 # Individual controls with detailed requirements
├── Whitepaper.md               # Full white paper (Markdown format)
├── LICENSE.md                  # CC BY-NC-ND 4.0 license terms
├── CONTRIBUTE.md               # Contribution guidelines
├── DOCUMENTATION_STANDARDS.md  # Documentation formatting standards
├── CHANGELOG.md                # Version history and release notes
├── ROADMAP.md                  # Development roadmap and planned enhancements
├── issues.md                   # Tracked issues and enhancement opportunities
├── examples/                   # Implementation examples and guidance
│   ├── framework_mappings.md   # Comprehensive framework mapping analysis
│   ├── implementation/         # Implementation examples organized by control
│   ├── prompt_engineering/     # Prompt templates and security patterns
│   │   ├── templates/          # Task-specific prompt templates
│   │   └── security/           # Security-focused prompt patterns
│   ├── validation_scenarios/   # Testing and verification scenarios
│   ├── audit_tooling/          # Assessment and compliance tools
│   └── config_templates/       # Configuration templates for tools and platforms
├── appendices/                 # Detailed appendices referenced in the whitepaper
│   ├── appendix_a_glossary.md  # Glossary of key terms
│   ├── appendix_b_assessment_checklist.md # Control assessment checklist
│   ├── appendix_c_prompts_and_validation.md # Example prompts and validation scenarios
│   └── appendix_d_resources.md # Selected resources for implementation
└── tools/                      # Optional tools and assessment templates
```

## 🚀 Getting Started

- Read [Whitepaper.md](./Whitepaper.md) to explore the control framework.
- Review individual controls (CTI-AI-*.md) for detailed requirements.
- Review [DOCUMENTATION_STANDARDS.md](./DOCUMENTATION_STANDARDS.md) for document formatting guidelines.
- Check [CHANGELOG.md](./CHANGELOG.md) for version history and recent updates.
- Explore [ROADMAP.md](./ROADMAP.md) for upcoming features, policy templates, and framework development plans.
- Explore [examples/](./examples/) for implementation guidance and practical templates.
- Review [CONTRIBUTE.md](./CONTRIBUTE.md) to learn how to provide feedback or suggest enhancements.

## 💡 How to Contribute

The CTI-AIU Control Framework is designed to be a community-driven standard that evolves with the rapid advancement of GenAI capabilities and threat landscapes. Contributors from CTI teams, AI/ML engineers, governance professionals, and security researchers are encouraged to participate.

To contribute:

1. Review individual controls and provide enhancement suggestions
2. Test controls in your environment and share feedback
3. Suggest new controls or implementation examples
4. See [CONTRIBUTE.md](./CONTRIBUTE.md) for more.

## 📋 Implementation Resources

The framework includes practical implementation resources to help organizations operationalize the controls:

- **Policy Templates**: Ready-to-customize templates for acceptable use, ethical guidelines, and governance
- **Workflow Documentation**: Detailed human oversight and verification workflow examples
- **Technical Implementations**: Data provenance tracking, metadata schemas, and API specifications
- **Prompt Engineering**: Templates and security patterns for effective GenAI use in CTI
- **Integration Guidance**: Code examples for integrating with common CTI platforms

These resources are available in the [examples/](./examples/) directory, organized by control and implementation type.

## ⚖️ License

This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/). You may share and redistribute the material in any format, but must give appropriate credit, provide a link to the license, and indicate if changes were made. You may not use the material for commercial purposes, nor distribute modified or derivative works. For details, see [LICENSE.md](./LICENSE.md).

## Contact

For inquiries or collaboration opportunities:
- Email: chris.cooley@centerforcyberintelligence.org
- Website: [Center for Cyber Intelligence](https://centerforcyberintelligence.org)
