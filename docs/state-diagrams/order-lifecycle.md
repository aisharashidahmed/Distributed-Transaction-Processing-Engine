```mermaid 
stateDiagram-v2
    [*] --> AWAITING_FUNDING

    AWAITING_FUNDING --> FUNDS_RESERVED: User allocates cash
    AWAITING_FUNDING --> CANCELLED: User cancels

    FUNDS_RESERVED --> FUNDS_RESERVED: User edits and reservation updates
    FUNDS_RESERVED --> AWAITING_FUNDING: Reservation released
    FUNDS_RESERVED --> READY_TO_SUBMIT: Validation succeeds
    FUNDS_RESERVED --> CANCELLED: User cancels / release funds

    READY_TO_SUBMIT --> SUBMISSION_PENDING: Submit using unique order ID
    READY_TO_SUBMIT --> FUNDS_RESERVED: Market closed or broker unavailable
    READY_TO_SUBMIT --> CANCELLED: User cancels before submission

    SUBMISSION_PENDING --> ACCEPTED: Broker accepts
    SUBMISSION_PENDING --> REJECTED: Broker rejects
    SUBMISSION_PENDING --> SUBMISSION_PENDING: Query unknown submission result

    ACCEPTED --> PARTIALLY_FILLED: Partial execution
    ACCEPTED --> EXECUTED: Full execution
    ACCEPTED --> CANCELLATION_PENDING: User requests cancellation
    ACCEPTED --> REJECTED: Broker invalidates accepted order

    PARTIALLY_FILLED --> PARTIALLY_FILLED: Additional partial execution
    PARTIALLY_FILLED --> EXECUTED: Remaining quantity filled
    PARTIALLY_FILLED --> CANCELLATION_PENDING: Cancel unfilled remainder

    CANCELLATION_PENDING --> CANCELLED: Broker confirms cancellation
    CANCELLATION_PENDING --> PARTIALLY_FILLED: More shares execute first
    CANCELLATION_PENDING --> EXECUTED: Entire remainder executes first

    EXECUTED --> SETTLEMENT_PENDING: Execution confirmed
    SETTLEMENT_PENDING --> SETTLED: Settlement completed

    CANCELLED --> [*]
    REJECTED --> [*]
    SETTLED --> [*]
```
- An order must never be submitted without sufficient reserved funds.
- The same reservation cannot fund multiple orders.
- Editing an order must atomically update both the order and its reservation.
- Repeated submission of the same order must not create duplicate broker orders.
- A submitted cancellation is a request until the broker confirms it.
- A partially filled order may cancel only its unfilled quantity.
- Every execution must be permanently recorded.
- Orders are never deleted, including rejected and cancelled orders.
- Temporary market or broker unavailability must not be represented as order rejection. 