# Usage-Aware Architecture Efficiency

Efficiency is the disciplined matching of compute, storage, freshness, and maintenance to evidence value.

## Objective

> Produce credible evidence with the least infrastructure necessary to support the civic question.

## Principles

### Static first

Deliver stable content, reference data, documentation, and prepared geography through static files and content delivery networks.

### Match cadence to change

Do not refresh every source at the fastest available interval. Match collection frequency to source change, public need, and validation value.

### Prepare once, reuse many times

Retrieve, validate, normalize, calculate, store, and reuse shared evidence. Public traffic should not multiply expensive upstream requests or geospatial work.

### Bound retention

Retain high-frequency evidence only for a defined analytical or accountability purpose. Prefer aggregates when detailed records are no longer needed.

### Assign narrow provider responsibilities

Use static delivery, serverless execution, relational storage, and persistent services according to workload characteristics. Do not introduce persistent infrastructure without a duration, state, or reliability requirement.

### Degrade honestly

Preserve last valid evidence where appropriate, show source time, distinguish stale from current, and never interpret missing as empty.

### Observe cost by workload

Separate provider-reported charges from estimates. Attribute recurring work to major features so civic value can be compared with operating burden.

### Apply a value gate

Before making a workload permanent, ask:

1. What civic question does it answer?
2. Who uses the result?
3. Does it need to be live?
4. Can it be prepared, cached, aggregated, or reused?
5. What volume of executions, reads, writes, and external requests will it create?
6. What happens when it fails?
7. How much history is required?
8. Can it be paused without harming the public product?
9. Is the value proportionate to compute, storage, and maintenance?

Reduce, redesign, pause, or retire work when the answer is no.

Use the [Cost and Capacity Governance](cost-and-capacity-governance.md) chapter and [workload cost card](../templates/workload-cost-card.md) to turn these principles into a repeatable operating decision.
