
# Migration: Monolith → Microservices


Migration should be **incremental**, using the *Strangler Pattern*.

## ASCII Diagram
```
Client
  │
  ▼
API Gateway
  │
  ├── Monolith (legacy)
  └── New Microservice(s)
```

## Key Steps
1. Analyze monolith & define bounded contexts  
2. Introduce API Gateway  
3. Extract features gradually  
4. Split database (per service)  
5. Add async communication for decoupling  
6. Implement observability (logs, metrics, tracing)  
7. Decommission old monolith modules
