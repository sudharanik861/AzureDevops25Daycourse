
# Cloud Deployment Models - Detailed Notes

## Overview

Deployment models define WHERE your cloud infrastructure lives
and WHO has access to it.

---

## 1. Public Cloud

### What Is It?
Cloud infrastructure owned by a third-party provider, shared across
multiple organizations, accessed over the public internet.

### Key Characteristics
- Multi-tenant: multiple customers share same physical infrastructure
- Provider manages everything: hardware, security, maintenance
- Pay-as-you-go: no upfront investment
- Globally available: deploy in any region worldwide

### Azure Public Cloud Regions
- 60+ regions worldwide
- India: Central India (Pune), South India (Chennai), West India (Mumbai)
- Each region has multiple data centers (Availability Zones)

### Who Uses It?
- Startups (no budget for own hardware)
- Web applications with variable traffic
- Development and testing environments
- Companies wanting global presence quickly

### Real-World Example
**Zomato/Swiggy:** Traffic goes 10x during lunch (12-2 PM) and dinner (7-10 PM).
Public cloud auto-scales servers during peak, removes them during off-peak.
They pay only for actual usage instead of buying servers for peak capacity.

---

## 2. Private Cloud

### What Is It?
Cloud infrastructure dedicated to a single organization.
Can be hosted on-premises or by a third-party provider.

### Key Characteristics
- Single-tenant: only your organization uses the infrastructure
- Full control over hardware, security, and network configuration
- Meets strict regulatory and compliance requirements
- Higher cost but maximum security and customization

### Types of Private Cloud
| Type | Where | Managed By | Example |
|---|---|---|---|
| On-Premises | Your data center | Your IT team | Company server room |
| Hosted | Provider's data center | Provider | Azure Stack |
| Virtual Private | Within public cloud | Provider with isolation | Azure Dedicated Host |

### Who Uses It?
- Banks and financial institutions (RBI compliance)
- Hospitals (patient data protection)
- Government and defense (classified data)
- Companies with strict data residency laws

### Real-World Example
**State Bank of India:** RBI regulations require customer financial data
to remain within India's borders. SBI operates its own private data centers
with full control over encryption, access policies, and audit trails.

---

## 3. Hybrid Cloud

### What Is It?
Combination of public and private cloud connected through a secure network.
Data and applications can move between the two environments.

### Key Characteristics
- Sensitive data stays on private cloud
- Scalable workloads run on public cloud
- Connected via VPN or Azure ExpressRoute
- Single management plane (Azure Arc)

### How It Works
### Who Uses It?
- Large enterprises with both compliance and scalability needs
- Companies gradually migrating from on-prem to cloud
- Healthcare with sensitive data + public-facing apps
- Financial institutions with regulatory requirements

### Real-World Example
**Apollo Hospitals:**
- PRIVATE: Patient records (Aadhaar, medical history, prescriptions)
  stored in hospital's own data center — compliance with Indian health data laws
- PUBLIC: Appointment booking website on Azure — handles 50,000+ daily
  bookings with auto-scaling during peak hours
- CONNECTION: Secure VPN tunnel between private and public environments

---

## 4. Multi-Cloud

### What Is It?
Using two or more cloud providers simultaneously.
Different workloads run on different providers.

### Why Multi-Cloud?
- Avoid vendor lock-in
- Use best service from each provider
- Redundancy — if one provider goes down, others continue
- Negotiate better pricing

### Common Combinations
| Provider 1 | Provider 2 | Why |
|---|---|---|
| Azure | AWS | Azure for .NET apps, AWS for ML |
| AWS | GCP | AWS for compute, GCP for BigQuery analytics |
| Azure | GCP | Azure for enterprise, GCP for Kubernetes |

### Real-World Example
**Netflix:** Uses AWS for streaming infrastructure and GCP for
data analytics and machine learning. If AWS has an issue in one region,
they can redirect traffic.

---

## 5. Community Cloud

### What Is It?
Cloud infrastructure shared by several organizations with common
requirements — same industry, compliance rules, or security needs.

### Who Uses It?
- Government agencies sharing common infrastructure
- Healthcare organizations with common HIPAA requirements
- Educational institutions sharing research computing
- Financial institutions sharing compliance frameworks

### Real-World Example
**NIC (National Informatics Centre):** Provides cloud infrastructure
for all Indian government departments and ministries. Common security
standards, shared compliance certification, reduced cost per department.

---

## Quick Reference: All 5 Models

| Model | Infrastructure | Access | Best For |
|---|---|---|---|
| Public | Provider-owned, shared | Everyone | Startups, web apps |
| Private | Org-owned, dedicated | One organization | Banks, hospitals, govt |
| Hybrid | Public + Private | One org, split workloads | Large enterprises |
| Multi-Cloud | Multiple providers | One org, multiple vendors | Avoiding lock-in |
| Community | Shared by similar orgs | Multiple orgs, same industry | Government, healthcare |
