# API Gateway vs Backend

API Gateway and Backend serve different roles:

- **API Gateway** → Entry point, routing, filtering, auth  
- **Backend** → Business logic, validation, database operations  

## ASCII Diagram
```
Client
  │
  ▼
┌──────────────────┐
│   API Gateway    │   (routing, auth, rate limit)
└──────────────────┘
      │
      ▼
┌──────────────────┐
│  Backend Service │   (logic, rules, DB operations)
└──────────────────┘
      │
      ▼
┌──────────────────┐
│     Database     │
└──────────────────┘
```

## Responsibilities

### API Gateway:
- Authentication & token validation  
- Rate limiting  
- Routing & aggregation  
- Logging & metrics  
- Cross-service orchestration  

### Backend:
- Business rules  
- Data validation  
- Database transactions  
- Domain logic  

## Comparison Table
| Feature | API Gateway | Backend |
|--------|-------------|---------|
| Role | Entry point | Business processing |
| Security | Auth, throttling | Domain access control |
| Scalability | Very high | Per domain |
| Dependencies | Multiple services | Database or internal services |
