# Master Cross-Framework Controls Matrix

**System:** CloudVault Federal Health Exchange (FHX)
**Framework Reference:** FedRAMP High (NIST SP 800-53 Rev. 5), HIPAA Security Rule, SOX ITGC, PCI-DSS v4.0, ISO 27001:2022, Privacy (CCPA/GDPR-aligned)
**Document ID:** FHX-MCM-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault FHX
**Review Cycle:** Annual (aligned to FedRAMP annual assessment cycle)
**Classification:** Internal Use Only

---

## Purpose

The Master Cross-Framework Controls Matrix (MCM) is the central artifact of the CloudVault FHX unified compliance approach. It maps every implemented control across six compliance frameworks against a single operational control implementation, demonstrating where one control satisfies multiple frameworks and where unique requirements exist.

This matrix solves the most persistent problem in multi-framework compliance programs: duplication of effort. Without a unified view, each framework audit produces its own evidence request, its own control testing, and its own documentation. With the MCM, the ISSO can demonstrate to any auditor, for any framework, that the implemented control meets the requirement, with evidence already organized.

The MCM also demonstrates portfolio-level GRC maturity to recruiters and hiring managers: this is not a practitioner who knows one framework. This is a practitioner who can manage an enterprise compliance program spanning federal, healthcare, financial, and privacy frameworks simultaneously.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| FHX-MCM-001.md | This document (matrix overview and usage guide) | Multi-framework | Current |
| mcm-access-control.md | Access control domain matrix across all 6 frameworks | AC family, HIPAA 164.312 | Current |
| mcm-audit-accountability.md | Audit and accountability domain matrix | AU family, HIPAA 164.312(b) | Current |
| mcm-configuration-management.md | Configuration management domain matrix | CM family, SOX CM | Current |
| mcm-incident-response.md | Incident response domain matrix | IR family, HIPAA 164.308(a)(6) | Current |
| mcm-identity-authentication.md | Identity and authentication domain matrix | IA family, PCI Req. 8 | Current |
| mcm-risk-assessment.md | Risk assessment domain matrix | RA family, HIPAA RA | Current |
| mcm-system-communications.md | System and communications protection matrix | SC family, PCI Req. 1-4 | Current |
| mcm-vulnerability-management.md | Vulnerability management cross-framework matrix | RA-5, PCI Req. 6.3 | Current |
| mcm-physical-protection.md | Physical and environmental protection matrix | PE family, PCI Req. 9 | Current |
| mcm-full-consolidated.md | Complete consolidated MCM: all domains, all frameworks | All frameworks | Current |

---

## Master Controls Matrix: Selected Critical Controls

The following table shows a representative sample of the full MCM, focused on the highest-overlap controls. The complete matrix is in mcm-full-consolidated.md.

### Access Control

| FHX Control Implementation | FedRAMP Control | HIPAA Standard | SOX ITGC | PCI-DSS v4.0 | ISO 27001 | Privacy |
|---|---|---|---|---|---|---|
| RBAC with least privilege on all systems | AC-2, AC-3, AC-6 | 164.312(a)(1) | User provisioning controls | Req. 7.2, 7.3 | A.5.15, A.5.18 | Data minimization |
| MFA enforcement on all privileged access | IA-2(1), IA-2(2), AC-17(2) | 164.312(d) | IAM MFA requirement | Req. 8.4, 8.5 | A.5.17 | N/A |
| Quarterly access reviews | AC-2(j), PS-4 | 164.308(a)(3)(ii)(B) | Access certification | Req. 7.2.3 | A.5.18 | Right to erasure process |
| Separation of duties: dev vs. prod | AC-5, CM-5 | 164.308(a)(3)(i) | Segregation of duties | Req. 6.4.2 | A.5.3 | N/A |
| Privileged access management (CyberArk) | AC-2(6), IA-2(5) | 164.312(a)(2)(i) | Privileged access controls | Req. 8.2.2 | A.5.18 | Admin access to PII |

### Audit and Accountability

| FHX Control Implementation | FedRAMP Control | HIPAA Standard | SOX ITGC | PCI-DSS v4.0 | ISO 27001 | Privacy |
|---|---|---|---|---|---|---|
| Centralized SIEM (Splunk ES) covering all systems | AU-2, AU-3, AU-9 | 164.312(b) | Audit trail requirement | Req. 10.2, 10.3 | A.8.15 | Processing activity logging |
| Log retention: 1 year online, 3 years archive | AU-11 | 164.312(b) | Audit evidence retention | Req. 10.7 | A.8.15 | Data retention policy |
| Privileged user activity monitoring | AU-9(4), SI-4(22) | 164.312(b) | Privileged activity logging | Req. 10.2.1.2 | A.8.15 | Admin access to PII records |
| Real-time alerting on critical events | AU-6, SI-4 | 164.308(a)(6)(ii) | Monitoring controls | Req. 10.6 | A.8.16 | Breach detection |
| Log integrity protection (CloudWatch + WORM) | AU-9(3) | 164.312(c)(1) | Audit trail integrity | Req. 10.5 | A.8.15 | N/A |

### Vulnerability Management

| FHX Control Implementation | FedRAMP Control | HIPAA Standard | SOX ITGC | PCI-DSS v4.0 | ISO 27001 | Privacy |
|---|---|---|---|---|---|---|
| Monthly authenticated vulnerability scans (Tenable, Qualys, Inspector) | RA-5, CA-7 | 164.308(a)(1)(ii)(A) | IT risk monitoring | Req. 6.3.3 | A.8.8 | N/A |
| Critical patch within 15 days (FedRAMP SLA) | SI-2, RA-5(5) | 164.308(a)(1)(ii)(B) | Patch management controls | Req. 6.3.3 | A.8.8 | N/A |
| Risk-based remediation prioritization (CVSS + context) | RA-3, RA-5 | 164.308(a)(1)(ii)(A) | IT risk assessment | Req. 6.3.1 | A.8.8 | N/A |
| Monthly FedRAMP ConMon reporting | CA-7, RA-5(6) | 164.308(a)(8) | Periodic monitoring | Req. 12.4.2 | A.5.35 | Privacy impact review |
| Container image scanning at build time | RA-5, CM-7(4) | 164.308(a)(1)(ii)(A) | Change management | Req. 6.4.1 | A.8.8 | N/A |

### Incident Response

| FHX Control Implementation | FedRAMP Control | HIPAA Standard | SOX ITGC | PCI-DSS v4.0 | ISO 27001 | Privacy |
|---|---|---|---|---|---|---|
| Documented IRP with defined roles and timelines | IR-8, IR-1 | 164.308(a)(6)(i) | Incident mgmt controls | Req. 12.10.1 | A.5.24 | Breach response plan |
| SIEM-driven incident detection and alerting | IR-6, SI-4 | 164.308(a)(6)(ii) | Monitoring for incidents | Req. 12.10.7 | A.5.25 | PII breach detection |
| HIPAA breach notification procedure (within 60 days) | IR-6(3) | 164.408, 164.410 | N/A | N/A | A.5.28 | HIPAA and CCPA notification |
| Annual IRP tabletop exercise | IR-3, CP-4 | 164.308(a)(6)(i) | Business continuity testing | Req. 12.10.4 | A.5.26 | Privacy incident testing |
| Forensic evidence preservation procedure | IR-4, AU-9 | 164.312(c)(1) | Audit evidence preservation | Req. 12.10.6 | A.5.27 | Data breach documentation |

### Configuration Management

| FHX Control Implementation | FedRAMP Control | HIPAA Standard | SOX ITGC | PCI-DSS v4.0 | ISO 27001 | Privacy |
|---|---|---|---|---|---|---|
| Hardened AMI baseline (CIS Level 2) | CM-6, CM-7 | 164.312(c)(2) | System hardening standard | Req. 2.2 | A.8.9 | N/A |
| Change management process with CAB approval | CM-3, CM-5 | 164.312(c)(2) | Change management controls | Req. 6.5.2 | A.8.32 | Privacy impact on changes |
| AWS Config conformance packs for continuous compliance | CM-6, CM-7(5) | 164.312(c)(2) | Configuration monitoring | Req. 2.2.1 | A.8.9 | N/A |
| IaC (Terraform) with version control | CM-2, CM-3(1) | 164.312(c)(2) | Change documentation | Req. 6.4.1 | A.8.32 | N/A |
| Software composition analysis in CI/CD | SA-11, RA-5 | 164.308(a)(1)(ii)(A) | Application change controls | Req. 6.3.2 | A.8.29 | Third-party code in PII systems |

---

## MCM Usage Guide for Auditors and Assessors

**For FedRAMP Assessors (ClearPath Security Assessors LLC):**
Navigate to the FedRAMP Control column and use the control identifier to find the row. The row shows which other frameworks the same control satisfies. Evidence for FedRAMP testing will also address HIPAA, PCI, and ISO requirements where the row is populated.

**For HIPAA Auditors:**
Navigate to the HIPAA Standard column using the 45 CFR section reference. Each row shows the specific FHX implementation and the FedRAMP control that serves as the primary evidence reference.

**For SOX External Auditors:**
Navigate to the SOX ITGC column. Each row in that column identifies which FedRAMP controls and technical implementations satisfy the ITGC requirement. Evidence packages are organized by the five SOX domains: RCM, IAM, Change Management, Computer Operations, and Application Controls.

**For PCI-DSS QSA:**
Navigate to the PCI-DSS v4.0 column using the Requirement number. Rows populated in that column show which technical controls and procedures satisfy each sub-requirement.

**For ISO 27001 Internal Auditors:**
Navigate to the ISO 27001 column using the Annex A control reference (A.x.y format). Each row shows the FHX implementation and whether the control is included in the Statement of Applicability.

---

## Control Coverage Statistics

| Framework | Total Requirements | Covered in MCM | Coverage Rate | Gap Analysis |
|---|---|---|---|---|
| FedRAMP High | 421 controls | 421 controls | 100% | No gaps — all controls implemented or accepted |
| HIPAA Security Rule | 54 addressable specifications | 54 specifications | 100% | No gaps — all addressable specs implemented |
| SOX ITGC | 25 control objectives | 25 objectives | 100% | No gaps — all ITGC domains covered |
| PCI-DSS v4.0 | 12 requirements (250+ sub-req) | 12 requirements | 100% | Sub-requirement detail in cloudvault-pci-dss |
| ISO 27001:2022 | 93 Annex A controls | 93 controls | 100% | All applicable controls implemented per SoA |
| Privacy Program | 19 key requirements | 19 requirements | 100% | Full ROPA, DPIA, DSR implementation |

---

## Related Documents

- [Framework Mappings](../framework-mappings/README.md)
- [Executive Summary](../executive-summary/README.md)
- [Portfolio README](../portfolio-readme/README.md)
- [FedRAMP ATO](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)
- [NIST RMF](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/README.md)
- [HIPAA Implementation](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/README.md)
- [SOX ITGC](https://github.com/enechi-njeze/cloudvault-sox-itgc/blob/main/README.md)
- [PCI-DSS](https://github.com/enechi-njeze/cloudvault-pci-dss/blob/main/README.md)
- [ISO 27001](https://github.com/enechi-njeze/cloudvault-iso27001/blob/main/README.md)
- [Privacy Program](https://github.com/enechi-njeze/cloudvault-privacy/blob/main/README.md)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
