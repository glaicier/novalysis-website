---
title: "Security"
meta_title: "Security | Novalysis M365 Migration Planner"
description: "Learn how Novalysis protects your data with a security-first architecture deployed within your own Azure environment."
draft: false
---

## Your Data, Your Control

Unlike traditional SaaS migration tools that require you to send your tenant data to third-party infrastructure, Novalysis takes a fundamentally different approach.

### Azure Managed Application

Novalysis is deployed as an Azure Managed Application directly within your Azure subscription. This means:

- **Your data never leaves your environment** — All tenant information stays within Azure resources you own
- **No external API calls** — The application communicates only with your M365 tenant and Azure services
- **Full visibility** — See exactly what resources are deployed and what they're doing
- **Compliance alignment** — Meets data residency requirements because data stays in your chosen Azure region

### No Third-Party Data Extraction

Traditional migration projects often involve consultancies or third parties extracting and downloading copies of sensitive tenant information onto their own devices. This creates risk and compliance concerns.

Novalysis eliminates this by keeping all data within the application:

- **Export controls built into RBAC** — Administrators explicitly control who can export what data
- **No local downloads required** — Work with your data through the secure web interface
- **Audit trail for exports** — If data is exported, you know who did it and when
- **Consultant access without data leakage** — Grant collaborators access to the platform without them needing copies of your data

---

## Authentication & Access Control

### Azure AD Integration

Novalysis uses Microsoft Entra ID (Azure AD) for all authentication. This simplifies things for your users—they sign in with credentials they already know, with no new passwords to remember or manage.

- **No local passwords** — Users sign in with their existing organisational credentials
- **MFA support** — Leverage your existing conditional access policies
- **Single sign-on** — Seamless experience for users already signed into Microsoft 365
- **Familiar experience** — Users don't need to create or remember another account

### Role-Based Access Control

Three roles provide appropriate access levels:

| Role | Capabilities |
|------|-------------|
| **Admin** | Full access including configuration, user management, export controls, and all features |
| **Analyst** | Access to discovery data, task management, and reporting |
| **Viewer** | Read-only access to dashboards and reports |

Export permissions are controlled separately, ensuring that even users with broad read access cannot extract data without explicit administrator consent.

---

## Data Protection

### Encryption

- **At rest**: All data encrypted using Azure SQL Transparent Data Encryption
- **In transit**: TLS 1.2+ for all communications
- **Secrets management**: Azure Key Vault for all sensitive configuration

---

## Audit & Compliance

### Complete Audit Trail

Every action in Novalysis is logged:

- Who accessed what data and when
- All changes to tasks, communications, and configuration
- AI agent interactions and outputs
- Data sync operations and results
- Export requests and approvals

### Data Retention

You control data retention:

- Configure retention periods to match your policies
- Export data before removal
- Complete data deletion on application removal

---

## Compliance Frameworks

Novalysis architecture supports compliance with:

- **GDPR** — Data stays in your chosen EU region
- **ISO 27001** — Built on Azure's certified infrastructure
- **SOC 2** — Leverages Azure's SOC 2 compliant services
- **Industry regulations** — Financial services, healthcare, and government compatible

---

## Security FAQ

**Q: Can Novalysis employees access my data?**
No. The application runs entirely within your Azure subscription. We have no access to your deployment or data.

**Q: What happens to my data if I stop using Novalysis?**
When you delete the Azure Managed Application, all data is deleted with it. You can export data before removal.

**Q: Can consultants or third parties access our data?**
You control access through RBAC. Grant collaborators Viewer or Analyst access so they can work within the platform without needing to download or extract your tenant data.

**Q: How are updates handled?**
Updates are published through Azure Managed Application versioning. You control when updates are applied.

**Q: Is the source code available for review?**
Enterprise customers can request source code review as part of security assessment.
