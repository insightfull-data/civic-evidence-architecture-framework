# Cost and Capacity Governance

Cost is an architectural constraint and an accountability signal. It should be considered when a workload is designed, not only after a provider invoice arrives.

## Objective

> Keep technology usage proportional to the evidence value a workload produces.

This approach connects operating cost with civic purpose, evidence quality, freshness, reliability, and public use. It is not a financial accounting system or a provider-specific configuration guide.

## What is governed

Cost governance covers:

- compute and function execution;
- provisioned memory and CPU;
- databases and retained records;
- observability events and log retention;
- network transfer and external API calls;
- builds, deployments, and stored artifacts;
- persistent workers and scheduled processing; and
- the human effort required to maintain a workload.

## Governing principles

### Attribute cost to a workload

Provider totals are insufficient for architectural decisions. Usage should be associated with a feature, experiment, data pipeline, or public evidence product.

### Connect cost to value

Every recurring workload should identify the question it answers, who can use the result, and why its processing frequency is necessary.

### Distinguish the evidence

Cost information should be labelled as provider-reported, allocated, estimated, or forecast. Estimates must not be presented as invoices.

### Use proportional controls

Small experimental workloads do not require enterprise-scale financial operations. Controls should grow with cost, risk, and operational dependency.

### Optimize the workload before the rate

Review execution frequency, caching, retention, observability volume, memory, CPU, and workload placement before relying on provider discounts.

### Design for pause and retirement

A recurring workload should have a defined method for reducing its frequency, pausing it, or retiring it without damaging unrelated evidence products.

## Workload lifecycle

1. **Register:** Identify the workload, owner, and evidence purpose.
2. **Estimate:** Identify likely cost drivers and expected usage.
3. **Guard:** Establish frequency, retention, and consumption boundaries.
4. **Observe:** Collect enough usage information to identify material changes.
5. **Review:** Compare operating burden with reliability and evidence value.
6. **Act:** Continue, optimize, redesign, pause, or retire the workload.

## Minimum workload record

| Field | Purpose |
| --- | --- |
| Civic or product question | Explains why the workload exists |
| Evidence output | Identifies what it produces |
| Processing pattern | Build-time, scheduled, request-time, or persistent |
| Freshness class | Describes how current the result must be |
| Cost categories | Compute, storage, transfer, observability, or external services |
| Cost evidence | Provider-reported, allocated, estimated, or forecast |
| Trend | Stable, increasing, decreasing, or unknown |
| Guardrails | Frequency, retention, or consumption boundaries |
| Failure behaviour | Describes what remains available when processing stops |
| Review decision | Continue, optimize, redesign, pause, or retire |

## Review triggers

A workload should be reviewed when:

- cost rises without a corresponding increase in use or evidence value;
- scheduled work repeatedly runs without producing a changed result;
- memory or CPU is disproportionate to the output;
- routine observability events become a major cost driver;
- the same source data is processed independently by several features;
- retained data exceeds its documented purpose;
- a persistent process could use scheduled or event-driven execution; or
- the requested freshness is greater than the public question requires.

## Public and private boundaries

The public framework may disclose principles, cost categories, decision criteria, workload classes, and reusable templates.

It must not disclose credentials, account identifiers, private endpoints, exact traffic volumes, detailed schedules, security configurations, provider tokens, private invoices, or production resource identifiers.

## Framework alignment

This component is informed by the [FinOps Framework](https://www.finops.org/framework/) concepts of value-based technology decisions, usage accountability, planning, and usage optimization. It does not represent formal FinOps adoption or certification.

