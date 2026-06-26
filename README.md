# Schoolyard Operations Ecosystem

The Schoolyard Operations Ecosystem is the authoritative operational knowledge base for the technology services that support Schoolyard Ltd.

This repository is not intended to be a simple collection of technical notes.

It is a structured Business Service Knowledge Model.

Its purpose is to preserve the knowledge required to understand, operate, maintain, recover and evolve the services that support the business.

---

## Core Principle

> One Service.
> One Source of Truth.
> Multiple Views.
> One Shared Understanding.

Each business service is documented once and then presented through different views for different audiences.

A business owner should be able to understand why a service exists and where it lives.

An operations person should be able to understand how the service supports daily work.

An engineer should be able to understand how the service is built, supported, backed up, recovered and evolved.

---

## Why This Exists

Most technology documentation is written for technical staff.

This creates a gap between the systems a business depends upon and the people responsible for the business.

The Schoolyard Operations Ecosystem closes that gap.

It explains technology in a way that is useful to:

* Business owners
* Directors
* Managers
* Operational staff
* Engineers
* External IT providers
* Future support teams

The ecosystem documents not only how systems work, but why they exist, where they live, who owns them, what they depend on and how they can be recovered.

---

## Repository Structure

```text
/
├── MANIFESTO.md
├── README.md
├── INDEX.md
├── docs/
│   ├── 0-Operations-Ecosystem-Model.md
│   ├── 01-Infrastructure-Standards.md
│   ├── 02-Infrastructure-Overview.md
│   ├── 03-Service-Catalogue.md
│   ├── 04-Service-Geography.md
│   ├── 05-Backup-Architecture.md
│   ├── 06-Recovery-Model.md
│   └── adr/
├── templates/
│   ├── Service-Document-Template.md
│   └── ADR-Template.md
└── diagrams/
```

---

## Foundational Documents

| Document                                 | Purpose                                                              |
| ---------------------------------------- | -------------------------------------------------------------------- |
| `MANIFESTO.md`                           | Defines the purpose, belief and founding principles of the ecosystem |
| `docs/0-Operations-Ecosystem-Model.md`   | Defines the model used to structure all service knowledge            |
| `templates/Service-Document-Template.md` | Provides the standard structure for documenting a business service   |
| `templates/ADR-Template.md`              | Provides the standard structure for recording architecture decisions |

---

## Service-Centric Model

The ecosystem is organised around business services, not servers.

Examples of business services include:

* Customer Ordering
* Purchase Order Management
* Mobile App Ordering
* Company Email
* Microsoft 365 Office Applications
* Website Hosting
* Payments
* Backup and Recovery
* Remote Access
* Development Environments

Each service may involve many technical components, suppliers, platforms and dependencies.

The service document connects them into one understandable model.

---

## Service Views

Each service document may include the following views:

1. Service Identity
2. Executive View
3. Service Geography View
4. Operational View
5. Engineering View
6. Architecture and Decision View
7. Recovery and Continuity View
8. Evolution View

These views allow different audiences to navigate the same service knowledge without duplicating or fragmenting information.

---

## Operating Standard

A technology project is not considered complete when the software is deployed.

A project is complete only when the service it creates is:

* Understood
* Documented
* Owned
* Recoverable
* Supportable
* Linked to its dependencies
* Connected to relevant decisions
* Capable of being handed over

---

## Current Status

This repository is in active development.

The first implementation of the model is the Schoolyard Operations Ecosystem.

The model will be refined through real operational use.

