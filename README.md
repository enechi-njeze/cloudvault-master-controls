# CloudVault Master Controls

![Framework](https://img.shields.io/badge/Framework-FedRAMP%20%7C%20HIPAA%20%7C%20SOX%20%7C%20PCI--DSS%20%7C%20ISO%2027001-blue)
![Standard](https://img.shields.io/badge/Standard-Cross--Framework%20Capstone-purple)
![FedRAMP](https://img.shields.io/badge/FedRAMP-High%20421%20Controls-red)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Cert](https://img.shields.io/badge/ISSO-CGRC%20%7C%20CISA%20%7C%20CISM-blue)

**Capstone portfolio repository: unified cross-framework controls matrix for CloudVault Federal Health Exchange (FHX)**

---

## About This Repository

This repository is the capstone of the CloudVault FHX GRC portfolio. It exists to answer one of the most important questions that senior GRC practitioners face in multi-framework environments: when a system must comply with FedRAMP, HIPAA, SOX, PCI-DSS, ISO 27001, and privacy frameworks simultaneously, how do you manage compliance without duplicating effort across every framework?

The answer is unified controls management. This repository demonstrates the ability to map, harmonize, and rationalize controls across frameworks, identify overlap and divergence, and produce integrated evidence that satisfies multiple auditors from a single set of operational controls.

This is graduate-level GRC work. It demonstrates not just knowledge of individual frameworks, but mastery of the underlying control philosophy that makes all of them coherent.

---

## System Overview

**System Name:** CloudVault Federal Health Exchange (FHX)
**System Owner:** Dr. Patricia Owens, Deputy CIO for Health Information Technology
**ISSO / ISSM:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**CISO:** Angela Torres
**Authorizing Official (AO):** Deputy Director Henry Kline
**Privacy Officer:** Sandra Voss
**Cloud Provider:** AWS GovCloud (us-gov-west-1, us-gov-east-1) — FedRAMP High Authorization
**3PAO:** ClearPath Security Assessors LLC
**ATO Status:** Active Authorization — FedRAMP High, FISMA High, HIPAA, SOX, PCI-DSS Level 1

CloudVault FHX is a cloud-hosted federal health information exchange platform serving 47 federal agencies, managing PHI, PII, CUI, FTI, and PCI data for 890,000 or more patients.

---

## Repository Structure

```
cloudvault-master-controls/
├── README.md                     # This file: capstone overview and cross-framework navigation
├── controls-matrix/              # Master cross-framework controls matrix (all frameworks)
├── framework-mappings/           # Bilateral framework mapping documents
├── executive-summary/            # Executive summary of portfolio and compliance posture
├── diagram-library/              # Architecture and compliance diagrams across all repositories
└── portfolio-readme/             # Comprehensive portfolio index and recruiter guide
```

---

## Portfolio Overview: All 10 Repositories

| # | Repository | Framework | Focus | Status |
|---|---|---|---|---|
| 1 | [cloudvault-fedramp-ato](https://github.com/enechi-njeze/cloudvault-fedramp-ato) | FedRAMP High | SSP, ATO, CIS, SAR, SAP, POA&M, 12 SSP attachments | Complete |
| 2 | [cloudvault-nist-rmf](https://github.com/enechi-njeze/cloudvault-nist-rmf) | NIST RMF | All 6 RMF steps: Prepare, Categorize, Select, Assess, Authorize, Monitor | Complete |
| 3 | [cloudvault-iso27001](https://github.com/enechi-njeze/cloudvault-iso27001) | ISO 27001:2022 | ISMS, Annex A controls, risk treatment, SoA, internal audit | Complete |
| 4 | [cloudvault-hipaa](https://github.com/enechi-njeze/cloudvault-hipaa) | HIPAA Security Rule | PHI inventory, safeguards, BAA templates, breach response | Complete |
| 5 | [cloudvault-sox-itgc](https://github.com/enechi-njeze/cloudvault-sox-itgc) | SOX ITGC | RCM, IAM controls, change management, computer operations, app controls | Complete |
| 6 | [cloudvault-pci-dss](https://github.com/enechi-njeze/cloudvault-pci-dss) | PCI-DSS v4.0 | CDE scope, requirements, network segmentation, SAQ | Complete |
| 7 | [cloudvault-privacy](https://github.com/enechi-njeze/cloudvault-privacy) | Privacy / CCPA / GDPR | ROPA, DPIA, data subject rights, DPA templates, breach notification | Complete |
| 8 | [cloudvault-vuln-mgmt](https://github.com/enechi-njeze/cloudvault-vuln-mgmt) | NIST SP 800-40 | Asset inventory, scan reports, risk classification, remediation, metrics | Complete |
| 9 | [cloudvault-risk-governance](https://github.com/enechi-njeze/cloudvault-risk-governance) | NIST SP 800-30 / ISO 31000 | Risk register, scoring model, governance workflows, stakeholder reporting | Complete |
| 10 | **cloudvault-master-controls** | **Cross-Framework Capstone** | **Unified controls matrix, framework mappings, executive summary** | **Active** |

---

## Cross-Framework Control Domains

The following domains represent the major control areas that appear across all frameworks in the FHX compliance portfolio. Each domain contains controls from multiple frameworks that overlap, complement, or sometimes diverge.

| Domain | FedRAMP / NIST 800-53 | HIPAA | SOX ITGC | PCI-DSS v4.0 | ISO 27001:2022 | Privacy |
|---|---|---|---|---|---|---|
| Access Control | AC family (25 controls) | 164.312(a)(1) | IAM controls | Req. 7, 8 | A.5.15-A.5.18 | Data access rights |
| Audit and Accountability | AU family (16 controls) | 164.312(b) | Audit evidence | Req. 10 | A.8.15, A.8.17 | Processing records |
| Configuration Management | CM family (12 controls) | 164.312(b) | Change management | Req. 6, 12 | A.8.8, A.8.9 | Privacy by design |
| Identification and Authentication | IA family (12 controls) | 164.312(d) | IAM controls | Req. 8 | A.5.16, A.5.17 | Identity verification |
| Incident Response | IR family (10 controls) | 164.308(a)(6) | Computer operations | Req. 12.10 | A.5.24-A.5.28 | Breach notification |
| Maintenance | MA family (6 controls) | 164.310(a)(2)(iv) | Change management | Req. 6 | A.5.37 | N/A |
| Media Protection | MP family (9 controls) | 164.310(d) | Computer operations | Req. 3, 9 | A.7.8, A.8.10 | Data retention |
| Physical Protection | PE family (20 controls) | 164.310(a)-(c) | Computer operations | Req. 9 | A.7 (14 controls) | Physical access to PII |
| Planning | PL family (11 controls) | 164.308(a)(7) | RCM documentation | Req. 12 | A.5.1-A.5.4 | Privacy policy |
| Risk Assessment | RA family (10 controls) | 164.308(a)(1) | Management assessment | Req. 12.3 | Clause 6.1 | DPIA requirement |
| System and Communications Protection | SC family (51 controls) | 164.312(e) | Network controls | Req. 1, 2, 4 | A.8.20-A.8.26 | Encryption of PII |
| System and Information Integrity | SI family (23 controls) | 164.312(c) | App controls | Req. 6.3 | A.8.7, A.8.16 | Data accuracy |
| Vulnerability Management | RA-5 and related | 164.308(a)(1) | App controls | Req. 6.3 | A.8.8 | N/A |
| Continuous Monitoring | CA-7 | 164.308(a)(8) | Ongoing monitoring | Req. 12.4 | A.5.35 | Data protection audits |

---

## Key Cross-Framework Mappings

The following pairwise mappings are documented in the framework-mappings/ folder. Each mapping shows which controls from one framework map to controls in another, enabling single-control implementations to satisfy multiple frameworks simultaneously.

| Mapping | Documents | Key Overlaps |
|---|---|---|
| FedRAMP to HIPAA | framework-mappings/fedramp-hipaa-mapping.md | AC-2 maps to 164.312(a)(2)(i); AU-2 maps to 164.312(b); IA-2 maps to 164.312(d) |
| FedRAMP to SOX ITGC | framework-mappings/fedramp-sox-mapping.md | CM-3 maps to change management; AC-2 maps to IAM controls; AU-6 maps to audit evidence |
| FedRAMP to PCI-DSS | framework-mappings/fedramp-pci-mapping.md | AC-3 maps to Req 7; IA-2 maps to Req 8; AU-2 maps to Req 10 |
| FedRAMP to ISO 27001 | framework-mappings/fedramp-iso27001-mapping.md | Extensive overlap: 421 FedRAMP controls map to 93 ISO 27001 Annex A controls |
| HIPAA to Privacy | framework-mappings/hipaa-privacy-mapping.md | PHI overlaps with PII; breach notification aligns with CCPA and GDPR |
| PCI-DSS to SOX | framework-mappings/pci-sox-mapping.md | Req 8 aligns with IAM controls; Req 10 aligns with audit evidence |

---

## Unified Control Evidence Strategy

The unified controls approach means that a single control implementation can produce evidence satisfying multiple frameworks. This section documents the evidence strategy for the highest-overlap control areas.

**Access Control: Single IAM Implementation, Multiple Framework Satisfaction**
FHX implements role-based access control (RBAC) with least privilege, MFA enforcement, and quarterly access reviews. This single implementation satisfies:
- FedRAMP: AC-2 (Account Management), AC-3 (Access Enforcement), AC-17 (Remote Access), IA-2 (Identification and Authentication)
- HIPAA: 164.312(a)(1) (Access Control), 164.312(d) (Person Authentication)
- SOX ITGC: IAM controls (user provisioning, access certification)
- PCI-DSS: Requirement 7 (Restrict Access), Requirement 8 (Strong Authentication)
- ISO 27001: A.5.15 (Access Control), A.5.16 (Identity Management), A.5.18 (Access Rights)

**Audit Logging: Single SIEM Implementation, Multiple Framework Satisfaction**
FHX implements centralized SIEM logging via Splunk Enterprise Security, covering all in-scope systems. This satisfies:
- FedRAMP: AU-2 (Event Logging), AU-3 (Log Content), AU-6 (Audit Review), AU-9 (Audit Information Protection)
- HIPAA: 164.312(b) (Audit Controls)
- SOX ITGC: Audit evidence requirements for IT general controls
- PCI-DSS: Requirement 10 (Log and Monitor All Access)
- ISO 27001: A.8.15 (Logging), A.8.17 (Clock Synchronization)

**Vulnerability Management: Single Program, Multiple Framework Satisfaction**
FHX's vulnerability management program (documented in cloudvault-vuln-mgmt) satisfies:
- FedRAMP: RA-5 (Vulnerability Monitoring and Scanning), CA-7 (Continuous Monitoring)
- HIPAA: 164.308(a)(1) (Risk Analysis) through ongoing technical risk identification
- PCI-DSS: Requirement 6.3 (Security Vulnerabilities are Identified and Addressed)
- ISO 27001: A.8.8 (Management of Technical Vulnerabilities)

---

## Framework Control Counts

| Framework | Total Controls / Requirements | FHX Implementation Level | Assessment Body |
|---|---|---|---|
| FedRAMP High (NIST SP 800-53) | 421 controls, 20 families | Full implementation | ClearPath Security Assessors LLC (3PAO) |
| HIPAA Security Rule | 18 standards, 36 specifications | Full implementation | Internal audit (CISA-qualified ISSO) |
| SOX ITGC | 5 domains, 25 control objectives | Full implementation | Internal audit, external audit support |
| PCI-DSS v4.0 | 12 requirements, 250+ sub-requirements | Full (Level 1 Service Provider) | QSA engagement |
| ISO 27001:2022 | 4 clauses, 93 Annex A controls | Full ISMS implementation | Internal audit |
| Privacy (CCPA, GDPR-aligned) | 7 data subject rights categories, 12 process requirements | Full implementation | Privacy Officer review |
| NIST CSF v2.0 | 6 functions, 23 categories | Aligned implementation | Self-assessment |

---

## Certifications and Competencies

| Certification | Issuing Body | Relevance to Cross-Framework Work |
|---|---|---|
| CGRC (Certified in Governance, Risk and Compliance) | ISC2 | GRC program design, cross-framework harmonization |
| CISA (Certified Information Systems Auditor) | ISACA | Multi-framework audit, controls testing, evidence evaluation |
| CISM (Certified Information Security Manager) | ISACA | Enterprise security governance, cross-framework strategy |
| PMP (Project Management Professional) | PMI | Portfolio management, GRC program delivery |
| PMI-RMP (Risk Management Professional) | PMI | Multi-framework risk methodology |
| CompTIA Security+ SY0-701 | CompTIA | Technical control implementation knowledge |
| CHP (Certified HIPAA Professional) | AAPC | HIPAA-specific controls expertise |
| CSCS (Certified Security Compliance Specialist) | NCSA | Compliance controls validation |
| CISSP (in progress) | ISC2 | Advanced multi-domain security and governance |

---

## Laws, Regulations, and Standards

| Law / Regulation / Standard | Frameworks Covered | Implementation Evidence |
|---|---|---|
| Federal Information Security Modernization Act (FISMA) 2014 | FedRAMP, NIST RMF | ATO, annual assessment, ConMon |
| HIPAA Security Rule (45 CFR 164) | HIPAA, Privacy | Security safeguards, BAA program, breach response |
| Sarbanes-Oxley Act Section 404 | SOX ITGC | RCM, ITGC control testing, audit evidence |
| PCI-DSS v4.0 | PCI-DSS | CDE scope, SAQ, scan results |
| ISO/IEC 27001:2022 | ISO 27001 | ISMS, SoA, internal audit, risk treatment |
| California Consumer Privacy Act (CCPA) | Privacy | CCPA supplement, DSR process |
| GDPR (relevant for international data transfers) | Privacy | DPA templates, DPIA process |
| NIST SP 800-53 Rev. 5 | FedRAMP, NIST RMF | Full 421-control implementation |
| OMB Circular A-130 | FedRAMP, Privacy | Privacy program, federal information lifecycle |
| IRS Publication 1075 | HIPAA, FedRAMP | FTI safeguards, strict access controls |

---

## Related Repositories

| Repository | Role in Portfolio |
|---|---|
| [cloudvault-fedramp-ato](https://github.com/enechi-njeze/cloudvault-fedramp-ato) | Primary authorization package |
| [cloudvault-nist-rmf](https://github.com/enechi-njeze/cloudvault-nist-rmf) | RMF implementation across all six steps |
| [cloudvault-iso27001](https://github.com/enechi-njeze/cloudvault-iso27001) | ISO 27001 ISMS and Annex A controls |
| [cloudvault-hipaa](https://github.com/enechi-njeze/cloudvault-hipaa) | HIPAA Security Rule implementation |
| [cloudvault-sox-itgc](https://github.com/enechi-njeze/cloudvault-sox-itgc) | SOX ITGC control documentation |
| [cloudvault-pci-dss](https://github.com/enechi-njeze/cloudvault-pci-dss) | PCI-DSS v4.0 compliance program |
| [cloudvault-privacy](https://github.com/enechi-njeze/cloudvault-privacy) | Privacy program: ROPA, DPIA, DSR |
| [cloudvault-vuln-mgmt](https://github.com/enechi-njeze/cloudvault-vuln-mgmt) | Vulnerability management program |
| [cloudvault-risk-governance](https://github.com/enechi-njeze/cloudvault-risk-governance) | Enterprise risk register and governance |

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
