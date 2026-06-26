# Document 00 – Operations Ecosystem Model

| Field          | Value                      |
| -------------- | -------------------------- |
| Document ID    | SOE-00                     |
| Title          | Operations Ecosystem Model |
| Version        | 1.0                        |
| Status         | Draft                      |
| Author         | Ken Parsons                |
| Owner          | Schoolyard Ltd             |
| Last Updated   | June 2026                  |
| Classification | Internal                   |

---

# 1. Purpose

This document defines the operating model used by the Schoolyard Operations Ecosystem.

The purpose of the model is to ensure that every business service is documented in a consistent, understandable and reusable way.

The ecosystem is not structured around servers, applications, code repositories or technical assets.

It is structured around **Business Services**.

A Business Service represents a capability that supports the organisation.

Examples include:

- Customer Ordering
    
- Purchase Order Management
    
- Mobile App Ordering
    
- Company Email
    
- Microsoft 365 Office Applications
    
- Website Hosting
    
- Backups
    
- Payments
    
- Remote Access
    
- Development Environments
    

Each Business Service is documented once and then presented through multiple views for different audiences.

This ensures that knowledge is not fragmented across separate documents.

---

# 2. Core Model

The Schoolyard Operations Ecosystem is based on the following principle:

> One Service.  
> One Source of Truth.  
> Multiple Views.  
> One Shared Understanding.

Each service document describes a single business service.

Different audiences may need different levels of detail, but they should all be looking at the same underlying service knowledge.

The business owner should be able to understand why the service exists and where it lives.

The operational user should be able to understand how the service supports daily work.

The engineer should be able to understand how the service is built, maintained, backed up and recovered.

All of this should exist within the same service document.

---

# 3. Why the Model Exists

Traditional IT documentation often separates business information from technical information.

This creates several problems:

- Business owners cannot easily understand the systems that support their organisation.
    
- Technical staff may understand how a system works but not why it exists.
    
- Knowledge becomes fragmented across documents, diagrams, support notes and individual memory.
    
- Documents become inconsistent over time.
    
- Future support becomes harder because the reasoning behind decisions is lost.
    

The Operations Ecosystem Model is designed to solve this by connecting business purpose, service geography, operational workflow and engineering detail inside a single structured service document.

The model exists to make business technology understandable, recoverable and transferable.

---

# 4. Business Service as the Primary Object

The primary object in the ecosystem is the **Business Service**.

A Business Service is any technology-enabled capability that helps the business operate.

A service may be supported by many technical components.

For example, the Mobile Ordering Service may involve:

- Apple App Store
    
- Google Play
    
- Mobile application source code
    
- DigitalOcean BFF server
    
- WordPress / WooCommerce
    
- Worldpay
    
- Email notifications
    
- Backups
    
- Monitoring
    

The business does not experience these as separate technical objects.

The business experiences them as one service:

> Parents can order school uniform using a mobile application.

Therefore the ecosystem documents the service first, and the technical components second.

---

# 5. The View-Based Model

Every Business Service shall be documented through a consistent set of views.

A view is not a separate document.

A view is a different way of looking at the same service.

This avoids duplication while allowing different audiences to access the level of knowledge relevant to them.

The standard views are:

1. Service Identity
    
2. Executive View
    
3. Service Geography View
    
4. Operational View
    
5. Engineering View
    
6. Architecture and Decision View
    
7. Recovery and Continuity View
    
8. Evolution View
    

Not every service will require the same level of technical depth, but the structure should remain consistent wherever practical.

---

# 6. View 1 — Service Identity

## Purpose

The Service Identity view gives the reader immediate understanding of what the service is, who owns it, where it lives and how important it is.

This view should be understandable within 30 seconds.

## Audience

- Business Owner
    
- Directors
    
- Managers
    
- Engineers
    
- Suppliers
    
- Auditors
    
- Future support staff
    

## Standard Fields

|Field|Description|
|---|---|
|Service Name|The name of the business service|
|Service Type|Business, operational, technical, infrastructure or support service|
|Business Owner|The organisation or person accountable for the service|
|Technical Custodian|The person or organisation responsible for technical maintenance|
|Primary Users|People who use or depend on the service|
|Business Criticality|Critical, High, Medium or Low|
|Data Owner|The organisation that owns the business data|
|Primary Location|Where the service is primarily hosted or administered|
|Main Provider|Main external provider, supplier or platform|
|Backup Location|Where backups are held|
|Off-site Backup|Whether an off-site backup exists|
|Recovery Target|Expected recovery timescale|
|Related Services|Other services this service depends on or supports|
|Last Reviewed|Date the service document was last reviewed|

## Principle

A business owner should not have to read beyond this section to identify what the service is and where it lives.

---

# 7. View 2 — Executive View

## Purpose

The Executive View explains why the service exists and what value it provides to the business.

It must be written in plain business language.

## Audience

- Business Owner
    
- Directors
    
- Senior Managers
    
- Non-technical stakeholders
    

## Questions Answered

- What is this service?
    
- Why does the business use it?
    
- What problem does it solve?
    
- Who benefits from it?
    
- What would happen if it was unavailable?
    
- How important is it to the business?
    

## Required Sections

- Business Purpose
    
- Business Value
    
- Primary Users
    
- Business Impact if Unavailable
    
- Ownership
    
- Key Dependencies
    
- Summary Risk Level
    

## Principle

The Executive View should not require technical knowledge.

Its purpose is to create understanding, not explain implementation.

---

# 8. View 3 — Service Geography View

## Purpose

The Service Geography View explains where the service lives.

This is one of the most important views in the Operations Ecosystem.

Many business owners know that they have email, websites, mobile apps or office systems, but they may not know where those services are actually hosted, who provides them, who administers them, or what other services they depend on.

The Service Geography View answers those questions.

## Audience

- Business Owner
    
- Directors
    
- Managers
    
- Suppliers
    
- Auditors
    
- Insurance providers
    
- New IT providers
    
- Engineers
    

## Questions Answered

- Where is this service hosted?
    
- Who provides the service?
    
- Who owns the data?
    
- Who administers the service?
    
- Which external platforms are involved?
    
- Which other systems does this service depend on?
    
- Where is the source code held, if applicable?
    
- Where are backups stored?
    

## Example

Company Email may be experienced through Microsoft Outlook, but the mailboxes and domain services may be hosted by 20i.

Mobile Apps may be downloaded from the Apple App Store and Google Play, but they may depend on a backend server hosted with DigitalOcean, WordPress data, Worldpay payments and source code held by KJP Technologies.

The Service Geography View makes these relationships visible.

## Principle

The Service Geography View should make the physical, supplier and platform location of a service immediately understandable.

---

# 9. View 4 — Operational View

## Purpose

The Operational View explains how the service works in normal business use.

It describes the flow of information, people, actions and outcomes.

This view should still be understandable to a non-technical person wherever possible.

## Audience

- Operations Managers
    
- Department Managers
    
- Support Staff
    
- Technical Managers
    
- Business users
    
- Engineers
    

## Questions Answered

- How is the service used day to day?
    
- Who uses it?
    
- What are the main workflows?
    
- What information enters the service?
    
- What information leaves the service?
    
- What does normal operation look like?
    
- What are the common support issues?
    
- What should staff do if something appears wrong?
    

## Recommended Content

- Simple process flow
    
- Main business workflow
    
- User roles
    
- Inputs and outputs
    
- Normal operating procedure
    
- Escalation path
    
- Common issues
    
- Linked support procedures
    

## Principle

The Operational View explains how the service supports the business without exposing unnecessary technical complexity.

---

# 10. View 5 — Engineering View

## Purpose

The Engineering View provides the technical information required to maintain, support, deploy, secure and recover the service.

This is the full technical layer of the service document.

## Audience

- Developers
    
- System Administrators
    
- Future Engineers
    
- Technical Support
    
- Infrastructure Engineers
    

## Questions Answered

- How is the service implemented?
    
- Which technologies are used?
    
- Where is the source code?
    
- Where is it deployed?
    
- How is it configured?
    
- How is it secured?
    
- How is it backed up?
    
- How is it monitored?
    
- How is it restored?
    
- What are the known risks or technical constraints?
    

## Recommended Content

- Technology stack
    
- Server details
    
- Hosting details
    
- Repository links
    
- Deployment process
    
- Environment variables
    
- Database details
    
- Network ports
    
- Certificates
    
- DNS
    
- Authentication
    
- Backup scripts
    
- Monitoring
    
- Logs
    
- Maintenance procedures
    
- Known technical issues
    

## Principle

Technical depth belongs here, not in the Executive or Service Geography views.

---

# 11. View 6 — Architecture and Decision View

## Purpose

The Architecture and Decision View explains why the service was built in its current form.

It links the service to relevant Architecture Decision Records.

This prevents future engineers from seeing only the implementation without understanding the reasoning behind it.

## Audience

- Engineers
    
- Architects
    
- Technical Custodians
    
- Future Developers
    
- Project Owners
    

## Questions Answered

- Why was this architecture chosen?
    
- What alternatives were considered?
    
- What constraints influenced the design?
    
- Which decisions are permanent?
    
- Which decisions may be revisited?
    
- Which ADRs apply to this service?
    

## Recommended Content

- Architecture summary
    
- Key design decisions
    
- ADR references
    
- Alternatives considered
    
- Constraints
    
- Trade-offs
    
- Consequences
    
- Future considerations
    

## Principle

A future engineer should be able to understand not only what was built, but why it was built that way.

---

# 12. View 7 — Recovery and Continuity View

## Purpose

The Recovery and Continuity View explains how the service can be restored or continued after failure.

This view connects business risk with technical recovery.

## Audience

- Business Owner
    
- Operations Managers
    
- Engineers
    
- Disaster Recovery Staff
    
- External IT Support
    

## Questions Answered

- What happens if the service fails?
    
- How quickly should it be restored?
    
- Where are the backups?
    
- How are backups verified?
    
- Who performs recovery?
    
- What are the restore steps?
    
- What dependencies must be restored first?
    
- Has recovery been tested?
    

## Recommended Content

- Recovery target
    
- Backup locations
    
- Backup frequency
    
- Off-site backup status
    
- Restore procedure
    
- Dependencies
    
- Verification process
    
- Last successful backup
    
- Last restore test
    
- Business continuity workaround
    

## Principle

A backup is not complete unless the business understands what is protected and an engineer can restore it.

---

# 13. View 8 — Evolution View

## Purpose

The Evolution View records how the service may change over time.

It prevents future improvements, known limitations and planned changes from being lost.

## Audience

- Business Owner
    
- Technical Custodian
    
- Future Engineers
    
- Project Managers
    

## Questions Answered

- What improvements are planned?
    
- What limitations are known?
    
- What technical debt exists?
    
- What business changes may affect the service?
    
- What should be reviewed in future?
    
- What opportunities exist for simplification?
    

## Recommended Content

- Planned improvements
    
- Known limitations
    
- Technical debt
    
- Future risks
    
- Review notes
    
- Enhancement ideas
    
- Related roadmap items
    

## Principle

The Operations Ecosystem is living knowledge. It should record not only what exists today, but how the service may evolve tomorrow.

---

# 14. Service Relationships

Each service may relate to other services.

These relationships should be made visible.

Common relationship types include:

|Relationship|Meaning|
|---|---|
|Depends On|This service requires another service to function|
|Provides To|This service supports another business service|
|Hosted By|The service is hosted by a platform or provider|
|Administered By|The service is managed by a person or organisation|
|Backed Up By|The service is protected by another backup service|
|Secured By|The service depends on a security or identity service|
|Paid Through|The service relies on a payment or billing provider|
|Distributed Through|The service is made available through another platform|
|Developed By|The service is built or maintained by a developer|
|Owned By|The business owns the data, process or responsibility|

These relationships allow the ecosystem to answer practical business questions, such as:

- What services depend on 20i?
    
- What services depend on DigitalOcean?
    
- What services would be affected if Microsoft 365 was unavailable?
    
- Which services are backed up to the UGREEN NAS?
    
- Which services have off-site backup protection?
    
- Which services depend on KJP Technologies for development?
    

---

# 15. Progressive Disclosure

The ecosystem uses progressive disclosure.

This means each document starts with simple, high-value business information and gradually moves toward deeper technical information.

The reader chooses how far they need to go.

A business owner may only need the Service Identity, Executive View and Service Geography View.

An operations manager may also need the Operational View.

An engineer may need all views.

This avoids forcing non-technical readers into technical detail while still preserving the full engineering knowledge required for support and recovery.

---

# 16. Visual Maps

Visual maps are encouraged throughout the ecosystem.

They should be simple, clear and audience-specific.

## Business-Level Map

Shows the service in plain language.

Example:

Customer places order  
↓  
Order is processed  
↓  
Supplier purchase order is created  
↓  
Goods are received  
↓  
Customer receives order

## Service Geography Map

Shows where the service lives.

Example:

Parent mobile phone  
↓  
Apple App Store / Google Play  
↓  
Schoolyard Mobile App  
↓  
DigitalOcean BFF Server  
↓  
WordPress / WooCommerce  
↓  
Worldpay  
↓  
Schoolyard

## Engineering Map

Shows the technical implementation.

Example:

Expo React Native App  
↓  
Next.js BFF API  
↓  
WooCommerce REST API  
↓  
Worldpay Hosted Payment Pages  
↓  
Webhook Processor  
↓  
WooCommerce Order Status

## Principle

Maps should reduce complexity, not decorate it.

A map is useful only if it helps the reader understand the service more quickly.

---

# 17. ADR Integration

Architecture Decision Records are used to preserve the reasoning behind important decisions.

A service document should reference relevant ADRs where decisions have shaped the service.

Examples:

- Why Ubuntu Server was selected
    
- Why Docker was used
    
- Why the mobile apps use a BFF server
    
- Why backups are copied to NAS and Backblaze
    
- Why source code is version controlled in GitHub
    
- Why services are documented using the view-based model
    

ADRs should be short, dated and decision-focused.

They should explain:

- Context
    
- Decision
    
- Alternatives considered
    
- Consequences
    
- Status
    

---

# 18. Documentation Standards

Every service document should follow these rules:

1. Start with the Service Identity.
    
2. Explain business purpose before technical implementation.
    
3. Include Service Geography.
    
4. Use plain language wherever possible.
    
5. Introduce technical detail only when useful.
    
6. Avoid duplicating service knowledge across separate documents.
    
7. Use links rather than copying the same information repeatedly.
    
8. Reference ADRs for major decisions.
    
9. Include recovery information for critical services.
    
10. Review documents regularly.
    

The aim is not to create more documentation.

The aim is to create better understanding.

---

# 19. Service Document Template

Every service document should follow this structure:

```markdown
# Service Name

## Service Identity

## Executive View

## Service Geography View

## Operational View

## Engineering View

## Architecture and Decision View

## Recovery and Continuity View

## Evolution View

## Related Documents

## Revision History
```

Where a view is not applicable, it may be marked as:

> Not applicable for this service.

The heading should remain in place to preserve consistency.

---

# 20. Model Validation

The Operations Ecosystem Model shall be validated through real services.

The first implementation of the model is the Schoolyard Operations Ecosystem.

The model will be refined as services are documented and reviewed.

If a section does not help the reader understand, operate, recover or evolve a service, it should be simplified or removed.

If a recurring need appears across multiple services, the model should be updated.

The model is expected to evolve.

Its purpose is not to create rigid bureaucracy.

Its purpose is to preserve useful operational knowledge.

---

# 21. Commercial and Future Potential

Although the Schoolyard Operations Ecosystem is being created first for internal operational use, the underlying model may have wider value.

The model may become reusable for future projects where technology services need to be handed over with clear business, operational and engineering understanding.

A completed technology project should not consist only of source code and deployment notes.

A completed project should include an Operational Knowledge Model that explains:

- Why the service exists
    
- Where the service lives
    
- How it supports the business
    
- How it operates
    
- How it is built
    
- How it is recovered
    
- Why key decisions were made
    
- How it may evolve
    

This principle may be applied to future applications, client systems and business technology projects.

However, the immediate purpose of this repository is model validation through real operational use.

Software or commercial product development should only be considered after the model has been proven useful in practice.

---

# 22. Foundational Principle

The Operations Ecosystem Model exists to reduce complexity.

Technology may be complex.

The model must not be.

Every document should help the reader understand the business service more clearly than they did before reading it.

If a document makes the service harder to understand, the document has failed.

The final test of the model is simple:

> Can a business owner understand the service?  
> Can an operations person use the service?  
> Can an engineer support and recover the service?  
> Can a future developer evolve the service?

If the answer is yes, the model is working.