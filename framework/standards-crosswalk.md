# Standards and Reference Framework Crosswalk

The Civic Evidence Architecture Framework is an implementation-oriented synthesis. It does not replace established architecture, data, security, or AI governance frameworks.

This crosswalk shows conceptual alignment and identifies where a team should consult the authoritative source. It does **not** claim certification, conformity, legal compliance, endorsement, or complete coverage.

**Last reviewed:** October 27, 2026

## Crosswalk

| Reference framework | Primary contribution | Alignment in this framework | Important boundary |
| --- | --- | --- | --- |
| [TOGAF Standard, 10th Edition](https://www.opengroup.org/togaf) | Enterprise architecture method, architecture domains, governance, stakeholder concerns, and lifecycle | Architecture principles, product surfaces, responsibility layers, decision records, staged change, and fitness tests | This repository is not a complete TOGAF Architecture Development Method implementation |
| [DAMA-DMBOK](https://dama.org/learning-resources/dama-data-management-body-of-knowledge-dmbok/) | Data governance, architecture, quality, metadata, security, integration, and lifecycle disciplines | Evidence contracts, semantic definitions, ownership, provenance, quality dimensions, retention, and data-product cards | This repository does not reproduce DAMA's copyrighted body of knowledge or cover every knowledge area |
| [NIST AI Risk Management Framework](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/) | Govern, Map, Measure, and Manage functions for AI risk | AI use-case registration, context and impact mapping, evaluation, monitoring, risk response, and retirement | The NIST AI RMF is broader and should be consulted directly; NIST is updating the framework |
| [ISO/IEC 42001:2023](https://www.iso.org/standard/81230.html) | Requirements for establishing, implementing, maintaining, and continually improving an AI management system | AI ownership, policy, lifecycle controls, monitoring, corrective action, and continual review | This repository is guidance, not an AI management system or certification package |
| [ISO/IEC 27001:2022](https://www.iso.org/standard/27001) | Information security management system and risk-based protection of confidentiality, integrity, and availability | Trust boundaries, access controls, secret handling, supplier awareness, incident response, and lifecycle review | No claim of ISO/IEC 27001 conformity or certification is made |
| [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework) | Govern, Identify, Protect, Detect, Respond, and Recover outcomes for cybersecurity risk | Security governance, inventories, access controls, monitoring, incident response, recovery, and architecture fitness checks | The framework provides high-level alignment, not a complete CSF Organizational Profile |
| [OECD AI Principles](https://oecd.ai/en/ai-principles) | Human rights and democratic values, transparency, robustness, safety, accountability, and inclusive benefit | Civic purpose, privacy, explanation, public limitations, robustness, accountability, and community-impact review | The principles are values-based and require contextual implementation |
| [Government of Canada Algorithmic Impact Assessment](https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai/automated-decision-making/algorithmic-impact-assessment.html) | Proportional assessment of automated-decision impact and corresponding mitigation | Risk tiers, early assessment, multidisciplinary review, human involvement, monitoring, documentation, and recourse | The AIA is mandatory in its defined federal-government context; this repository uses it only as a public reference unless it legally applies |
| [Microsoft Responsible AI Standard v2](https://www.microsoft.com/en/ai/responsible-ai) | Operational practices around fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability | Evaluation categories, disclosure, human oversight, safety boundaries, quality, and governance records | This repository does not reproduce Microsoft's internal requirements or imply Microsoft endorsement |

## How to use the crosswalk

### For enterprise architecture

Use TOGAF to place the civic product within business, data, application, and technology architecture. Use this repository to make evidence meaning, public interpretation, and publication gates more explicit within that architecture practice.

### For data management

Use DAMA-DMBOK for the wider data-management program. Use the evidence contract, semantic definitions, data-product card, quality dimensions, provenance, and retention rules here as practical implementation aids.

### For AI and agent governance

Use the NIST AI RMF to structure Govern, Map, Measure, and Manage activities. Use ISO/IEC 42001 when establishing a formal organizational AI management system. Use the OECD principles to test values and public accountability. Use the Canada AIA as an example of proportional impact assessment, where appropriate. Use vendor responsible-AI material as supplementary operational guidance, not as the only governance basis.

### For cybersecurity

Use NIST CSF 2.0 or an applicable security-management framework to establish organization-wide outcomes. Use ISO/IEC 27001 where an information security management system and possible certification are required. The security guidance in this repository is intentionally limited to architecture-level responsibilities.

## Suggested evidence package

An organization applying the framework can maintain:

1. Architecture principles and decision records
2. Data inventory, ownership, classification, and evidence contracts
3. Semantic definitions and lineage
4. Data-quality thresholds and monitoring
5. AI or model inventory with risk tiers
6. Model cards and agent policy records
7. Privacy, security, accessibility, and impact reviews
8. Test and evaluation evidence
9. Publication decisions and public disclosures
10. Incident, pause, correction, and retirement records

## Maintenance rule

Reference frameworks evolve. Review this crosswalk at least annually and whenever a referenced standard, law, organizational policy, or system purpose changes. Always rely on the authoritative source for current requirements.
