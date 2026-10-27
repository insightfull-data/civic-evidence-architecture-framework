# Publication Gates

Publication is a governance decision, not the automatic result of a successful calculation.

## Maturity path

```mermaid
flowchart LR
    Q[Question defined] --> S[Source connected]
    S --> M[Method prototyped]
    M --> D[Data quality assessed]
    D --> L[Private experiment]
    L --> I[Interpretation reviewed]
    I --> P[Public and monitored]
```

## Gate 1: Civic purpose

- The question is understandable without internal terminology.
- The audience and intended decision or understanding are defined.
- The output adds value beyond listing available data.

## Gate 2: Evidence

- Required sources are available and permitted for the intended use.
- Evidence classes and quality thresholds are defined.
- Coverage supports the claim.
- Missing data cannot be mistaken for zero.

## Gate 3: Method

- The method is documented and versioned.
- Assumptions are explicit.
- The result can be reproduced from retained evidence.
- Sensitivity or validation is proportionate to the risk.

## Gate 4: Interpretation

- The result does not imply unsupported causality or individual behavior.
- Public wording states what the evidence can and cannot establish.
- Contextual data is not presented as proof.

## Gate 5: Privacy, security, and accessibility

- Geography and grouping protect individuals and households.
- Secrets and protected operational detail remain private.
- Failure states are understandable.
- Mobile and accessibility behavior has been reviewed.

## Gate 6: Operations

- Refresh, monitoring, cost, retention, and ownership are defined.
- The workload can degrade safely.
- A pause, rollback, and retirement path exists.

## Publication decision

Record one of four decisions:

- **Publish:** all required gates are met.
- **Revise:** value is credible but a defined gap remains.
- **Keep private:** useful for research but not ready for public interpretation.
- **Retire:** value no longer justifies risk, cost, or maintenance.
