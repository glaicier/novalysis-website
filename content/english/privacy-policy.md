---
title: "Privacy Policy"
meta_title: "Privacy Policy | Novalysis"
description: "Privacy Policy for Novalysis M365 Migration Planner - Learn how we protect your data."
draft: false
---

**Novalysis / M365 Migration Planner**  
**Effective Date:** January 9, 2026  
**Last Updated:** January 9, 2026

---

## 1. Introduction

### Who We Are

Glaicier ("we," "us," or "our") provides the M365 Migration Planner (Novalysis), a SaaS application designed to help organizations plan, assess, and execute migrations between Microsoft 365 tenants. Our platform leverages artificial intelligence and automation to streamline complex migration projects while maintaining the highest standards of data security and privacy.

### What This Policy Covers

This Privacy Policy explains how we collect, use, store, and protect information when you use the M365 Migration Planner application deployed as an Azure Managed Application. This policy applies to all users of our service, regardless of subscription tier or deployment configuration.

### Our Commitment to Privacy

We are committed to transparency and your privacy. Our architecture is designed with **data sovereignty** as a core principle: your organization's Microsoft 365 data remains in **your Azure tenant** at all times. We only collect minimal, sanitized telemetry data necessary to operate and improve the service.

---

## 2. What Data We Collect

We collect only the minimum data necessary to provide, maintain, and improve our service. All data collection follows industry best practices for privacy and security.

### 2.1 Sanitized Telemetry Data

We collect anonymized operational telemetry from our application, including:

- **Application Performance Metrics**: API response times, function execution durations, database query performance
- **Feature Usage Statistics**: Which features are used, frequency of use, user interface interactions (no content data)
- **Error Logs**: Sanitized error messages with stack traces (stripped of all personally identifiable information)
- **System Health Indicators**: Resource utilization, sync job status, service availability metrics
- **Authentication Events**: Login/logout timestamps, authentication method used (no credentials)

**Important**: All telemetry data is automatically sanitized before transmission. User identifiers are replaced with anonymized tokens, and any potential PII is stripped from error messages and logs.

### 2.2 Account and Configuration Data

We store minimal configuration data necessary to operate your deployment:

- **Deployment Configuration**: Your customer code, subscription tier, Azure region, deployment date
- **API Subscription Keys**: Encrypted APIM subscription keys for accessing shared infrastructure
- **Service Endpoints**: URLs for your deployment's Azure Functions and App Service instances
- **Feature Flags**: Settings for AI deployment model (shared vs. dedicated) and enabled features

### 2.3 Aggregated Usage Metrics

We maintain aggregated, non-identifiable statistics for operational purposes:

- Total number of active deployments
- Average migration project size (in number of users/mailboxes/sites)
- Feature adoption rates across all customers
- Infrastructure capacity planning metrics

**These metrics cannot be traced back to individual customers or users.**

---

## 3. What Data We Don't Collect

**This is critical**: We want to be absolutely clear about what data we **DO NOT** collect or have access to:

### 3.1 Microsoft 365 Content

We **never** collect, store, or transmit:

- **Email content** — Message bodies, subjects, attachments, metadata
- **Documents** — Files from SharePoint, OneDrive, or Teams
- **Chat messages** — Teams conversations, private messages, channel communications
- **Calendar data** — Meeting details, appointments, attendee lists
- **Contact information** — Personal or business contact details beyond what's visible in directory metadata

### 3.2 Personally Identifiable Information (PII)

We do not collect or store:

- **User names** — Full names, display names, user principal names
- **Email addresses** — Personal or business email addresses
- **Phone numbers** — Mobile, office, or personal phone numbers
- **Physical addresses** — Office locations, mailing addresses
- **Identification numbers** — Employee IDs, social security numbers, passport numbers
- **Biometric data** — Fingerprints, facial recognition data
- **Financial information** — Credit cards, bank accounts, payment details

### 3.3 Migration Data Content

All migration assessment data remains in **your Azure tenant**:

- We do not access the content of mailboxes being migrated
- We do not read or store SharePoint documents being assessed
- We do not access Teams files or chat history
- We do not store user passwords or authentication credentials

### 3.4 Directory Metadata

While our application reads Microsoft 365 directory metadata (via Microsoft Graph API) to perform migration assessments, this data **remains exclusively in your tenant's database**. We do not copy or transmit:

- User display names or email addresses to our infrastructure
- Group membership details to our systems
- SharePoint site titles or URLs to our telemetry
- Mailbox sizes or quota information to our logs

---

## 4. How We Use Data

We use the limited data we collect solely for the following purposes:

### 4.1 Service Operation

- **Routing and Authentication**: Directing your requests to the correct infrastructure and validating access
- **Performance Monitoring**: Ensuring optimal response times and identifying bottlenecks
- **Error Detection**: Identifying and resolving technical issues in the application
- **Capacity Planning**: Scaling shared infrastructure (APIM, Azure OpenAI) based on aggregate demand

### 4.2 Product Improvement

- **Feature Analytics**: Understanding which features are most valuable to prioritize development
- **User Experience Optimization**: Identifying UI/UX pain points through anonymized interaction patterns
- **AI Model Enhancement**: Improving AI assistant responses based on sanitized usage patterns (no customer data)

### 4.3 Customer Support

- **Troubleshooting**: Investigating reported issues using sanitized logs and error traces
- **Performance Optimization**: Recommending configuration changes based on usage patterns
- **Proactive Monitoring**: Detecting and resolving issues before they impact your users

### 4.4 Compliance and Security

- **Audit Logs**: Maintaining records of system access and changes for security purposes
- **Threat Detection**: Identifying and responding to potential security incidents
- **Regulatory Compliance**: Meeting legal obligations under GDPR, SOC 2, and other frameworks

**We will never:**
- Sell your data to third parties
- Use your data for advertising or marketing to you
- Share your data with other customers or external parties (except as required by law)
- Train public AI models on your data

---

## 5. Data Storage & Sovereignty

### 5.1 Customer Data Resides in Your Tenant

**This is our key architectural differentiator**: All of your organization's Microsoft 365 data, migration assessments, and configuration settings are stored exclusively in **your Azure tenant**, specifically:

- **Azure SQL Database**: All migration data, user lists, site inventories, and application settings are stored in a database within your Azure subscription
- **Azure Blob Storage**: Migration artifacts, reports, and temporary files are stored in your storage account
- **Azure Key Vault**: Your secrets, connection strings, and encryption keys remain in your Key Vault

**You maintain complete control**: You can access, audit, export, or delete this data at any time using standard Azure tools.

### 5.2 Shared Infrastructure in Our Tenant

We operate shared infrastructure for cost-efficiency and centralized management:

- **Azure API Management**: Routes requests and enforces policies (no customer data stored)
- **Azure OpenAI**: Processes AI assistant queries with sanitized prompts (no retention after response)
- **Application Insights**: Collects sanitized telemetry with PII stripped (90-day retention)
- **Control Plane Database**: Stores only deployment metadata (customer code, subscription keys, endpoint URLs)

### 5.3 Data Residency

- **Your Data**: Resides in the Azure region you selected during deployment (e.g., East US, West Europe)
- **Our Telemetry**: Stored in our primary Azure region (United States) but contains no identifiable customer data
- **Compliance**: You can select Azure regions that meet your specific data residency requirements (EU, UK, Canada, etc.)

### 5.4 Data Isolation

Each customer deployment is fully isolated:

- **Dedicated Database**: Your data is in your own Azure SQL Database, not shared with other customers
- **Dedicated Storage**: Your files are in your own Storage Account with encryption keys you control
- **Network Isolation**: Optional Azure Private Endpoints can be enabled to keep all traffic within Azure backbone

---

## 6. AI & Machine Learning

### 6.1 Azure OpenAI Usage

We use **Azure OpenAI Service** to power our AI assistant feature, which helps answer questions about your migration project. Here's how we protect your privacy:

**Shared OpenAI Model (Default)**:
- We operate a shared Azure OpenAI deployment in our tenant for cost-efficiency
- Your Functions send API requests to our Azure API Management gateway
- APIM forwards requests to Azure OpenAI with customer-specific policies applied

**Dedicated OpenAI Model (Optional)**:
- Enterprise customers can deploy Azure OpenAI in their own tenant
- Requests are processed entirely within your Azure subscription
- You have complete control over the AI instance

### 6.2 Prompt Sanitization

**Critical privacy protection**: Before any query reaches Azure OpenAI, we sanitize prompts to remove PII:

**What We Strip**:
- User names → Replaced with anonymized identifiers (e.g., "User_ABC123")
- Email addresses → Replaced with role descriptions (e.g., "Marketing Manager")
- SharePoint URLs → Replaced with generic references (e.g., "Site_001")
- Mailbox names → Replaced with department labels (e.g., "Finance Department")
- Any detected PII → Automatically redacted using pattern matching

### 6.3 AI Data Retention

- **Azure OpenAI**: Does **not** store prompts or responses after generating answers (per Microsoft's Abuse Monitoring policy for Azure OpenAI)
- **Our Logs**: We log sanitized prompts only for troubleshooting (30-day retention), with all PII already stripped
- **Model Training**: Your data is **never** used to train OpenAI's models or our custom models

---

## 7. Data Security

### 7.1 Encryption

**Data at Rest**:
- All data in your Azure tenant is encrypted using **AES-256 encryption**
- Azure SQL Database: Transparent Data Encryption (TDE) enabled by default
- Azure Blob Storage: Storage Service Encryption (SSE) enabled by default
- Option to use **Customer-Managed Keys (CMK)** in your Azure Key Vault for additional control

**Data in Transit**:
- All API communications use **TLS 1.2 or higher** encryption
- HTTPS enforced for all web traffic
- Private Endpoints available for Azure backbone-only communication (no public internet)

### 7.2 Access Controls

**Azure Role-Based Access Control (RBAC)**:
- Your Functions use **Managed Identity** to access your database (no stored passwords)
- Principle of least privilege: Each component has only the permissions it requires
- Deny assignment on managed resource group prevents unauthorized modifications

**Authentication**:
- User authentication via **Microsoft Entra ID** (Azure Active Directory)
- Multi-factor authentication (MFA) supported and recommended
- OAuth 2.0 and OpenID Connect protocols for secure token exchange

### 7.3 Security Monitoring

- **Application Insights**: Real-time monitoring of security events and anomalies
- **Azure Monitor Alerts**: Automatic notifications for suspicious activity
- **Automated Threat Detection**: AI-powered anomaly detection in access patterns
- **Regular Security Audits**: Periodic third-party security assessments

---

## 8. Sub-Processors

We engage the following third-party service providers ("sub-processors") who may process data on our behalf:

### 8.1 Microsoft Azure (Primary Infrastructure)

- **Services Used**: Azure App Service, Azure Functions, Azure SQL Database, Azure Storage, Azure Key Vault, Application Insights, Azure API Management
- **Data Processed**: All customer data (in customer's tenant), sanitized telemetry (in our tenant)
- **Location**: Your selected Azure region for customer data; United States for our telemetry
- **Security**: Microsoft Azure SOC 2 Type II, ISO 27001, GDPR-compliant

### 8.2 Azure OpenAI (AI Processing)

- **Services Used**: Azure OpenAI Service (GPT-4, text-embedding models)
- **Data Processed**: Sanitized prompts only (all PII stripped before transmission)
- **Security**: Azure OpenAI does not retain prompts or outputs

### 8.3 No Other Sub-Processors

We do **not** use:
- Third-party analytics platforms (e.g., Google Analytics, Mixpanel)
- Third-party marketing tools for your data
- Third-party AI services beyond Azure OpenAI
- Third-party data processors or data brokers

---

## 9. User Rights (GDPR Compliance)

We are committed to complying with the **General Data Protection Regulation (GDPR)** and similar privacy laws worldwide. As a data subject, you have the following rights:

### 9.1 Right to Access (Article 15)

You have the right to request access to your personal data. Contact us at privacy@glaicier.com.

### 9.2 Right to Rectification (Article 16)

You have the right to request correction of inaccurate data through the admin interface or by contacting support.

### 9.3 Right to Erasure (Article 17)

You can delete your Azure SQL Database, Storage Account, or entire resource group at any time. Contact privacy@glaicier.com to request deletion of sanitized telemetry.

### 9.4 Right to Data Portability (Article 20)

Export your migration data directly from your Azure SQL Database using standard Azure tools. Formats available: JSON, CSV, SQL backup (.bacpac).

### 9.5 Right to Lodge a Complaint

**EU Residents**: Contact your national Data Protection Authority (DPA)  
**UK Residents**: Contact the Information Commissioner's Office (ICO)

---

## 10. Data Retention

### 10.1 Customer Tenant Data (Your Control)

Data in your Azure tenant is retained **indefinitely** until you choose to delete it.

### 10.2 Sanitized Telemetry in Our Tenant

| Data Type | Retention Period |
|-----------|------------------|
| Application Logs | 90 days |
| Error Traces | 90 days |
| Performance Metrics | 13 months |
| Feature Usage Stats | 24 months |
| Aggregated Analytics | Indefinite (anonymized) |

---

## 11. Changes to This Policy

We may update this Privacy Policy from time to time. When we make material changes:

1. **Email Notification**: We will send an email at least **30 days before** changes take effect
2. **In-App Notification**: A banner will appear in the application
3. **Version History**: Previous versions will be archived at our website

---

## 12. Contact Information

### Data Protection Officer (DPO)

**Email**: privacy@glaicier.com  
**Response Time**: Within 2 business days (initial response); within 30 days (full resolution)

### General Support

**Email**: support@glaicier.com  
**Website**: [https://novalysis.io](https://novalysis.io)
