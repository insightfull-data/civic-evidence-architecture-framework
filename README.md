# Civic Evidence Architecture Framework

A practical, technology-neutral framework for turning public and approved data into civic evidence that people can understand, question, and reuse.

The framework begins with a civic question rather than a dashboard, model, or technology. It connects product design, data architecture, governance, privacy, security, quality, reliability, and operating cost in one decision process.

## Why this exists

Public-interest products often combine live observations, schedules, estimates, models, and community context. Those sources do not carry the same meaning. A product can be technically correct and still mislead people if it hides uncertainty, blurs evidence types, or publishes an experiment before its interpretation is ready.

This repository provides a reusable way to prevent that drift.

> Civic question -> evidence contract -> source acquisition -> validation -> transformation -> interpretation boundary -> public or private experience

## What is included

- [Architecture framework](framework/architecture-framework.md)
- [Evidence classification](framework/evidence-classification.md)
- [AI and agent governance](framework/ai-agent-governance.md)
- [MAPE-K bounded operational loop](framework/mape-k-operational-loop.md)
- [Standards and reference framework crosswalk](framework/standards-crosswalk.md)
- [Publication gates](framework/publication-gates.md)
- [Usage-aware efficiency](framework/usage-aware-efficiency.md)
- [Architecture diagrams](diagrams/README.md)
- [Evidence contract template](templates/evidence-contract.md)
- [Architecture decision record template](templates/architecture-decision-record.md)
- [Model card template](templates/model-card.md)
- [AI and agent governance assessment](templates/ai-agent-governance-assessment.md)
- [Data product card template](templates/data-product-card.md)
- [Fictional transit example](examples/fictional-transit-example.md)
- [Originating case study](case-studies/README.md)

## Core principles

1. Start with the civic question.
2. Preserve evidence classes from source to interface.
3. Separate experimentation from publication.
4. Prefer prepared, reusable evidence over repeated computation.
5. Design privacy and failure behavior before release.
6. Make compute and retention proportional to public value.
7. Keep every published claim traceable to its source, method, date, and limitations.
8. Retire capabilities when their value no longer justifies their burden.

## AI and agent governance

The framework now includes a dedicated, risk-proportionate approach for deterministic automation, machine-learning models, generative features, bounded agents, and automated decision systems.

The governance lifecycle covers use-case registration, capability and impact classification, approved data and tools, autonomy boundaries, evaluation, human oversight, public disclosure, monitoring, incident handling, pausing, and retirement. Controls become stronger as autonomy, data sensitivity, or potential impact increases. For bounded runtime operation, the framework adapts IBM's MAPE-K pattern: Monitor, Analyze, Plan, and Execute using shared Knowledge.

See [AI and Agent Governance](framework/ai-agent-governance.md), the [MAPE-K Bounded Operational Loop](framework/mape-k-operational-loop.md), and the reusable [governance assessment](templates/ai-agent-governance-assessment.md).

## Relationship to recognized frameworks

The framework is informed by established architecture, data-management, security, and responsible-AI references, including:

- [TOGAF Standard, 10th Edition](https://www.opengroup.org/togaf)
- [DAMA-DMBOK](https://dama.org/learning-resources/dama-data-management-body-of-knowledge-dmbok/)
- [NIST AI Risk Management Framework](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/)
- [ISO/IEC 42001:2023](https://www.iso.org/standard/81230.html)
- [ISO/IEC 27001:2022](https://www.iso.org/standard/27001)
- [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework)
- [OECD AI Principles](https://oecd.ai/en/ai-principles)
- [Government of Canada Algorithmic Impact Assessment](https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai/automated-decision-making/algorithmic-impact-assessment.html)
- [Microsoft Responsible AI](https://www.microsoft.com/en/ai/responsible-ai)
- [IBM Autonomic Computing Reference Architecture and MAPE-K](https://www.redbooks.ibm.com/redbooks/pdfs/sg246665.pdf)

The [standards crosswalk](framework/standards-crosswalk.md) explains conceptual alignment and boundaries. The repository does not claim certification, conformity, endorsement, or complete implementation of any referenced framework.

## Intended users

- Civic technology teams
- Open-data programs
- Municipal and public-sector analysts
- Community organizations
- Data product managers
- Researchers and journalists
- Teams building responsible models or bounded agents

## What this repository is not

This repository is not a deployable application, production topology, compliance certification, or substitute for legal, privacy, accessibility, security, or domain review. It intentionally excludes application source code, credentials, internal endpoints, production schemas, operational schedules, and proprietary model logic.

## Quick start

1. Write one civic question in plain language.
2. Complete the [evidence contract](templates/evidence-contract.md).
3. Classify every input using the [evidence classification](framework/evidence-classification.md).
4. Choose the lightest suitable processing and storage pattern.
5. If AI, a model, or an agent is involved, complete the [AI governance assessment](templates/ai-agent-governance-assessment.md).
6. Document the decision using the [ADR template](templates/architecture-decision-record.md).
7. Use the [publication gates](framework/publication-gates.md) before releasing the result.
8. Revisit the capability when cost, source quality, interpretation, or public value changes.

## Origin

The framework grew from the architecture work behind **Toronto Public Transit Service Pulse**, an independent civic product that uses public transit and community data. The case study is included to show how the framework can be applied, but the framework is designed for use beyond transit.

Toronto Public Transit Service Pulse is not an official TTC platform or TTC website.

## Referencing the framework

Use the citation metadata in [CITATION.cff](CITATION.cff). Attribution should identify the **Civic Evidence Architecture Framework**, Donald Williams, and the repository URL.

## Licence

Documentation, diagrams, and templates are licensed under [Creative Commons Attribution 4.0 International](LICENSE.md). You may share and adapt the material with attribution.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Contributions should improve clarity, responsible evidence use, or practical adoption without introducing product-specific secrets or implementation code.
