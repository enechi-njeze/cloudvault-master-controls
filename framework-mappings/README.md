# Framework Mappings

**System:** CloudVault Federal Health Exchange (FHX)
**Framework Reference:** FedRAMP, HIPAA, SOX ITGC, PCI-DSS v4.0, ISO 27001:2022, Privacy
**Document ID:** FHX-FM-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault FHX
**Review Cycle:** Annual (aligned to FedRAMP annual assessment cycle)
**Classification:** Internal Use Only

---

## Purpose

This folder contains the bilateral framework mapping documents that establish the relationships between each pair of compliance frameworks in the FHX portfolio. These mappings are the analytical foundation for the Master Cross-Framework Controls Matrix in controls-matrix/.

A framework mapping answers a precise question: given that FHX implements Control X under Framework A, which requirements under Framework B does that implementation satisfy? Bilateral mappings document this relationship in both directions for every major control domain.

These mappings are used operationally during audit preparation to assemble evidence packages that satisfy multiple auditors simultaneously. They are also used during annual reviews to identify any divergences introduced by framework updates.

---

## Documents in This Folder

| Document | Description | Coverage | Status |
|---|---|---|---|
| FHX-FM-001.md | This document (mapping program overview) | All frameworks | Current |
| fedramp-hipaa-mapping.md | FedRAMP High to HIPAA Security Rule bilateral mapping | AC, AU, IA, IR, RA families | Current |
| fedramp-sox-mapping.md | FedRAMP High to SOX ITGC bilateral mapping | AC, AU, CM, SI families | Current |
| fedramp-pci-mapping.md | FedRAMP High to PCI-DSS v4.0 bilateral mapping | AC, AU, IA, SC, SI families | Current |
| fedramp-iso27001-mapping.md | FedRAMP High to ISO 27001:2022 bilateral mapping | All 20 control families | Current |
| hipaa-privacy-mapping.md | HIPAA Security Rule to Privacy framework mapping | PHI and PII overlap | Current |
| pci-sox-mapping.md | PCI-DSS v4.0 to SOX ITGC bilateral mapping | IAM, audit, change mgmt | Current |
| nist-csf-mapping.md | NIST CSF v2.0 to FedRAMP High mapping | All 6 CSF functions | Current |

---

## FedRAMP to HIPAA Mapping: Key Relationships

The FedRAMP High baseline and HIPAA Security Rule share a common technical foundation in NIST SP 800-53. The mapping below identifies the primary FedRAMP controls and their HIPAA equivalents across the most critical security domains.

| Domain | FedRAMP Controls | HIPAA Standard | Mapping Strength | Notes |
|---|---|---|---|---|
| Access Control | AC-2, AC-3, AC-6, AC-17 | 164.312(a)(1), 164.312(d) | Direct | RBAC and least privilege satisfy both |
| Audit Controls | AU-2, AU-3, AU-9, AU-11 | 164.312(b) | Direct | SIEM implementation satisfies both |
| Integrity | SI-7, AU-9(3) | 164.312(c)(1), 164.312(c)(2) | Direct | Hash-based integrity verification |
| Transmission Security | SC-8, SC-8(1), IA-3 | 164.312(e)(1), 164.312(e)(2)(ii) | Direct | TLS 1.3 enforcement satisfies both |
| Risk Analysis | RA-3, RA-5 | 164.308(a)(1)(ii)(A) | Direct | NIST SP 800-30 methodology satisfies HIPAA RA |
| Security Management | PM-9, CA-7 | 164.308(a)(1) | Aligned | FedRAMP program management exceeds HIPAA |
| Workforce Training | AT-2, AT-3 | 164.308(a)(5) | Direct | Annual security awareness training |
| Contingency Planning | CP-2, CP-4, CP-9 | 164.308(a)(7) | Direct | BCP/DR documentation |
| Device and Media | MP-2, MP-6, PE-10 | 164.310(d) | Direct | Media sanitization and physical controls |
| Incident Response | IR-8, IR-6(3) | 164.308(a)(6) | Direct | IRP with HIPAA breach notification procedure |

**Divergence Note:** HIPAA does not require continuous monitoring reporting to an external body. FedRAMP's ConMon requirement is more stringent. The FedRAMP ConMon process, however, also satisfies HIPAA's periodic review requirement under 164.308(a)(8).

---

## FedRAMP to ISO 27001 Mapping: Key Relationships

The FedRAMP High baseline (421 controls) and ISO 27001:2022 (93 Annex A controls) represent the two most comprehensive frameworks in the FHX portfolio. The mapping between them covers all 20 NIST SP 800-53 control families and all 4 themes and 11 control categories in ISO 27001 Annex A.

| ISO 27001 Theme | Annex A Controls | Mapped FedRAMP Families | Coverage |
|---|---|---|---|
| Organizational Controls (A.5) | A.5.1-A.5.37 (37 controls) | PM, PL, SA, CA, IR, RA | Comprehensive |
| People Controls (A.6) | A.6.1-A.6.8 (8 controls) | PS, AT | Comprehensive |
| Physical Controls (A.7) | A.7.1-A.7.14 (14 controls) | PE | Comprehensive |
| Technological Controls (A.8) | A.8.1-A.8.34 (34 controls) | AC, AU, CM, IA, SC, SI, RA-5 | Comprehensive |

**Key Equivalencies:**
- ISO A.5.23 (Information Security for Cloud Services) maps to FedRAMP SA-9 and CA-3 (cloud service provider management)
- ISO A.8.8 (Management of Technical Vulnerabilities) maps to FedRAMP RA-5 and SI-2 (vulnerability scanning and patching)
- ISO A.5.24 through A.5.28 (Incident Management) maps to FedRAMP IR family (10 controls)
- ISO A.6.3 (Information Security Awareness Training) maps to FedRAMP AT-2 and AT-3

**Divergence Note:** ISO 27001 requires a formal ISMS with documented scope, leadership commitment, and internal audit program (Clauses 4-10). These clause requirements have no direct FedRAMP equivalents but are satisfied through the FHX security governance program documented in cloudvault-iso27001.

---

## FedRAMP to PCI-DSS Mapping: Key Relationships

PCI-DSS v4.0's 12 requirements address a subset of what FedRAMP High covers, specifically focused on cardholder data protection, network security, and access control. All 12 PCI requirements are satisfied by FedRAMP controls, but not all FedRAMP controls are required by PCI.

| PCI-DSS Requirement | PCI Focus | Mapped FedRAMP Controls | Notes |
|---|---|---|---|
| Req. 1: Network Security Controls | Firewall and network segmentation | SC-7, AC-4, SC-5 | AWS VPC security groups and NACLs |
| Req. 2: Secure Configurations | Default passwords, unnecessary services | CM-6, CM-7, IA-5 | CIS hardened AMIs |
| Req. 3: Protect Stored Data | Encryption of cardholder data at rest | SC-28, SC-28(1) | AES-256 via AWS KMS |
| Req. 4: Protect Data in Transit | Encryption of cardholder data in transit | SC-8, SC-8(1) | TLS 1.3 enforcement |
| Req. 6: Secure Systems and Software | Vulnerability management, patch management | RA-5, SI-2, SA-11 | Monthly scans, 15-day critical patch SLA |
| Req. 7: Restrict Access | Least privilege access to cardholder data | AC-3, AC-6 | RBAC on PCI systems |
| Req. 8: Identify and Authenticate | Strong authentication | IA-2, IA-2(1), IA-5 | MFA, password complexity |
| Req. 9: Restrict Physical Access | Physical access to PCI environments | PE-2, PE-3, PE-6 | AWS GovCloud physical controls (inherited) |
| Req. 10: Log All Access | Audit logging of all access to CDE | AU-2, AU-3, AU-12 | Splunk SIEM centralized logging |
| Req. 11: Test Security Regularly | Penetration testing, vulnerability scanning | CA-8, RA-5 | Annual pen test, monthly scans |
| Req. 12: Support Policies | Security policies and risk management | PL-1, RA-1, CA-5 | Policy suite and POA&M |

---

## FedRAMP to SOX ITGC Mapping: Key Relationships

SOX ITGC focuses on five domains: Change Management, Access Controls, Computer Operations, Program Development, and Monitoring. All five map to specific FedRAMP control families.

| SOX ITGC Domain | Key Controls | Mapped FedRAMP Controls | Notes |
|---|---|---|---|
| Change Management | Change documentation, testing, approval, segregation | CM-3, CM-4, CM-5, CM-9 | CAB process, IaC version control |
| Access Controls | User provisioning, access reviews, privileged access | AC-2, AC-3, AC-5, AC-6 | RBAC, quarterly reviews, PAM |
| Computer Operations | Monitoring, backup, incident management | CP-9, CP-10, IR-8, AU-6 | Automated backups, SIEM, IRP |
| Program Development | SDLC controls, security testing, code review | SA-3, SA-11, SA-15 | Secure SDLC, SAST/DAST |
| Monitoring | Ongoing monitoring, management review | CA-7, AU-6, PM-6 | Monthly ConMon, CISO reporting |

---

## Unified Evidence Architecture

The following table identifies the evidence artifacts that satisfy the highest number of frameworks simultaneously. These are the highest-value evidence items in the FHX compliance portfolio.

| Evidence Artifact | FedRAMP | HIPAA | SOX | PCI-DSS | ISO 27001 | Privacy |
|---|---|---|---|---|---|---|
| SIEM audit log exports | AU-2, AU-3 | 164.312(b) | Audit evidence | Req. 10.3 | A.8.15 | Processing logs |
| Quarterly access review reports | AC-2(j) | 164.308(a)(3)(ii)(B) | Access certification | Req. 7.2.3 | A.5.18 | DSR access review |
| Vulnerability scan reports | RA-5 | 164.308(a)(1)(ii)(A) | IT risk monitoring | Req. 6.3.3 | A.8.8 | N/A |
| Change management tickets (Jira) | CM-3 | 164.312(c)(2) | Change documentation | Req. 6.5.2 | A.8.32 | Privacy-impact changes |
| Monthly ConMon report | CA-7 | 164.308(a)(8) | Ongoing monitoring | Req. 12.4.2 | A.5.35 | Privacy audit |
| Incident response records | IR-5, IR-6 | 164.308(a)(6)(ii) | Incident documentation | Req. 12.10.2 | A.5.27 | Breach notification records |
| Security training records | AT-2, AT-3 | 164.308(a)(5)(ii)(B) | Workforce training | Req. 12.6.1 | A.6.3 | Privacy training |
| Risk assessment report | RA-3 | 164.308(a)(1)(ii)(A) | Risk assessment | Req. 12.3.1 | Clause 6.1.2 | DPIA |

---

## Related Documents

- [Controls Matrix](../controls-matrix/README.md)
- [Executive Summary](../executive-summary/README.md)
- [Portfolio README](../portfolio-readme/README.md)
- [FedRAMP SSP](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)
- [ISO 27001 SoA](https://github.com/enechi-njeze/cloudvault-iso27001/blob/main/README.md)
- [HIPAA Safeguards](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/safeguards/README.md)
- [PCI-DSS Requirements](https://github.com/enechi-njeze/cloudvault-pci-dss/blob/main/requirements/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
