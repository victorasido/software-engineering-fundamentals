
# Three‑Tier Architecture


The system is separated into **Presentation**, **Application**, and **Database** layers.

## ASCII Diagram
```
┌──────────────┐
│ Presentation │  (UI)
└──────┬───────┘
       │ HTTP
┌──────▼───────┐
│ Application  │  (Backend API)
└──────┬───────┘
       │ SQL
┌──────▼───────┐
│   Database   │
└──────────────┘
```

## Explanation
- Very common for web and mobile apps.
- Provides separation of concerns.
- Easier to maintain and scale than 2‑tier.

## Pros
- Good maintainability
- Secure DB access (backend-controlled)
- Scales reasonably well

## Cons
- Backend may become a bottleneck
