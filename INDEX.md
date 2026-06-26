# Schoolyard Operations Ecosystem Index

This index is the main navigation page for the Schoolyard Operations Ecosystem.

Use this page to move between the foundational model, service documents, operational procedures, architecture decisions and recovery information.

---

# 1. Start Here

|Document|Purpose|
|---|---|
|[[MANIFESTO]]|Foundation stone of the Operations Ecosystem|
|[[0-Operations-Ecosystem-Model]]|Defines the Business Service Knowledge Model|
|[[Service-Document-Template]]|Template for documenting each business service|
|[[ADR-Template]]|Template for recording architecture decisions|

---

# 2. Core Operating Model

|Area|Document|
|---|---|
|Infrastructure Standards|[[01-Infrastructure-Standards]]|
|Infrastructure Overview|[[02-Infrastructure-Overview]]|
|Service Catalogue|[[03-Service-Catalogue]]|
|Service Geography|[[04-Service-Geography]]|
|Backup Architecture|[[05-Backup-Architecture]]|
|Recovery Model|[[06-Recovery-Model]]|

---

# 3. Business Services

Each business service should have its own document using the standard service document template.

|Service|Status|Notes|
|---|---|---|
|Customer Ordering Service|Planned|PO System customer order workflow|
|Purchase Order Service|Planned|Supplier purchasing and fulfilment|
|Warehouse Fulfilment Service|Planned|Goods receipt and shipment workflow|
|Mobile Ordering Service|Planned|School uniform mobile apps|
|BFF Service|Planned|Backend service for mobile apps|
|Website and Online Shop Service|Planned|WordPress / WooCommerce sites|
|Company Email Service|Planned|Email hosting and client access|
|Microsoft 365 Office Service|Planned|Office applications and business productivity|
|Backup and Recovery Service|Planned|NAS, Backblaze and restore process|
|Remote Access Service|Planned|Tailscale private access|
|Development Environment Service|Planned|Pi5, demo systems and code workflow|

---

# 4. Service Geography Maps

Service Geography explains where each service lives, who provides it and what it depends on.

|Map|Status|
|---|---|
|Schoolyard Overall Service Geography|Planned|
|Mobile Ordering Geography|Planned|
|Email and Domains Geography|Planned|
|PO System Geography|Planned|
|Backup Estate Geography|Planned|
|Development Estate Geography|Planned|

---

# 5. Architecture Decision Records

Architecture Decision Records preserve why important decisions were made.

|ADR|Title|Status|
|---|---|---|
|ADR-0001|Business Service Knowledge Model|Planned|
|ADR-0002|Service-Centric Documentation|Planned|
|ADR-0003|Service Geography View|Planned|
|ADR-0004|Markdown and Git as Initial Implementation|Planned|
|ADR-0005|Progressive Disclosure for Multiple Audiences|Planned|

---

# 6. Recovery and Continuity

|Document|Purpose|
|---|---|
|Backup Architecture|Describes how backups are structured|
|Backup Verification|Describes how backups are checked|
|Restore Procedures|Describes how services are recovered|
|Disaster Recovery|Describes wider continuity planning|

---

# 7. Templates

|Template|Purpose|
|---|---|
|Service Document Template|Standard service document structure|
|ADR Template|Architecture decision record structure|
|Server Build Template|Future server build standard|
|Change Record Template|Future change tracking format|

---

# 8. Review Notes

This index should be updated whenever a new document, service, ADR or template is added.

The index is not just a list of files.

It is the navigation map for the Operations Ecosystem.