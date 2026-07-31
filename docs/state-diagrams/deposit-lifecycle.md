```mermaid
stateDiagram-v2
    [*] --> REQUESTED

    REQUESTED --> WAITING_FOR_PIN: Provider accepts request
    REQUESTED --> FAILED: Provider rejects request

    WAITING_FOR_PIN --> PAYMENT_CONFIRMED: Successful callback
    WAITING_FOR_PIN --> FAILED: Customer timeout
    WAITING_FOR_PIN --> FAILED: Customer cancels
    WAITING_FOR_PIN --> FAILED: Payment declined

    PAYMENT_CONFIRMED --> CREDIT_PENDING: Begin internal credit
    CREDIT_PENDING --> CREDIT_PENDING: Retry after temporary failure
    CREDIT_PENDING --> CREDITED: Ledger credit committed

    CREDITED --> [*]
    FAILED --> [*]
```

    - A deposit may only be credited after a verified successful provider callback.
    - Duplicate callbacks must not create duplicate credits.
    - A confirmed payment must not become failed because of a temporary internal error.
    - CREDIT_PENDING operations must be safely retryable.