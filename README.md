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
- [Publication gates](framework/publication-gates.md)
- [Usage-aware efficiency](framework/usage-aware-efficiency.md)
- [Architecture diagrams](diagrams/README.md)
- [Evidence contract template](templates/evidence-contract.md)
- [Architecture decision record template](templates/architecture-decision-record.md)
- [Model card template](templates/model-card.md)
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
5. Document the decision using the [ADR template](templates/architecture-decision-record.md).
6. Use the [publication gates](framework/publication-gates.md) before releasing the result.
7. Revisit the capability when cost, source quality, interpretation, or public value changes.

## Origin

The framework grew from the architecture work behind **Toronto Public Transit Service Pulse**, an independent civic product that uses public transit and community data. The case study is included to show how the framework can be applied, but the framework is designed for use beyond transit.

Toronto Public Transit Service Pulse is not an official TTC platform or TTC website.

## Referencing the framework

Use the citation metadata in [CITATION.cff](CITATION.cff). Attribution should identify the **Civic Evidence Architecture Framework**, Donald Williams, and the repository URL.

## Licence

Documentation, diagrams, and templates are licensed under [Creative Commons Attribution 4.0 International](LICENSE.md). You may share and adapt the material with attribution.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Contributions should improve clarity, responsible evidence use, or practical adoption without introducing product-specific secrets or implementation code.
