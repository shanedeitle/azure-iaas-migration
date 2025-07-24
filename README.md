
# Cloud Security Implementation Plan – Azure IaaS

## Overview
This project documents a secure cloud migration plan for a nationwide enterprise transitioning from leased data centers to Microsoft Azure. The implementation prioritizes regulatory compliance, data security, and departmental isolation while leveraging Infrastructure-as-a-Service (IaaS).

## Executive Summary
SWBTL LLC, a nationwide enterprise, is migrating its operations to Microsoft Azure to meet security, compliance, and scalability demands. The plan addresses FISMA and PCI DSS requirements, enforces encryption at rest and in transit, and implements resource group and Key Vault segregation to ensure least privilege access.

## Cloud Service Model
- **Model:** Infrastructure as a Service (IaaS)  
- **Compliance:** Federal Information Security Modernization Act (FISMA) & Payment Card Industry Data Security Standard (PCI DSS)  
- **Benefits:** Granular control, scalability, customizable security  
- **Challenges:** Requires vigilant configuration management and continuous monitoring

## Role-Based Access Control (RBAC)
**Recommendations Implemented:**
1. Reassigned Key Vaults to correct Resource Groups for departmental isolation.
2. Applied department-specific Key Vault Contributor roles to enforce least privilege.
3. Implemented Tag Contributor roles to facilitate resource management per department.

## Azure Key Vault Best Practices
**Implemented:**
- Private Endpoints for secure connections.
- Key rotation and versioning policies for encryption management.

**Encryption:**  
- TLS/SSL for secure communication (data in transit).  
- Azure Disk Encryption for virtual machines (data at rest).  

## Backup & Recovery
- **Backup Policy:** Daily backups with a 45-day retention window.  
- **Recovery Point Objective (RPO):** 1 day  
- **Recovery Time Objective (RTO):** 36 hours  

## Shared Responsibility Model
- **Company Responsibilities:** IAM, encryption management, OS/app security, and custom application configurations.
- **Azure Responsibilities:** Physical infrastructure, hypervisor management, and security of platform services.
- **Shared:** Compliance, monitoring, incident detection, and response.

## Threats & Mitigation
1. **Unauthorized Access:** Mitigated using Multi-Factor Authentication (MFA), RBAC audits, and Azure Identity Protection.
2. **Data Breach:** Secured with TLS, Azure Private Link, and disk encryption.
3. **Backup Failures:** Addressed via testing backup procedures and implementing geo-redundant storage.

## Lessons Learned
- Regulatory compliance must drive cloud architecture design.
- Least privilege principles significantly reduce cross-departmental risks.
- Ongoing monitoring and audits are essential for sustaining a secure cloud environment.

---
*This project demonstrates enterprise-level cloud security planning and implementation using Microsoft Azure IaaS.*
