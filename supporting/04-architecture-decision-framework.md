# Architecture Decision Framework

A reference guide for the Architecture Agent to make and document technical decisions.

---

## Architecture Decision Record (ADR) Template

```markdown
### Decision: [Title]

**Status:** Proposed | Accepted | Deprecated | Superseded

**Context:**
[What is the issue that we're seeing that is motivating this decision?]

**Decision:**
[What is the change that we're proposing and/or doing?]

**Rationale:**
[Why is this the best choice among the alternatives?]

**Consequences:**
- Positive: [Benefits]
- Negative: [Drawbacks/trade-offs]
- Neutral: [Other implications]

**Alternatives Considered:**
1. [Alternative 1] - Rejected because [reason]
2. [Alternative 2] - Rejected because [reason]
```

---

## Architecture Style Decision

### When to Choose What

| Style | Best For | Avoid When |
|-------|----------|------------|
| **Monolith** | Small team, MVP, unclear boundaries | Large team, independent scaling needs |
| **Modular Monolith** | Medium complexity, single deployment | Need independent deployments |
| **Microservices** | Large teams, independent scaling, polyglot | Small team, simple domain |
| **Serverless** | Event-driven, variable load, low ops | Consistent high load, complex state |

### Key Questions
- How big is the team? (< 5 people → lean toward monolith)
- How complex is the domain? (Simple → monolith, Complex → modular)
- What are the scaling requirements? (Uniform → monolith, Variable → services)
- What's the deployment frequency? (Same cadence → monolith, Different → services)

---

## Frontend Architecture Decision

| Approach | Best For | Trade-offs |
|----------|----------|------------|
| **SPA** (React, Vue, Angular) | Rich interactivity, app-like feel | SEO challenges, initial load time |
| **SSR** (Next.js, Nuxt) | SEO important, fast initial load | Server complexity, hosting cost |
| **MPA** (Traditional) | Content-heavy, simple interactions | Page refreshes, less dynamic |
| **Hybrid** (Islands) | Content + some interactivity | Complexity in architecture |

### Key Questions
- Is SEO critical? → Consider SSR
- Is it highly interactive? → Consider SPA
- Is it content-heavy with minimal interaction? → Consider MPA
- What's the team's expertise?

---

## API Style Decision

| Style | Best For | Trade-offs |
|-------|----------|------------|
| **REST** | CRUD operations, caching, simplicity | Over/under-fetching, versioning |
| **GraphQL** | Complex data needs, multiple clients | Complexity, caching challenges |
| **gRPC** | Internal services, high performance | Browser support, learning curve |
| **WebSocket** | Real-time, bidirectional | Connection management, scaling |

### Key Questions
- How complex are data requirements? → Complex = GraphQL
- Is it internal or external API? → Internal = gRPC option
- Need real-time updates? → WebSocket
- Team familiarity?

---

## Database Decision

### Database Types

| Type | Examples | Best For |
|------|----------|----------|
| **Relational** | PostgreSQL, MySQL | Structured data, ACID, complex queries |
| **Document** | MongoDB, Firestore | Flexible schema, nested data |
| **Key-Value** | Redis, DynamoDB | Caching, sessions, simple lookups |
| **Graph** | Neo4j, Neptune | Relationships, social networks |
| **Time-Series** | InfluxDB, TimescaleDB | Metrics, logs, IoT data |

### Decision Factors
- Data structure: Highly relational → SQL, Flexible → Document
- Query patterns: Complex joins → SQL, Simple lookups → NoSQL
- Scale requirements: Read-heavy → consider caching layer
- Consistency needs: Strong → SQL, Eventual OK → NoSQL options

---

## Tech Stack Evaluation Matrix

Rate each option 1-5:

| Criteria | Option A | Option B | Option C |
|----------|----------|----------|----------|
| Team expertise | | | |
| Community/ecosystem | | | |
| Performance | | | |
| Scalability | | | |
| Maintainability | | | |
| Cost | | | |
| Time to market | | | |
| **Total** | | | |

---

## Data Model Design Checklist

### Entity Design
- [ ] Primary key defined (prefer UUID for distributed systems)
- [ ] Required vs optional fields identified
- [ ] Data types appropriate for the data
- [ ] Constraints defined (unique, not null, etc.)
- [ ] Indexes planned for query patterns

### Relationship Design
- [ ] Cardinality defined (1:1, 1:N, N:M)
- [ ] Foreign keys identified
- [ ] Cascade behavior defined (delete, update)
- [ ] Junction tables for N:M relationships

### Data Integrity
- [ ] Validation rules defined
- [ ] Default values set where appropriate
- [ ] Audit fields included (created_at, updated_at)
- [ ] Soft delete vs hard delete decision made

---

## API Design Principles

### RESTful Conventions
```
GET    /resources          → List resources
GET    /resources/:id      → Get single resource
POST   /resources          → Create resource
PUT    /resources/:id      → Update resource (full)
PATCH  /resources/:id      → Update resource (partial)
DELETE /resources/:id      → Delete resource
```

### Naming Conventions
- Use plural nouns: `/users`, `/products`
- Use kebab-case: `/user-profiles`
- Nest for relationships: `/users/:id/orders`
- Use query params for filtering: `/users?status=active`

### Response Structure
```json
{
  "data": { ... },
  "meta": {
    "page": 1,
    "total": 100
  },
  "errors": []
}
```

### Error Response Structure
```json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid input",
    "details": [
      { "field": "email", "message": "Invalid format" }
    ]
  }
}
```

---

## Security Checklist

### Authentication
- [ ] Password hashing (bcrypt, argon2)
- [ ] JWT or session-based auth decision
- [ ] Token expiration and refresh strategy
- [ ] MFA/2FA support (if required)

### Authorization
- [ ] Role-based access control (RBAC)
- [ ] Resource-level permissions
- [ ] API rate limiting
- [ ] CORS configuration

### Data Protection
- [ ] Encryption at rest
- [ ] Encryption in transit (HTTPS)
- [ ] Sensitive data handling (PII)
- [ ] Input validation and sanitization

### Infrastructure
- [ ] Secrets management (not in code)
- [ ] Security headers configured
- [ ] Dependency vulnerability scanning
- [ ] Audit logging

---

## NFR Implementation Patterns

### Performance
| Requirement | Implementation Pattern |
|-------------|----------------------|
| Fast page load | CDN, code splitting, lazy loading |
| Fast API response | Caching, query optimization, indexing |
| Handle high load | Horizontal scaling, load balancing |

### Reliability
| Requirement | Implementation Pattern |
|-------------|----------------------|
| High availability | Multi-AZ deployment, health checks |
| Fault tolerance | Circuit breakers, retry logic, fallbacks |
| Data durability | Backups, replication, point-in-time recovery |

### Scalability
| Requirement | Implementation Pattern |
|-------------|----------------------|
| User growth | Stateless services, auto-scaling |
| Data growth | Sharding, archiving, data lifecycle |
| Geographic | Multi-region, edge computing |

---

## Architecture Quality Checklist

Before finalizing, verify:

### Completeness
- [ ] All major components identified
- [ ] Data flow documented
- [ ] Integration points defined
- [ ] Security considerations addressed
- [ ] NFRs have implementation approach

### Clarity
- [ ] Diagrams are clear and readable
- [ ] Decisions have rationale
- [ ] Trade-offs are documented
- [ ] Technology choices are justified

### Feasibility
- [ ] Team has required skills (or plan to acquire)
- [ ] Technology is mature enough
- [ ] Cost is within budget
- [ ] Timeline is achievable

### Flexibility
- [ ] Design allows for future changes
- [ ] No premature optimization
- [ ] Clear boundaries between components
- [ ] Dependencies are managed
