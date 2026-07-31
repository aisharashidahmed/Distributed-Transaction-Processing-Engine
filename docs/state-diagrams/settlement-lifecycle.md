```mermaid
stateDiagram-v2
    [*] --> PENDING

    PENDING --> PROCESSING: Settlement started

    PROCESSING --> PARTIALLY_SETTLED: Portion settled
    PROCESSING --> SETTLED: Entire execution settled
    PROCESSING --> UNKNOWN: Provider timeout / unknown outcome
    PROCESSING --> FAILED: Permanent failure

    PARTIALLY_SETTLED --> PARTIALLY_SETTLED: Additional settlement
    PARTIALLY_SETTLED --> SETTLED: Remaining amount settled
    PARTIALLY_SETTLED --> UNKNOWN: Settlement status uncertain

    UNKNOWN --> PROCESSING: Retry / reconciliation
    UNKNOWN --> SETTLED: Settlement confirmed
    UNKNOWN --> FAILED: Failure confirmed

    FAILED --> PROCESSING: Retry settlement

    SETTLED --> [*]
```
Invariants
- A settlement belongs to exactly one execution.
- An execution may have multiple settlement records.
- Settled amount can never exceed the executed amount.
- Once an amount is settled, it can never become unsettled.
- Every successful settlement must produce immutable ledger entries.
- Settlement retries must be idempotent.
- Completed settlement records are never deleted.