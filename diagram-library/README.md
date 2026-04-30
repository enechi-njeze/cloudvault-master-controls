# Portfolio Diagram Library

**System:** CloudVault Federal Health Exchange (FHX)
**Document ID:** FHX-DIAG-LIB-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Review Cycle:** Annual (or upon significant system or governance change)
**Classification:** Internal Use Only

---

## Purpose

This folder serves as the centralized diagram library for the entire CloudVault FHX GRC portfolio. It indexes every process flow diagram, architecture diagram, workflow map, and visual reference across all 10 repositories, providing a single navigation point for auditors, assessors, and stakeholders who need visual documentation.

Visual documentation is not supplementary: it is primary evidence in a mature GRC program. When a FedRAMP assessor needs to understand how vulnerability findings flow from scanner to POA&M, a diagram communicates in seconds what 10 pages of procedure documentation communicates in an hour. This library makes every diagram in the portfolio findable and accessible.

---

## Documents in This Folder

| Document | Description | Status |
|---|---|---|
| FHX-DIAG-LIB-001.md | This document (library index) | Current |
| architecture-overview.md | High-level FHX system architecture on AWS GovCloud | Current |
| governance-program-map.md | GRC program structure: frameworks, repositories, and governance relationships | Current |
| compliance-framework-wheel.md | Visual representation of all 6 frameworks and their overlaps | Current |
| data-flow-diagram.md | Data flow: PHI, PII, CUI, FTI, PCI data movement through FHX | Current |
| authorization-boundary-diagram.md | FedRAMP authorization boundary: in-scope systems and services | Current |

---

## Complete Portfolio Diagram Index

### FedRAMP and NIST RMF Diagrams

| Diagram | Description | Location | Framework |
|---|---|---|---|
| SSP System Architecture | FHX system architecture with AWS GovCloud components | [cloudvault-fedramp-ato/ssp-attachments](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/ssp-attachments/README.md) | FedRAMP |
| Authorization Boundary | Defined authorization boundary with system components | [cloudvault-fedramp-ato/ssp-attachments](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/ssp-attachments/README.md) | FedRAMP |
| Data Flow Diagram | PHI, PII, CUI, FTI, PCI data flow through FHX | [cloudvault-fedramp-ato/ssp-attachments](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/ssp-attachments/README.md) | FedRAMP |
| Network Architecture | AWS GovCloud VPC topology, security groups, NACLs | [cloudvault-fedramp-ato/ssp-attachments](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/ssp-attachments/README.md) | FedRAMP |
| RMF Step 1-6 Workflow | NIST RMF implementation process flow for FHX | [cloudvault-nist-rmf](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/README.md) | NIST RMF |
| ConMon Reporting Flow | Monthly continuous monitoring report generation workflow | [cloudvault-nist-rmf/step6-monitor](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/step6-monitor/README.md) | NIST RMF |

---

### ISO 27001 Diagrams

| Diagram | Description | Location | Framework |
|---|---|---|---|
| ISMS Scope Map | Information Security Management System scope boundaries | [cloudvault-iso27001/isms-scope](https://github.com/enechi-njeze/cloudvault-iso27001/blob/main/README.md) | ISO 27001 |
| Risk Treatment Flow | ISO 31000 risk treatment lifecycle diagram | [cloudvault-iso27001](https://github.com/enechi-njeze/cloudvault-iso27001/blob/main/README.md) | ISO 27001 |
| Annex A Control Map | Visual mapping of 93 Annex A controls to FHX domains | [cloudvault-iso27001](https://github.com/enechi-njeze/cloudvault-iso27001/blob/main/README.md) | ISO 27001 |

---

### HIPAA Diagrams

| Diagram | Description | Location | Framework |
|---|---|---|---|
| PHI Data Flow | PHI data ingestion, processing, storage, and transmission flows | [cloudvault-hipaa/diagrams](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/diagrams/README.md) | HIPAA |
| BAA Network | Business Associate Agreement network across 47 agencies | [cloudvault-hipaa/baa-templates](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/baa-templates/README.md) | HIPAA |
| Breach Response Workflow | HIPAA breach detection, notification, and remediation flow | [cloudvault-hipaa/breach-response](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/breach-response/README.md) | HIPAA |

---

### SOX ITGC Diagrams

| Diagram | Description | Location | Framework |
|---|---|---|---|
| ITGC Control Domains | Five SOX ITGC domains and their relationships | [cloudvault-sox-itgc/diagrams](https://github.com/enechi-njeze/cloudvault-sox-itgc/blob/main/diagrams/README.md) | SOX |
| Change Management Flow | IT change lifecycle: request through CAB approval to deployment | [cloudvault-sox-itgc/change-management](https://github.com/enechi-njeze/cloudvault-sox-itgc/blob/main/change-management/README.md) | SOX |
| IAM Lifecycle Diagram | User provisioning, access review, and deprovisioning workflow | [cloudvault-sox-itgc/iam-controls](https://github.com/enechi-njeze/cloudvault-sox-itgc/blob/main/iam-controls/README.md) | SOX |

---

### PCI-DSS Diagrams

| Diagram | Description | Location | Framework |
|---|---|---|---|
| CDE Network Topology | Cardholder Data Environment network segmentation diagram | [cloudvault-pci-dss/diagrams](https://github.com/enechi-njeze/cloudvault-pci-dss/blob/main/diagrams/README.md) | PCI-DSS |
| CDE Scope Boundary | Systems and components in scope for PCI-DSS | [cloudvault-pci-dss/cde-scope](https://github.com/enechi-njeze/cloudvault-pci-dss/blob/main/cde-scope/README.md) | PCI-DSS |
| Network Segmentation Diagram | Isolation of CDE from non-CDE systems | [cloudvault-pci-dss/network-segmentation](https://github.com/enechi-njeze/cloudvault-pci-dss/blob/main/network-segmentation/README.md) | PCI-DSS |

---

### Privacy Diagrams

| Diagram | Description | Location | Framework |
|---|---|---|---|
| Data Flow Map (Privacy) | PII data flows mapped to ROPA categories | [cloudvault-privacy/ropa](https://github.com/enechi-njeze/cloudvault-privacy/blob/main/ropa/README.md) | Privacy |
| DPIA Process Flow | Data Protection Impact Assessment workflow | [cloudvault-privacy/dpia](https://github.com/enechi-njeze/cloudvault-privacy/blob/main/dpia/README.md) | Privacy |
| DSR Workflow | Data Subject Request intake, processing, and response flow | [cloudvault-privacy/data-subject-rights](https://github.com/enechi-njeze/cloudvault-privacy/blob/main/data-subject-rights/README.md) | Privacy |

---

### Vulnerability Management Diagrams

| Diagram | Description | Location | Framework |
|---|---|---|---|
| Vulnerability Lifecycle Flow | End-to-end: discovery, triage, remediation, verification | [cloudvault-vuln-mgmt/diagrams](https://github.com/enechi-njeze/cloudvault-vuln-mgmt/blob/main/diagrams/README.md) | NIST SP 800-40 |
| Scan Architecture | Multi-tool scanning architecture in AWS GovCloud | [cloudvault-vuln-mgmt/diagrams](https://github.com/enechi-njeze/cloudvault-vuln-mgmt/blob/main/diagrams/README.md) | NIST SP 800-40 |
| Remediation Workflow | Triage to assignment to verification workflow | [cloudvault-vuln-mgmt/diagrams](https://github.com/enechi-njeze/cloudvault-vuln-mgmt/blob/main/diagrams/README.md) | NIST SP 800-40 |
| ConMon Reporting Flow | Monthly ConMon report production and submission | [cloudvault-vuln-mgmt/diagrams](https://github.com/enechi-njeze/cloudvault-vuln-mgmt/blob/main/diagrams/README.md) | FedRAMP |

---

### Risk Governance Diagrams

| Diagram | Description | Location | Framework |
|---|---|---|---|
| Three-Tier Risk Architecture | NIST SP 800-39 Tier 1-3 governance structure | [cloudvault-risk-governance/diagrams](https://github.com/enechi-njeze/cloudvault-risk-governance/blob/main/diagrams/README.md) | NIST SP 800-39 |
| Risk Lifecycle Flow | Risk identification through closure | [cloudvault-risk-governance/diagrams](https://github.com/enechi-njeze/cloudvault-risk-governance/blob/main/diagrams/README.md) | NIST SP 800-30 |
| RGC Committee Structure | Risk Governance Committee membership and authority | [cloudvault-risk-governance/diagrams](https://github.com/enechi-njeze/cloudvault-risk-governance/blob/main/diagrams/README.md) | FHX Governance |
| Risk Escalation Flow | Escalation paths for High and Very High risks | [cloudvault-risk-governance/diagrams](https://github.com/enechi-njeze/cloudvault-risk-governance/blob/main/diagrams/README.md) | FHX Governance |

---

## FHX System Architecture Overview

CloudVault FHX operates entirely within AWS GovCloud (us-gov-west-1 and us-gov-east-1) under a FedRAMP High Authorization. The architecture is designed for multi-region availability, strict data isolation, and defense-in-depth security.

**Compute Tier:**
EC2 instances run the core FHX application workloads, deployed across multiple Availability Zones within the FedRAMP authorization boundary. All instances use hardened Amazon Machine Images (CIS Level 2 benchmark) with no public IP addresses. Systems Manager (SSM) handles patching and operational management without requiring SSH or RDP access.

**Data Tier:**
RDS PostgreSQL instances store structured health and enrollment data. S3 provides object storage for documents and backups. All data at rest is encrypted using AES-256 through AWS KMS with customer-managed keys (CMKs). Data in transit uses TLS 1.3 enforced at all layers.

**Network Tier:**
A multi-layered network security approach uses VPC security groups as the primary host-based firewall, Network ACLs for subnet-level control, and AWS Network Firewall at the VPC perimeter. No direct internet ingress is permitted. All inbound traffic flows through AWS WAF and CloudFront (for agency-facing endpoints).

**Identity and Access:**
AWS IAM with RBAC and least privilege across all accounts in the FHX AWS Organization. AWS Single Sign-On (SSO) with MFA enforcement for all human access. CyberArk PAM (in deployment as of Q3 2025) for privileged access management. Service accounts use IAM roles with no long-term credentials.

**Security Operations:**
Amazon Inspector (continuous) and Tenable Nessus (monthly authenticated) for vulnerability management. Qualys VMDR agents on all application workloads. Splunk Enterprise Security as the centralized SIEM, receiving logs from all CloudTrail, VPC Flow Logs, S3 access logs, and application logs. AWS Security Hub as the aggregation point for GuardDuty, Inspector, Config, and Macie findings.

---

## Related Documents

- [Controls Matrix](../controls-matrix/README.md)
- [Framework Mappings](../framework-mappings/README.md)
- [Executive Summary](../executive-summary/README.md)
- [Portfolio README](../portfolio-readme/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
