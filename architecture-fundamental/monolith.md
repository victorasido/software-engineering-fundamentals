
# Monolithic Architecture


The entire application lives inside **one codebase** and **one deployment unit**.

## ASCII Diagram
```
┌────────────────────────────────────────────┐
│ UI + Business Logic + Data Access + Config │
└───────────────┬────────────────────────────┘
                │
          ┌─────▼─────┐
          │ Database  │
          └───────────┘
```

## Explanation
- Simple to build at early stages.
- Easy to debug because everything is in one place.
- Becomes difficult to scale and maintain as it grows.

## Pros
- Fast development for small teams
- Single deployment pipeline
- No internal network latency

## Cons
- Hard to scale specific features
- Risky deployment (one crash → whole system down)
