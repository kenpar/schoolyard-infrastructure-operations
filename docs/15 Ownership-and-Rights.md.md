# Document 14 – Ownership and Rights

| **Document ID**    | IOM-14                       |
| ------------------ | ---------------------------- |
| **Title**          | Ownership and Rights         |
| **Version**        | 0.1                          |
| **Status**         | Draft                        |
| **Author**         | Ken Parsons                  |
| **Owner**          | Schoolyard Ltd / Ken Parsons |
| **Last Updated**   | June 2026                    |
| **Classification** | Internal                     |

---

# 1. Purpose

This document records the intended ownership, usage rights and development responsibilities for software systems, applications and infrastructure components created for the Schoolyard operating environment.

The purpose is to avoid ambiguity regarding what Schoolyard Ltd may use operationally, what intellectual property remains owned by Ken Parsons, and who is authorised to develop, modify or commercially reuse the underlying codebases.

This document is an operational ownership record and should be reviewed formally where legal certainty is required.

---

# 2. Scope

This document applies to:

- Schoolyard mobile applications
    
- Schoolyard BFF/API services
    
- Schoolyard PO System
    
- Supporting infrastructure scripts
    
- Deployment processes
    
- Operational documentation
    
- Backup and recovery scripts
    
- Related source code repositories
    

---

# 3. General Principle

Systems built for Schoolyard may be used by Schoolyard for their intended operational purpose.

However, unless otherwise agreed in writing, underlying base code, frameworks, reusable components, implementation patterns and development rights remain controlled by the original developer, Ken Parsons.

Schoolyard’s operational use of a system does not automatically transfer ownership of the underlying source code or grant unrestricted development rights.

---

# 4. Mobile Applications

The Schoolyard mobile applications are considered a jointly beneficial project.

Schoolyard benefits from the applications as a service to schools, parents and uniform operations.

Ken Parsons has designed, built, configured, deployed and maintained the applications and associated technical architecture.

## 4.1 Operational Use

Schoolyard may use the deployed mobile applications for their intended operational purpose.

This includes:

- school uniform ordering
    
- parent-facing product browsing
    
- checkout integration
    
- school-specific app deployments
    
- service delivery to participating schools
    

## 4.2 Development Ownership

The underlying mobile app codebase, architecture, implementation approach and deployment knowledge remain controlled by Ken Parsons unless otherwise agreed.

Schoolyard does not automatically acquire unrestricted rights to independently modify, resell, repackage or redeploy the underlying mobile app framework outside the agreed Schoolyard operational context.

## 4.3 Deployment and Maintenance

Ken Parsons remains the primary technical authority for:

- code development
    
- app configuration
    
- app store deployment
    
- BFF integration
    
- payment integration
    
- release management
    

---

# 5. PO System

The PO System is considered a joint operational project.

Schoolyard may use the deployed PO System to support its working purchase order, customer order, supplier order and fulfilment workflows.

## 5.1 Schoolyard Operational Rights

Schoolyard may use the PO System for its internal business operations.

This includes:

- creating and managing customer orders
    
- creating and managing purchase orders
    
- managing suppliers
    
- managing product data
    
- operating fulfilment workflows
    
- reporting and internal administration
    

## 5.2 Base Code Ownership

The underlying base code, application framework, system design, reusable components, workflow logic and development methodology remain owned and controlled by Ken Parsons unless otherwise agreed in writing.

Schoolyard’s right is an operational right to use the implemented system, not an unrestricted transfer of ownership of the base platform.

## 5.3 Development Authority

Ken Parsons is the primary and authorised developer of the PO System.

Changes to the codebase, workflow design, database structure, deployment model or infrastructure should not be undertaken by third parties without prior agreement.

This protects system integrity, operational continuity and the maintainability of the codebase.

---

# 6. Infrastructure and Backup Scripts

Infrastructure automation, backup scripts and operational procedures created by Ken Parsons for Schoolyard may be used by Schoolyard for the purpose of operating and protecting Schoolyard systems.

Reusable scripting patterns, backup architecture design and general implementation methods remain part of Ken Parsons’ technical work product unless otherwise agreed.

---

# 7. Documentation

Operational documentation created for the Schoolyard infrastructure is intended to support:

- day-to-day operation
    
- handover
    
- maintenance
    
- disaster recovery
    
- continuity planning
    

Schoolyard may use this documentation internally for operational purposes.

The documentation should not be treated as granting unrestricted rights to reuse underlying software designs, codebases or commercial implementation patterns outside the Schoolyard operating environment.

---

# 8. Third-Party Components

The systems may include third-party software, frameworks, libraries, APIs and cloud services.

Ownership and usage of third-party components remain subject to their respective licences and terms.

Examples include:

- WordPress
    
- WooCommerce
    
- Next.js
    
- Expo
    
- React Native
    
- Supabase
    
- Worldpay
    
- Twilio
    
- Tailscale
    
- Backblaze B2
    
- UGREEN NAS software
    

---

# 9. Handover Principle

The objective of this documentation is to make the infrastructure operable and recoverable by another competent engineer if required.

Operational handover does not imply transfer of intellectual property ownership unless explicitly agreed.

A future engineer may operate, maintain and recover systems according to documented procedures, but ownership and development rights remain subject to this document and any formal agreements in place.

---

# 10. Review Requirement

Because this document concerns ownership and rights, it should be reviewed periodically and, where appropriate, formalised through written agreement.

This document should not be treated as a substitute for legal advice.

---

# Revision History

|Version|Date|Author|Description|
|---|---|---|---|
|0.1|March 2026|Ken Parsons|Initial draft|