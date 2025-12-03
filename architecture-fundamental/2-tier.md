
# Two‑Tier Architecture


Two-tier architecture is a simple client–server model where the client communicates **directly** with the database layer.

## ASCII Diagram
```
┌────────────┐
│   Client   │
└─────┬──────┘
      │  SQL Queries
┌─────▼──────┐
│  Database  │
└────────────┘
```

## Explanation
- Business logic often resides on the client.
- Suitable for desktop applications and small internal tools.
- Fast communication, but weak in scalability and security.

## Pros
- Very simple to build
- Low infrastructure cost
- Low latency between client and database

## Cons
- Cannot scale for many users
- Business logic tied to client
- Security risks (direct DB exposure)
