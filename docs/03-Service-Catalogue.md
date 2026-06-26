# Document 03 — Service Catalogue

| Field          | Value             |
| -------------- | ----------------- |
| Document ID    | SOE-03            |
| Title          | Service Catalogue |
| Version        | 1.0               |
| Status         | Draft             |
| Author         | Ken Parsons       |
| Owner          | Schoolyard Ltd    |
| Last Updated   | June 2026         |
| Classification | Internal          |

---

# 1. Purpose

This document provides the Service Catalogue for the Schoolyard Operations Ecosystem.

The Service Catalogue lists the business services that support Schoolyard Ltd and identifies the purpose, ownership, criticality and documentation status of each service.

The catalogue is not a server inventory.

It is not a list of applications.

It is a business-facing map of the services that allow the organisation to operate.

Each service listed here should eventually have its own service document using the standard Service Document Template.

---

# 2. Catalogue Principle

The Service Catalogue follows the core Operations Ecosystem principle:

> One Service.  
> One Source of Truth.  
> Multiple Views.  
> One Shared Understanding.

Each service represents a business capability.

A service may depend on many technical components, but the business experiences it as a single capability.

For example, the Mobile Ordering Service may involve mobile apps, app stores, source code, a BFF server, WordPress, WooCommerce and Worldpay.

The catalogue records that as one business service.

---

# 3. Service Categories

Services are grouped into the following categories:

|Category|Description|
|---|---|
|Business Services|Services directly supporting business operations|
|Customer Services|Services used directly or indirectly by customers or parents|
|Operational Services|Services used by staff to process work|
|Infrastructure Services|Services supporting hosting, networking, backup and access|
|Productivity Services|Services supporting office work and communication|
|Development Services|Services supporting software development and testing|
|Governance Services|Services supporting ownership, documentation, security and continuity|

---

# 4. Service Catalogue

|Service ID|Service Name|Category|Business Criticality|Status|Service Document|
|---|---|---|---|---|---|
|SVC-001|Customer Ordering Service|Business Service|Critical|Planned|Planned|
|SVC-002|Purchase Order Service|Business Service|Critical|Planned|Planned|
|SVC-003|Warehouse Fulfilment Service|Operational Service|Critical|Planned|Planned|
|SVC-004|Supplier Purchasing Service|Business Service|High|Planned|Planned|
|SVC-005|Mobile Ordering Service|Customer Service|High|Planned|Planned|
|SVC-006|BFF Service|Infrastructure Service|High|Planned|Planned|
|SVC-007|Website and Online Shop Service|Customer Service|High|Planned|Planned|
|SVC-008|Payments Service|Business Service|Critical|Planned|Planned|
|SVC-009|Company Email Service|Productivity Service|Critical|Planned|Planned|
|SVC-010|Microsoft 365 Office Service|Productivity Service|High|Planned|Planned|
|SVC-011|Domain and DNS Service|Infrastructure Service|Critical|Planned|Planned|
|SVC-012|Backup and Recovery Service|Infrastructure Service|Critical|Planned|Planned|
|SVC-013|Remote Access Service|Infrastructure Service|High|Planned|Planned|
|SVC-014|Development Environment Service|Development Service|Medium|Planned|Planned|
|SVC-015|Source Control Service|Development Service|High|Planned|Planned|
|SVC-016|Demo and Test Service|Development Service|Medium|Planned|Planned|
|SVC-017|Documentation and Knowledge Service|Governance Service|High|Active|This repository|

---

# 5. Initial Service Descriptions

## SVC-001 — Customer Ordering Service

The service that records and manages customer orders from creation through fulfilment.

This includes order entry, order status, customer order lines, delivery charges, services applied to products and final completion.

---

## SVC-002 — Purchase Order Service

The service that allows Schoolyard to generate purchase orders from customer demand, send supplier orders, receive goods and track supplier fulfilment.

---

## SVC-003 — Warehouse Fulfilment Service

The service that supports receipt of goods, preparation of shipments and completion of customer orders.

---

## SVC-004 — Supplier Purchasing Service

The service that connects product demand to supplier purchasing, including supplier-specific product data, variants, costs and purchase order lines.

---

## SVC-005 — Mobile Ordering Service

The service that allows parents to browse school uniform products, place orders and make payments using the Schoolyard mobile apps.

This service includes Apple App Store, Google Play, mobile app source code, BFF, WordPress / WooCommerce and Worldpay dependencies.

---

## SVC-006 — BFF Service

The backend service that sits between the mobile applications and the Schoolyard WordPress / WooCommerce systems.

It supports tenant-aware product access, authentication, checkout and payment session creation.

---

## SVC-007 — Website and Online Shop Service

The service that provides public-facing school uniform shop websites and WooCommerce ordering capability.

---

## SVC-008 — Payments Service

The service that enables customer payments through Worldpay and connects payment status back to ordering systems.

---

## SVC-009 — Company Email Service

The service that provides company email communication.

This must clearly identify the difference between the email client used by staff and the provider where mailboxes and domain services are actually hosted.

---

## SVC-010 — Microsoft 365 Office Service

The service that provides office productivity applications such as Outlook, Word, Excel, Teams, OneDrive and related Microsoft 365 functionality.

---

## SVC-011 — Domain and DNS Service

The service that controls domain ownership, DNS records and routing for public-facing and internal services.

---

## SVC-012 — Backup and Recovery Service

The service that protects business systems through local NAS backups, off-site cloud backup and restore procedures.

---

## SVC-013 — Remote Access Service

The service that provides secure private access to servers and infrastructure using Tailscale.

---

## SVC-014 — Development Environment Service

The service that provides local and server-based development environments, including the Pi5 development server and local project repositories.

---

## SVC-015 — Source Control Service

The service that preserves source code history, version control and collaborative development through Git and GitHub.

---

## SVC-016 — Demo and Test Service

The service that provides demonstration and testing environments separate from production systems.

---

## SVC-017 — Documentation and Knowledge Service

The service represented by this repository.

It preserves the Business Service Knowledge Model, operational documentation, templates, ADRs, service maps and future handover knowledge.

---

# 6. Criticality Definitions

|Criticality|Meaning|
|---|---|
|Critical|Service failure would significantly affect business operation, customer ordering, payments, fulfilment, communication or recovery|
|High|Service failure would cause operational disruption but may have a short-term workaround|
|Medium|Service failure would affect productivity or development but not immediately stop core business operations|
|Low|Service failure would have limited immediate business impact|

---

# 7. Service Documentation Status

|Status|Meaning|
|---|---|
|Planned|Service has been identified but not yet fully documented|
|Draft|Service document exists but requires review or completion|
|Active|Service document is usable and maintained|
|Reviewed|Service document has been reviewed and confirmed accurate|
|Retired|Service no longer operates but is retained for historical reference|

---

# 8. Review Process

The Service Catalogue should be reviewed whenever:

- A new business service is introduced.
    
- A service is retired.
    
- A provider changes.
    
- A service becomes more or less critical.
    
- A service document is created or updated.
    
- A recovery procedure changes.
    
- A major architecture decision affects the service landscape.
    

---

# 9. Revision History

|Version|Date|Author|Notes|
|---|---|---|---|
|1.0|March 2026|Ken Parsons|Initial service catalogue created|