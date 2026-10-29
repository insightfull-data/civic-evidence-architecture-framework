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

## Select the lightest suitable processing pattern

Choose a processing pattern from the evidence requirement rather than from provider features.

| Pattern | Use when | Avoid when | Typical controls |
| --- | --- | --- | --- |
| Build-time or static | Evidence changes slowly and can be prepared before publication | People require current operational conditions | Rebuild trigger, artifact expiry, source date |
| Scheduled | Sources change at a known cadence and results can be reused | Every request requires unique processing | Run frequency, timeout, unchanged-result skip, retry limit |
| Request-time | The output depends on a current user request and cannot be safely prepared | The same expensive result is repeatedly requested | Cache, rate limit, execution timeout, bounded query |
| Event-driven or queued | Work should occur only after a meaningful change and can tolerate asynchronous completion | Immediate synchronous completion is essential | Queue depth, retry policy, deduplication, dead-letter handling |
| Persistent | State, connection duration, or continuous coordination is a documented requirement | Periodic or event-driven execution can provide the same evidence | Capacity floor, idle policy, health check, restart and pause control |

Revisit the selected pattern when freshness, use, source behaviour, or cost changes.

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

## Useful unit measures

Aggregate provider charges are useful for budgeting but weak for architectural diagnosis. Select one or more units that connect consumption to an output.

| Workload type | Example unit measure |
| --- | --- |
| Source collection | Cost per successful collection run |
| Data preparation | Cost per processed batch or million records |
| Public API | Cost per 1,000 valid requests |
| Static publication | Cost per published update |
| Model or simulation | Cost per completed and validated run |
| Retained evidence | Cost per retained dataset-month |
| Observability | Events or retained bytes per successful workload run |
| Public experience | Cost per useful session or completed evidence view |

The selected unit should not reward low-quality output. Pair it with evidence-quality, reliability, and freshness measures.

## Responsibilities

One person may hold several roles in a small project. The responsibilities should still be explicit.

| Responsibility | Accountable for |
| --- | --- |
| Product or civic owner | Question, intended users, evidence value, and continuation decision |
| Workload owner | Processing pattern, implementation, reliability, and optimization |
| Data owner or steward | Source suitability, quality, retention, and permitted use |
| Cost reviewer | Provider evidence, allocation method, trends, and forecast limitations |
| Governance reviewer | Privacy, security, public boundaries, and decision record |

## When to review

Thresholds are prompts for investigation, not universal limits. Teams should set them from their own scale, risk, and evidence needs. A review might begin when:

- monthly cost or a workload unit changes materially from its recent baseline;
- executions increase while successful outputs remain stable;
- most scheduled runs produce no changed evidence;
- memory or CPU is disproportionate to the output;
- observability volume grows faster than successful workload activity;
- the same source data is processed independently by several features;
- retained records pass their documented analytical period;
- persistent capacity remains idle when scheduled or event-driven execution could meet the need;
- requested freshness is greater than the civic question requires; or
- source failures create repeated retries without a useful public update.

Document the baseline, observation period, threshold rationale, and resulting decision. Do not publish sensitive production values merely to demonstrate that a review occurred.

## Review and improve cycle

Use a plain, repeatable review cycle for each material workload:

1. **Observe:** Review usage, cost drivers, successful outputs, failures, freshness, quality, and public use.
2. **Assess:** Identify unexpected growth, idle capacity, duplicate processing, excessive retention, or work that produces no new evidence.
3. **Decide:** Continue, optimize, redesign, pause, or retire the workload.
4. **Change:** Apply one bounded change with testing, approval, failure behaviour, and rollback defined.
5. **Record:** Update the workload card with the reason, expected benefit, observed result, and next review point.

Automation may alert, recommend, or apply pre-approved low-risk controls. It should not make unbounded financial, publication, or retirement decisions.

Teams that already use MAPE-K may map this cycle to Monitor, Analyze, Plan, Execute, and shared Knowledge. MAPE-K is optional; the required outcome is a documented and repeatable cost decision process.

## Public and private boundaries

The public framework may disclose principles, cost categories, decision criteria, workload classes, and reusable templates.

It must not disclose credentials, account identifiers, private endpoints, exact traffic volumes, detailed schedules, security configurations, provider tokens, private invoices, or production resource identifiers.

## Framework alignment

This component is informed by the [FinOps Framework](https://www.finops.org/framework/) concepts of value-based technology decisions, usage accountability, planning, and usage optimization. It does not represent formal FinOps adoption or certification.

See the [fictional cost-governance example](../examples/fictional-cost-governance-example.md) for an end-to-end application and the [workload cost card](../templates/workload-cost-card.md) for a reusable record.

