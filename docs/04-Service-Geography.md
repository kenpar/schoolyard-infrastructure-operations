# Document 04 — Service Geography

| Field          | Value             |
| -------------- | ----------------- |
| Document ID    | SOE-04            |
| Title          | Service Geography |
| Version        | 1.0               |
| Status         | Draft             |
| Author         | Ken Parsons       |
| Owner          | Schoolyard Ltd    |
| Last Updated   | June 2026         |
| Classification | Internal          |

---

# 1. Purpose

This document defines the Service Geography model used within the Schoolyard Operations Ecosystem.

Service Geography explains where a business service lives.

It identifies the providers, platforms, hosting locations, source code locations, data locations, dependencies and ownership responsibilities that make up a service.

This is one of the most important parts of the Operations Ecosystem because it gives business owners and technical staff a shared understanding of where services are physically, logically and commercially held.

---

# 2. Why Service Geography Matters

Many businesses use technology services without clearly knowing where those services actually live.

For example:

- A business may use Outlook and assume its email is with Microsoft.
    
- A business may have a website without knowing who controls the domain or DNS.
    
- A business may use a mobile app without knowing where the backend server is hosted.
    
- A business may take payments without understanding which systems sit between the customer and the payment provider.
    
- A business may have backups without knowing where they are stored or whether an off-site copy exists.
    

This creates operational risk.

If something fails, the business may not know who to contact, which platform is responsible, where the data is held or what dependencies are involved.

Service Geography makes these relationships visible.

---

# 3. Core Principle

A business service should not be documented only by what it is called.

It should be documented by where it lives, who provides it, who owns it, what it depends on and how it connects to the business.

The core principle is:

> If the business depends on a service, the business should know where that service lives.

---

# 4. What Service Geography Records

A Service Geography view should identify:

|Area|Description|
|---|---|
|User Entry Point|How users access the service|
|Business Owner|Who is accountable for the service|
|Technical Custodian|Who maintains the service|
|Primary Provider|The main provider or platform|
|Hosting Location|Where the service is hosted|
|Data Location|Where business data is stored|
|Source Code Location|Where source code is held, if applicable|
|Domain / DNS Provider|Who controls domain routing|
|Authentication Provider|How users authenticate|
|Payment Provider|Which platform handles payments, if applicable|
|Backup Location|Where backups are stored|
|Off-site Backup|Whether an off-site copy exists|
|Dependencies|Other services required for this service to operate|
|Support Route|Who should be contacted if the service fails|

---

# 5. Business-Level Geography

The business-level map should be written in plain language.

It should avoid unnecessary technical detail.

Its purpose is to help business owners, directors and managers understand where the service lives.

## Example — Company Email

|Component|Location / Provider|Purpose|
|---|---|---|
|Domain|20i|Holds the domain and DNS records|
|Mailboxes|20i|Hosts the company email accounts|
|Email Client|Microsoft Outlook|Used by staff to read and send email|
|Office Applications|Microsoft 365|Provides Outlook, Word, Excel and other applications|

Plain English explanation:

> Staff may use Microsoft Outlook to access email, but the email mailboxes and domain services are hosted with 20i. Microsoft Outlook is the application used to read and send email; it is not necessarily where the email service itself lives.

---

# 6. Technical Geography

The technical geography map provides deeper information for engineers and technical support staff.

It may include:

- Server hostnames
    
- IP addresses
    
- Tailscale addresses
    
- DNS records
    
- Ports
    
- Runtime environments
    
- Application paths
    
- Repositories
    
- Environment file locations
    
- Backup scripts
    
- Monitoring locations
    
- Certificates
    
- Third-party APIs
    

This information belongs in the Engineering View of the relevant service document, but Service Geography provides the conceptual map that links the technical detail back to the business service.

---

# 7. Service Geography Map Format

Each service should include a simple visual map.

The map should show the path from user or business actor to business outcome.

## Standard Map Pattern

```text
[Actor]
  ↓
[Entry Point]
  ↓
[Distribution / Access Platform]
  ↓
[Core Service]
  ↓
[Supporting Services]
  ↓
[Business Outcome]
```

The map should be simple enough for a non-technical reader to understand.

Technical maps may be added later in the Engineering View.

---

# 8. Example — Mobile Ordering Service

## Business-Level Map

```text
Parent
  ↓
Apple App Store / Google Play
  ↓
Schoolyard Mobile App
  ↓
Schoolyard Ordering Service
  ↓
Payment
  ↓
Schoolyard Order Processing
```

## Service Geography

|Component|Location / Provider|Purpose|
|---|---|---|
|Mobile App Distribution|Apple App Store / Google Play|Allows parents to download the app|
|Mobile App Source Code|KJP Technologies|Maintains and develops the mobile application code|
|Backend Service|DigitalOcean|Hosts the BFF server used by the mobile apps|
|Product and Order Data|WordPress / WooCommerce|Holds product and order information|
|Payments|Worldpay|Processes customer payments|
|Business Operation|Schoolyard Ltd|Processes and fulfils customer orders|

## Plain English Explanation

> Parents access the service through the mobile app. The app is distributed through Apple and Google, but the source code is maintained separately. The app communicates with a backend server hosted by DigitalOcean, which connects to Schoolyard’s WooCommerce systems and Worldpay payments. The business outcome is that parents can place and pay for orders that Schoolyard can process.

---

# 9. Example — Backup and Recovery Service

## Business-Level Map

```text
Production Systems
  ↓
Local Backup Scripts
  ↓
UGREEN NAS
  ↓
Backblaze B2 Off-site Backup
  ↓
Recovery if Required
```

## Service Geography

|Component|Location / Provider|Purpose|
|---|---|---|
|Production Systems|Schoolyard / Cloud / VPS / Local servers|Systems being protected|
|Local Backup Storage|UGREEN NAS|Holds primary backup copies|
|Off-site Backup|Backblaze B2|Holds cloud-based off-site backup copy|
|Backup Automation|Linux cron / scripts|Runs scheduled backups|
|Verification|Backup check scripts|Confirms backup status|

## Plain English Explanation

> Business systems are copied to the UGREEN NAS so that local recovery is possible. The NAS is then copied to Backblaze B2 to provide an off-site copy. This protects the business against both system failure and local storage failure.

---

# 10. Dependency Mapping

Every Service Geography view should identify dependencies.

A dependency is another service, provider or platform required for the service to operate.

## Dependency Types

|Dependency Type|Meaning|
|---|---|
|Hosting Dependency|The service requires a hosting platform|
|Data Dependency|The service requires another system’s data|
|Authentication Dependency|The service requires login or identity services|
|Payment Dependency|The service requires a payment provider|
|Network Dependency|The service requires internet, DNS or private networking|
|Backup Dependency|The service requires backup storage or backup automation|
|Development Dependency|The service requires source code, build tools or developer access|
|Supplier Dependency|The service requires an external supplier|

---

# 11. Business Questions Answered by Service Geography

Service Geography should allow the business to answer questions such as:

- Where is our email hosted?
    
- Who controls our domain?
    
- Where are our websites hosted?
    
- Where do the mobile apps live?
    
- Where is the backend server for the mobile apps?
    
- Where is the source code held?
    
- Where are payments processed?
    
- Which services depend on 20i?
    
- Which services depend on DigitalOcean?
    
- Which services depend on Microsoft 365?
    
- Which services are backed up?
    
- Where are the backups?
    
- Which services would be affected if a supplier was unavailable?
    

---

# 12. Engineering Questions Answered by Service Geography

Service Geography should allow technical staff to answer questions such as:

- Which systems are in the path of a customer transaction?
    
- Which DNS provider controls the service?
    
- Which server hosts the backend?
    
- Which repositories support the service?
    
- Which backup scripts protect the service?
    
- Which APIs are involved?
    
- Which provider outage would affect the service?
    
- Which ADRs explain why the service is built this way?
    

---

# 13. Documentation Rules

When creating a Service Geography view:

1. Start with the business actor.
    
2. Show the service path in plain language.
    
3. Identify all providers and platforms.
    
4. Separate user-facing tools from actual hosting locations.
    
5. Identify who owns the data.
    
6. Identify who administers the service.
    
7. Identify dependencies.
    
8. Link to technical detail rather than overcrowding the business view.
    
9. Use simple maps.
    
10. Keep the map understandable.
    

---

# 14. Review Process

Service Geography should be reviewed whenever:

- A provider changes.
    
- A hosting location changes.
    
- A domain or DNS provider changes.
    
- A new dependency is added.
    
- A service is moved to another platform.
    
- A backup location changes.
    
- A source code location changes.
    
- A support responsibility changes.
    
- A business owner or technical custodian changes.
    

---

# 15. Foundational Statement

Service Geography exists to make invisible technology visible.

It allows the business to understand not only that a service exists, but where it lives, who provides it, what it depends on and how it connects to the organisation.

A business owner should never be left saying:

> “We have email, but I do not know where it is.”

The Operations Ecosystem exists to answer that question clearly.

---

# 16. Revision History

|Version|Date|Author|Notes|
|---|---|---|---|
|1.0|March 2026|Ken Parsons|Initial Service Geography document created|