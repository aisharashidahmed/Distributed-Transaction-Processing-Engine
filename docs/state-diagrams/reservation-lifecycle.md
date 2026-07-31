```mermaid 
stateDiagram-v2
    [*] --> AWAITING_FUNDS

    AWAITING_FUNDS --> RESERVED: Funds successfully locked
    AWAITING_FUNDS --> RESERVATION_FAILED: Insufficient funds or reservation error
    AWAITING_FUNDS --> CANCELLED: Order abandoned before funds are locked

    RESERVATION_FAILED --> AWAITING_FUNDS: Retry reservation
    RESERVATION_FAILED --> CANCELLED: Order abandoned

    RESERVED --> RESERVED: Reservation amount updated
    RESERVED --> PARTIALLY_CONSUMED: Partial execution recorded
    RESERVED --> CONSUMED: Full execution recorded
    RESERVED --> RELEASE_PENDING: Cancellation or rejection requires release

    PARTIALLY_CONSUMED --> PARTIALLY_CONSUMED: Additional execution recorded
    PARTIALLY_CONSUMED --> CONSUMED: Remaining quantity fully executed
    PARTIALLY_CONSUMED --> RELEASE_PENDING: Cancel unfilled remainder

    RELEASE_PENDING --> RELEASED: Unused funds returned
    RELEASE_PENDING --> PARTIALLY_CONSUMED: More execution occurs before release
    RELEASE_PENDING --> CONSUMED: Remaining amount executes before release

    CONSUMED --> [*]
    RELEASED --> [*]
    CANCELLED --> [*]

```
Key rules:

- Only one active reservation may exist for an order.
- A reservation belongs to exactly one order.
- Executed value becomes consumed; unexecuted value remains reserved.
- Rejection or confirmed cancellation releases only unused funds.
- Consuming or releasing funds must be idempotent.
- Reservation and balance updates must be atomic.
- Terminal reservations are never reopened or deleted.