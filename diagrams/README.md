# Architecture Diagrams

The diagrams use Mermaid so they remain readable, editable, and render directly on GitHub.

## Platform context

```mermaid
flowchart TB
    subgraph Sources[Public and approved sources]
        A[Operational or live data]
        B[Administrative and community data]
        C[Geographic and place data]
        D[Consented product-use data]
    end

    subgraph Evidence[Evidence pipeline]
        E[Acquire and validate]
        F[Normalize and classify]
        G[Store and model]
    end

    subgraph Experiences[Product experiences]
        H[Public product]
        I[Private lab]
        J[Administration]
        K[Sandbox]
    end

    Sources --> E --> F --> G
    G --> H
    G --> I
    G --> J
    G --> K
```

## Trust boundaries

```mermaid
flowchart LR
    PUBLIC[Public product<br/>reviewed evidence]
    PRIVATE[Private lab<br/>experiments and validation]
    ADMIN[Administration<br/>health, cost, and controls]
    SANDBOX[Sandbox<br/>governed testing]

    PUBLIC -. publication gate .-> PRIVATE
    PRIVATE --> ADMIN
    SANDBOX --> ADMIN
```

## Evidence lifecycle

```mermaid
flowchart LR
    Q[Civic question] --> C[Evidence contract]
    C --> A[Acquire]
    A --> V[Validate]
    V --> N[Normalize and classify]
    N --> M[Analyze or model]
    M --> B[Interpretation boundary]
    B --> X[Product experience]
    X --> R[Monitor and review]
    R -. revise .-> C
```

## Bounded agent loop

```mermaid
flowchart LR
    P[Plan] --> O[Observe]
    O --> D[Decide within policy]
    D --> E[Record evidence]
    E --> R[Review]
    R -. next bounded step .-> O

    G[Guardrails:<br/>approved sources<br/>permitted actions<br/>stop conditions<br/>compute limits<br/>retention] --- D
```

## MAPE-K bounded operational loop

```mermaid
flowchart LR
    S[Approved sensors<br/>and data sources] --> M[Monitor]
    M --> A[Analyze]
    A --> P[Plan]
    P --> E[Execute]
    E --> T[Allowlisted tools<br/>and managed process]
    T -. resulting state .-> S

    K[(Governed Knowledge:<br/>evidence and state<br/>policies and limits<br/>versions and audit history)]
    K --- M
    K --- A
    K --- P
    K --- E

    H[Human oversight<br/>approval, pause, rollback] -. constrains .-> P
    H -. constrains .-> E
```

This adapts IBM's Monitor-Analyze-Plan-Execute over shared Knowledge model for bounded agent operation. See the [MAPE-K framework page](../framework/mape-k-operational-loop.md) and [IBM's autonomic-computing documentation](https://www.redbooks.ibm.com/redbooks/pdfs/sg246665.pdf).

## Cost and capacity feedback loop

```mermaid
flowchart LR
    W[Workload and civic purpose] --> M[Monitor usage, cost, quality, and freshness]
    M --> A[Analyze baseline, unit measures, and guardrails]
    A --> P[Plan bounded response]
    P --> E[Execute approved change]
    E --> O[Observe outcome]
    O -. next review .-> M

    K[(Knowledge:<br/>workload card<br/>cost evidence<br/>assumptions<br/>decisions)]
    K --- M
    K --- A
    K --- P
    K --- E

    H[Owner review<br/>continue, optimize,<br/>pause, or retire] -. constrains .-> P
    H -. approves .-> E
```

See [Cost and Capacity Governance](../framework/cost-and-capacity-governance.md) and the [fictional cost-governance example](../examples/fictional-cost-governance-example.md).

## AI governance lifecycle

```mermaid
flowchart LR
    A[Register] --> B[Classify capability and impact]
    B --> C[Map data, tools, people, and harms]
    C --> D[Define controls]
    D --> E[Test and evaluate]
    E --> F{Release decision}
    F -->|Private| G[Controlled experiment]
    F -->|Public| H[Publish with disclosure]
    F -->|Revise| C
    G --> I[Monitor]
    H --> I
    I --> J[Continue, pause, or retire]
```

## Publication maturity

```mermaid
flowchart LR
    Q[Question defined] --> S[Source connected]
    S --> M[Method prototyped]
    M --> D[Quality assessed]
    D --> L[Private experiment]
    L --> I[Interpretation reviewed]
    I --> P[Public and monitored]
```

These diagrams describe conceptual responsibilities. They intentionally exclude product credentials, internal endpoints, production schemas, infrastructure identifiers, and exploitable operational detail.
