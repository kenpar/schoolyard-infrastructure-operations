# Service Document Template

Use this template for every Business Service documented within the Operations Ecosystem.

Each service should have one document containing multiple views of the same service.

The principle is:

> One Service.  
> One Source of Truth.  
> Multiple Views.  
> One Shared Understanding.

---

# [Service Name]

|Field|Value|
|---|---|
|Document ID|[e.g. SOE-SVC-001]|
|Service Name|[Service name]|
|Service Type|[Business / Operational / Technical / Infrastructure / Support]|
|Version|1.0|
|Status|Draft|
|Author|[Name]|
|Business Owner|[Organisation / Person]|
|Technical Custodian|[Person / Organisation]|
|Last Updated|[Date]|
|Classification|Internal|

---

# 1. Service Identity

## 1.1 At a Glance

|Field|Value|
|---|---|
|Service Name|[Name of the service]|
|Business Purpose|[Short description of what the service does for the business]|
|Primary Users|[Who uses or depends on the service]|
|Business Criticality|[Critical / High / Medium / Low]|
|Business Owner|[Who owns the business responsibility]|
|Technical Custodian|[Who maintains or supports the technology]|
|Data Owner|[Who owns the business data]|
|Primary Provider|[Main external provider, if applicable]|
|Primary Location|[Where the service is hosted, administered or physically held]|
|Backup Location|[Where backups are held]|
|Off-site Backup|[Yes / No / Not applicable]|
|Recovery Target|[Expected recovery timescale]|
|Related Services|[Linked services]|
|Last Reviewed|[Date]|

## 1.2 Plain English Summary

[Write a short plain-English description of the service.]

This section should be understandable to a non-technical business owner.

Example:

> This service allows parents to place school uniform orders online. It connects the mobile application, the Schoolyard online shop and the payment provider so that orders can be placed, paid for and processed by Schoolyard staff.

---

# 2. Executive View

## 2.1 Why This Service Exists

[Explain why the business uses this service.]

## 2.2 Business Value

[Explain what value the service provides.]

Consider:

- Time saved
    
- Revenue protected
    
- Customer service improved
    
- Risk reduced
    
- Operational visibility improved
    
- Manual work avoided
    

## 2.3 Who Uses This Service

|User / Role|How They Use the Service|
|---|---|
|[Role]|[Usage]|
|[Role]|[Usage]|

## 2.4 Business Impact if Unavailable

[Explain what happens if this service stops working.]

|Impact Area|Description|
|---|---|
|Customers|[Impact]|
|Staff|[Impact]|
|Operations|[Impact]|
|Finance|[Impact]|
|Reputation|[Impact]|

## 2.5 Business Criticality

|Level|Selected|
|---|---|
|Critical|[Yes / No]|
|High|[Yes / No]|
|Medium|[Yes / No]|
|Low|[Yes / No]|

Reason:

[Explain why this criticality level has been selected.]

---

# 3. Service Geography View

## 3.1 Where This Service Lives

[Explain where the service is physically, logically and commercially held.]

This should include hosting providers, cloud platforms, app stores, domain providers, source code locations, third-party systems and backup locations.

|Component|Location / Provider|Purpose|
|---|---|---|
|[Component]|[Provider / Location]|[Purpose]|
|[Component]|[Provider / Location]|[Purpose]|

## 3.2 Service Geography Map

```text
[Actor / User]
      ↓
[Service entry point]
      ↓
[Supporting platform]
      ↓
[Core system]
      ↓
[Business outcome]
```

Replace the map above with a simple visual flow.

Example:

```text
Parent
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
Schoolyard Order Processing
```

## 3.3 Providers and Platforms

|Provider / Platform|Role in Service|Administered By|
|---|---|---|
|[Provider]|[Role]|[Person / Organisation]|
|[Provider]|[Role]|[Person / Organisation]|

## 3.4 Ownership and Responsibility

|Area|Responsible Party|
|---|---|
|Business Ownership|[Name / Organisation]|
|Technical Maintenance|[Name / Organisation]|
|Source Code Ownership|[Name / Organisation]|
|Data Ownership|[Name / Organisation]|
|Supplier Relationship|[Name / Organisation]|
|Billing Responsibility|[Name / Organisation]|

---

# 4. Operational View

## 4.1 Normal Business Workflow

[Describe how the service works in day-to-day business use.]

## 4.2 Operational Flow Map

```text
[Step 1]
  ↓
[Step 2]
  ↓
[Step 3]
  ↓
[Step 4]
  ↓
[Outcome]
```

## 4.3 Inputs and Outputs

|Type|Description|
|---|---|
|Inputs|[Information, actions or data entering the service]|
|Outputs|[Information, actions or data produced by the service]|

## 4.4 User Roles

|Role|Responsibility|
|---|---|
|[Role]|[Responsibility]|
|[Role]|[Responsibility]|

## 4.5 Normal Operating Procedure

[Describe the normal operational process.]

## 4.6 Common Issues

|Issue|Likely Cause|First Action|
|---|---|---|
|[Issue]|[Cause]|[Action]|

## 4.7 Escalation Path

|Situation|Escalate To|
|---|---|
|[Situation]|[Person / Team / Supplier]|

---

# 5. Engineering View

## 5.1 Technical Summary

[Summarise how the service is technically implemented.]

## 5.2 Technology Stack

|Layer|Technology|
|---|---|
|Application|[Technology]|
|Backend|[Technology]|
|Database|[Technology]|
|Hosting|[Technology / Provider]|
|Authentication|[Technology / Provider]|
|Payments|[Technology / Provider]|
|Monitoring|[Technology / Provider]|
|Backup|[Technology / Provider]|

## 5.3 Source Code

|Repository|Location|Purpose|
|---|---|---|
|[Repository name]|[GitHub / Local / Other]|[Purpose]|

## 5.4 Hosting and Server Details

|Item|Value|
|---|---|
|Hostname|[Hostname]|
|Provider|[Provider]|
|IP Address|[IP / Tailscale IP / Internal IP]|
|Operating System|[OS]|
|Runtime|[Docker / PM2 / Other]|
|Primary Path|[Filesystem path]|
|Public URL|[URL]|

## 5.5 Configuration

|Configuration Area|Location / Notes|
|---|---|
|Environment Variables|[Path / system]|
|DNS|[Provider / records]|
|Certificates|[Provider / location]|
|Secrets|[Where managed]|
|Application Config|[Location]|

Do not place secret values directly in this document.

Document where they are held and how they are managed.

## 5.6 Deployment

[Describe how the service is deployed.]

```bash
# Deployment commands or reference to deployment procedure
```

## 5.7 Logs and Monitoring

|Log / Monitor|Location / Access|
|---|---|
|[Log]|[Location]|
|[Monitor]|[Location]|

## 5.8 Maintenance Tasks

|Task|Frequency|Owner|
|---|---|---|
|[Task]|[Frequency]|[Owner]|

---

# 6. Architecture and Decision View

## 6.1 Architecture Summary

[Describe the architecture at a high level.]

## 6.2 Engineering Architecture Map

```text
[Technical Component]
      ↓
[Technical Component]
      ↓
[Technical Component]
      ↓
[Technical Outcome]
```

## 6.3 Key Design Decisions

|Decision|Reason|ADR|
|---|---|---|
|[Decision]|[Reason]|[ADR reference]|

## 6.4 Relevant ADRs

|ADR|Title|Status|
|---|---|---|
|ADR-0001|[Title]|[Accepted / Draft / Superseded]|

## 6.5 Constraints and Trade-offs

[Explain any important limitations, trade-offs or constraints.]

## 6.6 Alternatives Considered

[Record any alternatives that were considered and why they were not selected.]

---

# 7. Recovery and Continuity View

## 7.1 Recovery Summary

[Explain how the service can be recovered if it fails.]

## 7.2 Backup Overview

|Backup Item|Location|Frequency|Retention|
|---|---|---|---|
|[Item]|[Location]|[Frequency]|[Retention]|

## 7.3 Off-site Protection

|Off-site Backup|Details|
|---|---|
|Status|[Yes / No / Not applicable]|
|Provider|[Provider]|
|Location|[Location]|
|Verification|[How verified]|

## 7.4 Recovery Target

|Target|Value|
|---|---|
|Recovery Time Objective|[Target time]|
|Recovery Point Objective|[Maximum acceptable data loss]|

## 7.5 Restore Procedure

[Either include the restore procedure or link to the restore document.]

```bash
# Restore commands or reference
```

## 7.6 Recovery Dependencies

|Dependency|Required Before Restore?|Notes|
|---|---|---|
|[Dependency]|[Yes / No]|[Notes]|

## 7.7 Last Backup Verification

|Item|Value|
|---|---|
|Last Successful Backup|[Date / status]|
|Last Backup Check|[Date / status]|
|Last Restore Test|[Date / status]|
|Verified By|[Name]|

## 7.8 Business Continuity Workaround

[Explain how the business can continue temporarily if the service is unavailable.]

---

# 8. Evolution View

## 8.1 Current Status

[Describe the current maturity or operational status of the service.]

## 8.2 Known Limitations

|Limitation|Impact|Possible Improvement|
|---|---|---|
|[Limitation]|[Impact]|[Improvement]|

## 8.3 Planned Improvements

|Improvement|Priority|Notes|
|---|---|---|
|[Improvement]|[High / Medium / Low]|[Notes]|

## 8.4 Future Opportunities

[Capture ideas that may be useful later.]

## 8.5 Technical Debt

|Item|Risk|Proposed Action|
|---|---|---|
|[Item]|[Risk]|[Action]|

## 8.6 Review Notes

[Record notes from service reviews.]

---

# 9. Related Documents

|Document|Purpose|
|---|---|
|[Document name]|[Purpose]|

Examples:

- Operations Ecosystem Model
    
- Infrastructure Standards
    
- Backup Architecture
    
- Restore Procedure
    
- Relevant ADRs
    
- Supplier records
    
- Service agreements
    

---

# 10. Revision History

|Version|Date|Author|Notes|
|---|---|---|---|
|1.0|[Date]|[Name]|Initial version|