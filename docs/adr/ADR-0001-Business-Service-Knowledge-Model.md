# ADR-0001 — Business Service Knowledge Model

| Field             | Value                                                                                      |
| ----------------- | ------------------------------------------------------------------------------------------ |
| ADR ID            | ADR-0001                                                                                   |
| Title             | Business Service Knowledge Model                                                           |
| Status            | Accepted                                                                                   |
| Date              | June 2026                                                                                  |
| Author            | Ken Parsons                                                                                |
| Related Service   | Ecosystem-wide                                                                             |
| Related Documents | MANIFESTO.md, docs/0-Operations-Ecosystem-Model.md, templates/Service-Document-Template.md |

---

# 1. Context

The Schoolyard technology environment has grown to include multiple business-critical services, including the Purchase Order System, mobile applications, backend services, WordPress / WooCommerce sites, email, Microsoft 365, backup infrastructure, remote access and development environments.

These services are supported by different technologies, providers, platforms and operational processes.

Traditional IT documentation often describes technical assets such as servers, applications, repositories or infrastructure components. This creates a gap between the business understanding of a service and the technical implementation behind it.

For example, a business owner may understand that the company has email, mobile apps or an online ordering system, but may not know where those services are hosted, who provides them, what they depend on, how they are backed up, or how they could be recovered.

The Operations Ecosystem requires a model that connects business purpose, operational use, service geography and engineering detail without fragmenting the knowledge across separate documents.

---

# 2. Decision

The Schoolyard Operations Ecosystem shall be structured around **Business Services** rather than servers, applications, repositories or technical assets.

Each Business Service shall have a single source of truth presented through multiple audience-specific views.

The core model is:

> One Service.  
> One Source of Truth.  
> Multiple Views.  
> One Shared Understanding.

The standard views for a Business Service are:

1. Service Identity
    
2. Executive View
    
3. Service Geography View
    
4. Operational View
    
5. Engineering View
    
6. Architecture and Decision View
    
7. Recovery and Continuity View
    
8. Evolution View
    

---

# 3. Reasoning

A Business Service is the most useful object around which to organise operational knowledge because it reflects how the organisation actually experiences technology.

The business does not think in terms of servers, databases, APIs or repositories.

The business thinks in terms of capabilities.

Examples include:

- Parents can place orders.
    
- Staff can process customer orders.
    
- Purchase orders can be created and sent to suppliers.
    
- Company email can be used for communication.
    
- Office applications are available to staff.
    
- Business systems are backed up and recoverable.
    

By organising knowledge around services, the ecosystem remains understandable to business owners while still preserving the technical depth needed by engineers.

This model avoids duplicated documentation by allowing different audiences to view the same underlying service knowledge from different perspectives.

The Executive View supports business understanding.

The Service Geography View explains where the service lives and what it depends on.

The Operational View explains how the service supports daily work.

The Engineering View explains how the service is built and maintained.

The Architecture and Decision View preserves why key decisions were made.

The Recovery and Continuity View explains how the service can be restored.

The Evolution View records how the service may change over time.

---

# 4. Alternatives Considered

|Alternative|Reason Not Selected|
|---|---|
|Server-based documentation|Useful for engineers but does not explain business purpose or service value|
|Application-based documentation|Risks separating one business service across multiple documents where several applications are involved|
|Repository-based documentation|Too technical for business users and does not capture service ownership, geography or recovery|
|Traditional operations manual|Often becomes a static document rather than a living model|
|Separate business and technical documents|Creates duplication and increases the risk that documents become inconsistent over time|

---

# 5. Consequences

## Positive Consequences

- Business owners can understand the services that support the business.
    
- Engineers can still access full technical detail.
    
- Knowledge is not duplicated across multiple documents.
    
- Each service has one source of truth.
    
- Service dependencies become visible.
    
- Recovery and continuity information is connected directly to business services.
    
- Future handover is improved because the service is explained from business, operational and engineering perspectives.
    
- The model can be reused for future projects.
    

## Negative Consequences / Trade-offs

- Each service document requires more thought than a simple technical note.
    
- The model depends on discipline and consistency.
    
- Some services may initially be difficult to define because they cross several platforms or providers.
    
- The model may need refinement as real services are documented.
    

---

# 6. Impacted Services

|Service|Impact|
|---|---|
|Ecosystem-wide|All future documents shall use the Business Service Knowledge Model|
|Purchase Order Service|Will be documented as a Business Service rather than only as an application|
|Mobile Ordering Service|Will connect app stores, source code, BFF, WordPress, WooCommerce and payments into one service view|
|Company Email Service|Will explain the distinction between email hosting, domain hosting and email client software|
|Backup and Recovery Service|Will be documented as a business continuity service rather than only as scripts and storage locations|

---

# 7. Review Criteria

This decision should be reviewed if:

- The model becomes too complex to maintain.
    
- Business owners cannot understand the first sections of service documents.
    
- Engineers cannot find the information required to support or recover services.
    
- Service documents become fragmented or duplicated.
    
- The repository evolves into a web-based application.
    
- The model is reused for another organisation or commercial project.
    

---

# 8. Status History

|Date|Status|Notes|
|---|---|---|
|March 2026|Accepted|Initial decision defining the Business Service Knowledge Model|