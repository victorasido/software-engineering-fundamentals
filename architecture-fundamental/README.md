# Software Architecture Fundamentals

A comprehensive overview of core software architecture patterns, including 2-tier, 3-tier, N-tier, monolithic, and microservices models.  
This documentation provides foundational understanding, diagrams, benefits, drawbacks, and guidance on choosing the right architecture.

---

## What Is Software Architecture?

Software architecture defines the **high-level structure** of a system, including:
- how components are organized,
- how they communicate,
- how responsibilities are separated,
- and how the system evolves over time.

Good architecture improves **scalability, maintainability, reliability, and team productivity**.

---

# Architecture Index

## 1. Two-Tier Architecture  
Basic client–server model where the client communicates directly with the database.
```
Client ↔ Database
```
 [2-tier.md](2-tier.md)

---

## 2. Three-Tier Architecture  
Presentation layer, backend layer, and database layer separated.
```
UI → Backend → Database
```
 [3-tier.md](3-tier.md)

---

## 3. N-Tier Architecture  
Enterprise multi-layer model with gateway, services, domain, and integration layers.
```
UI → Gateway → Services → Domain → Data/Cache
```
 [n-tier.md](n-tier.md)

---

## 4. Monolithic Architecture  
A single unified codebase and deployment unit.
```
[ UI + Logic + Data Access ] → DB
```
 [monolith.md](monolith.md)

---

## 5. Microservices Architecture  
System broken into independently deployable services.
```
Service A │ Service B │ Service C → API Gateway
```
 [microservices.md](microservices.md)

---

## 6. Migration (Monolith → Microservices)  
Gradual extraction approach using Strangler Pattern.

 [migration.md](migration.md)

---

## 7. Architecture Comparison  
Detailed comparison table of all architecture types.

 [comparison.md](comparison.md)

---

# Which Architecture Should I Choose? (Decision Table)

| Scenario | Recommended Architecture | Reason |
|---------|--------------------------|--------|
| Small internal tool | **2-Tier** | Simple, fast, low overhead |
| Standard web/mobile app | **3-Tier** | Clear separation & maintainability |
| Large enterprise system | **N-Tier** | Supports integrations & scaling layers |
| MVP / Startup | **Monolith** | Fast to build and deploy |
| High-scale, multi-team system | **Microservices** | Independent scaling & team autonomy |
| Migrating legacy system | **Microservices (Gradual)** | Strangler pattern modernization |

---

## Resources

### Official Documentation
- [Microsoft Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/)
- [Azure Architecture Styles — N-Tier, Microservices, Event-Driven](https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/)
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)
- [Google Cloud — Architecture Framework](https://cloud.google.com/architecture/framework)
- [RFC 7450 — Software Architecture Terminology](https://www.rfc-editor.org/rfc/rfc7450)  
- [Kubernetes Documentation — Microservices-Oriented Deployment](https://kubernetes.io/docs/home/)

### Additional Learning
- [Martin Fowler — Microservices](https://martinfowler.com/articles/microservices.html)
- [Martin Fowler — Strangler Fig Pattern](https://martinfowler.com/bliki/StranglerFigApplication.html)
- [microservices.io — Architecture Patterns](https://microservices.io/)
- [12-Factor App Methodology](https://12factor.net/)
- [System Design Primer (GitHub)](https://github.com/donnemartin/system-design-primer)
- [Nginx — Reverse Proxy Architecture](https://docs.nginx.com/nginx/admin-guide/load-balancer/reverse-proxy/)
- [Kong — API Gateway & Decoupled Architecture](https://docs.konghq.com/)
- [Cloudflare Learning Center — Load Balancing & Architecture Basics](https://www.cloudflare.com/learning/performance/what-is-load-balancing/)

