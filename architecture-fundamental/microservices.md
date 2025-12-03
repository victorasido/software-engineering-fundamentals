
# Microservices Architecture


Application is split into small, independent services that communicate over HTTP/gRPC or message brokers.

## ASCII Diagram
```
┌────────────┐   ┌────────────┐   ┌──────────────┐
│ Auth Svc   │   │ User Svc   │   │ Payment Svc  │
└─────┬──────┘   └─────┬──────┘   └──────┬───────┘
      │                │                │
      └─────API Gateway / Mesh──────────┘
                   │
        DB per Service / Broker
```

## Explanation
- Enables independent scaling and deployment.
- Ideal for large engineering teams and high‑scale systems.

## Pros
- Fault isolation
- Independent scaling & deployment
- Technology flexibility per service

## Cons
- Very high operational complexity
- Requires monitoring, tracing, service discovery
