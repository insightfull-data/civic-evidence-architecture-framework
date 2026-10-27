# Architecture Framework

## 1. Purpose

The Civic Evidence Architecture Framework helps teams translate public and approved data into evidence that supports a defined civic question.

It treats architecture as a responsibility system, not only a technology stack. The design must preserve meaning, provenance, uncertainty, privacy, limitations, reliability, and cost from source to public experience.

The objective is:

> Produce the most credible and useful civic evidence possible for each unit of data collection, compute, storage, network traffic, and maintenance effort.

## 2. Architecture position

A conventional dashboard often begins with available data and asks how to display it. A civic evidence product should begin with a public question and ask what evidence can responsibly support an answer.

The governing sequence is:

```text
Civic question
  -> evidence contract
  -> source acquisition
  -> validation
  -> normalization
  -> analysis or model
  -> interpretation boundary
  -> product experience
  -> monitoring and review
```

Technology is selected after evidence and responsibility requirements are understood.

## 3. Product surfaces

Mature civic platforms usually need more than one product surface.

| Surface | Purpose | Typical audience | Publication rule |
| --- | --- | --- | --- |
| Public product | Explain reviewed civic evidence | Residents, advocates, researchers, journalists, institutions | Sources, dates, methods, quality, and limitations are visible |
| Private lab | Develop and validate experiments | Approved researchers and administrators | Authentication required; results are not automatically public |
| Administration | Operate the platform | Platform operators | Secrets and operational records remain protected |
| Sandbox | Test governance, architecture, and controlled workflows | Authorized users and selected public explainers | Public explanations are separated from protected operations |

A shared platform does not imply shared access. Each surface carries a distinct trust and publication boundary.

## 4. Architecture principles

### 4.1 Start with the civic question

Every major capability should identify:

- The question it answers
- The audience that can use the answer
- The evidence required
- What the result can and cannot establish
- The necessary freshness
- The appropriate product surface

### 4.2 Preserve evidence classes

Observed, scheduled, estimated, modeled, and contextual information must remain distinguishable in data contracts, storage, methods, interfaces, and public wording.

### 4.3 Separate product maturity

Use controlled maturity stages:

1. Question defined
2. Source connected
3. Method prototyped
4. Data quality assessed
5. Private experiment operating
6. Interpretation reviewed
7. Public-ready evidence
8. Published and monitored

A technically functioning model is not automatically public-ready.

### 4.4 Prefer prepared evidence

Calculate stable or reusable evidence during builds or scheduled jobs, then serve it many times. Reserve request-time processing for current selections, live evidence, protected workflows, or calculations that cannot be prepared safely in advance.

### 4.5 Preserve failure meaning

Do not silently convert missing data into zero. Distinguish source failure, stale evidence, partial coverage, unavailable fields, suppression, and genuine zero values.

### 4.6 Keep models and agents bounded

Models and agents should have approved sources, permitted actions, prohibited actions, compute limits, retention rules, stop conditions, and an audit history.

## 5. Logical layers

### Source layer

Documents source ownership, licence, update frequency, schema, expected coverage, request limits, and fallback behavior.

### Acquisition and quality layer

Retrieves data with bounded requests and evaluates freshness, completeness, validity, consistency, coverage, and traceability.

### Normalization layer

Converts source-specific formats into stable, source-aware contracts while preserving timestamps, missing fields, evidence class, quality state, and warnings.

### Semantic layer

Defines the civic meaning, grain, key, source, allowed joins, evidence class, and interpretation boundary of shared concepts.

### Evidence and model layer

Produces current snapshots, historical evidence, screens, comparisons, scenarios, or bounded agent workflows using versioned methods.

### Storage and delivery layer

Selects static assets, bounded caches, current-state records, event history, or immutable snapshots according to purpose.

### Experience layer

Presents the result in the correct product surface with plain-language meaning, quality, source, date, and limitations.

## 6. Data product requirements

Treat each published or private output as a small data product with:

- A named civic question
- An intended audience
- An accountable owner
- Source contracts
- Quality checks
- A refresh cadence
- A method and version
- A publication status
- Interpretation boundaries
- Retention and retirement conditions

## 7. Processing patterns

| Pattern | Use when | Typical examples |
| --- | --- | --- |
| Build time | Evidence changes slowly or requires heavier preparation | Geographic assets, reference networks, static documentation |
| Scheduled | Shared evidence changes predictably | Observations, baselines, calendars, maintenance |
| Request time | A current selection or live source is required | Selected place, route, alert, or protected interaction |
| Persistent | Work cannot fit bounded execution and requires stable state or duration | Specialized long-running services |

Choose the lightest pattern that satisfies the evidence requirement.

## 8. Trust and security boundaries

- Public interfaces expose only information intended for publication.
- Authentication protects labs, administration, and operational sandbox functions.
- State changes require authorization, input validation, and auditable results.
- Credentials and internal operational detail remain server-side.
- Protected responses must not be publicly cached.
- Public architecture material should describe safeguards without exposing weaknesses.
- Dependencies and generated artifacts should be verified before release.

## 9. Privacy approach

Prefer grouped evidence and representative locations over resident-level tracking or household addresses.

Privacy controls may include:

- Aggregated geography
- Small-population suppression
- Purpose-limited retention
- Representative rather than household origins
- Clear separation between modeled agents and real people
- Consent before optional analytics
- Review when adding finer geography, linked history, communication, or behavioral inference

## 10. Quality and reliability

Every public measure should expose a human-readable quality state.

The system should use bounded requests, quality thresholds, explicit source timestamps, stale-state labels, partial-result behavior, idempotent writes, scheduler health, and documented failure reasons.

Graceful degradation protects meaning. When one source fails, retain what remains valid and explain what is missing.

## 11. Governance

Every model or agent should have:

- Purpose and owner
- Approved sources
- Permitted and prohibited actions
- Method or policy version
- Quality threshold
- Compute and retention limits
- Review state
- Public-claim boundary
- Audit record

AI, machine-learning, generative, and agent capabilities require controls proportional to their autonomy, data sensitivity, and potential impact. See [AI and Agent Governance](ai-agent-governance.md) for the risk tiers, lifecycle, bounded-agent controls, human oversight, evaluation, incident handling, and disclosure requirements.

The framework's relationship to established architecture, data, security, and AI references is documented in the [Standards and Reference Framework Crosswalk](standards-crosswalk.md).

## 12. Delivery and change control

Use a staged release process:

1. Build prepared evidence and product artifacts.
2. Run integrity, quality, security, and output checks.
3. Deploy to a stable review environment.
4. Review evidence, wording, mobile behavior, and accessibility.
5. Promote the reviewed artifact.
6. Run production checks and monitor results.

Record an architecture decision when a change adds a provider, persistent compute, a sensitive data class, a new evidence definition, materially different retention, autonomous action, public experiment, or cross-product dependency.

## 13. Architecture fitness tests

The framework is working when the team can answer yes:

- Can every public result be traced to a source and method?
- Can users distinguish observation, schedule, estimate, model, and context?
- Can a source fail without producing a misleading claim?
- Can an optional experiment pause without breaking the public product?
- Can costs be attributed to major workloads?
- Can historical results retain the method and policy used at the time?
- Can a new civic question be added without duplicating the full pipeline?
- Can a feature be retired when its value no longer justifies its burden?
