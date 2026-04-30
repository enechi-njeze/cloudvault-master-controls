# Executive Summary: CloudVault FHX GRC Portfolio

**System:** CloudVault Federal Health Exchange (FHX)
**Document ID:** FHX-EXEC-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Audience:** Authorizing Official, CISO, System Owner, Executive Leadership, Hiring Managers and Recruiters
**Classification:** Internal Use Only (Public Portfolio Version)

---

## Portfolio Overview

This portfolio documents the complete information security and privacy governance program for the CloudVault Federal Health Exchange (FHX), a cloud-hosted federal health information exchange platform built on AWS GovCloud. FHX serves 47 federal agencies and manages health enrollment, benefits administration, and clinical data exchange for more than 890,000 patients.

The portfolio spans 10 GitHub repositories covering every major aspect of a mature, multi-framework GRC program: federal authorization, risk management, vulnerability management, compliance frameworks, privacy governance, and enterprise risk governance. All work was designed, implemented, and documented by Enechi P.C. Njeze in the role of ISSO and ISSM.

---

## System Profile

| Attribute | Detail |
|---|---|
| System Name | CloudVault Federal Health Exchange (FHX) |
| System Owner | Dr. Patricia Owens, Deputy CIO for Health IT |
| ISSO / ISSM | Enechi P.C. Njeze |
| CISO | Angela Torres |
| Authorizing Official | Deputy Director Henry Kline |
| Privacy Officer | Sandra Voss |
| DevOps Lead | Trevor L. Abrams |
| 3PAO | ClearPath Security Assessors LLC |
| Cloud Platform | AWS GovCloud (us-gov-west-1, us-gov-east-1) |
| Authorization Level | FedRAMP High, FISMA High |
| Data Types | PHI, PII, CUI, FTI, PCI |
| Agencies Served | 47 federal agencies |
| Patients Covered | 890,000+ |

---

## Authorization and Compliance Status

| Framework | Authorization Status | Last Assessment | Next Assessment |
|---|---|---|---|
| FedRAMP High | Active ATO | Q2 2025 (3PAO annual assessment) | Q2 2026 |
| FISMA High | Current | Annual (FY 2025) | FY 2026 |
| HIPAA Security Rule | Compliant | Quarterly internal review | Q3 2025 |
| SOX ITGC | Compliant | FY 2024 external audit | FY 2025 |
| PCI-DSS v4.0 (Level 1) | Compliant | Q1 2025 SAQ / QSA review | Q1 2026 |
| ISO 27001:2022 | Aligned (not certified) | Annual internal audit | Q4 2025 |
| Privacy (CCPA/GDPR-aligned) | Compliant | Quarterly | Q3 2025 |

---

## Risk Posture Summary

As of Q2 2025, the CloudVault FHX risk posture is Moderate. There are no Very High risks. Two High risks are under active treatment with approved corrective action plans. The FedRAMP ATO is maintained in good standing with no unresolved findings from the most recent 3PAO assessment.

| Metric | Q2 2025 Value | Target | Status |
|---|---|---|---|
| Open Risk Register Items | 12 | Below 15 | On Target |
| Very High Risks | 0 | 0 | On Target |
| High Risks | 2 | Below 3 | On Target |
| Open POA&M Items | 12 | Below 20 | On Target |
| Overdue POA&M Items | 0 | 0 | On Target |
| Scan Coverage Rate | 99.7% | 98% minimum | Exceeding Target |
| Critical MTTR | 10 days | 12 days (SLA: 15) | Exceeding Target |
| SLA Compliance Overall | 96% | 95% | On Target |
| ATO Status | Active | Maintained | On Target |

---

## What This Portfolio Demonstrates

This portfolio demonstrates professional competency across every dimension of senior GRC practice. The competencies below map directly to the most common requirements found in ISSO, ISSM, GRC Manager, and Security Compliance Lead job descriptions.

**Federal Compliance Program Management:**
End-to-end FedRAMP High authorization, from system categorization through SSP development, 3PAO assessment coordination, and ATO maintenance. All six NIST RMF steps are documented with real-world artifacts including SSP attachments, security assessment plans, and POA&M registers.

**Multi-Framework Compliance:**
Simultaneous management of FedRAMP, HIPAA, SOX ITGC, PCI-DSS, ISO 27001, and privacy requirements for a single system. This is not a collection of standalone compliance programs: it is an integrated, unified compliance architecture where one control implementation satisfies multiple frameworks.

**Risk Management:**
Full enterprise risk governance program including a scored risk register with 12 entries, a documented risk scoring methodology aligned to NIST SP 800-30, quarterly AO risk briefings, and corrective action plans with milestone tracking and POA&M linkage.

**Vulnerability Management:**
End-to-end vulnerability management program including asset inventory, multi-tool scanning (Tenable, Inspector, Qualys), risk-based triage, remediation tracking, SLA performance reporting, and FedRAMP continuous monitoring integration.

**Privacy Governance:**
Comprehensive privacy program covering GDPR-aligned ROPA, DPIA methodology, data subject rights workflows, data processing agreements, HIPAA breach notification, and CCPA supplemental compliance. Privacy Officer coordination integrated throughout.

**Technical Writing and Documentation:**
All 10 repositories are populated with professional-grade documentation that a real 3PAO, external auditor, or AO could use as primary evidence. Documents follow federal format conventions, cite specific regulatory references, and avoid generic placeholder content.

---

## Portfolio Repository Index

| Repository | Framework | Content Summary | Link |
|---|---|---|---|
| cloudvault-fedramp-ato | FedRAMP High | SSP, ATO, SAP, SAR, CIS, POA&M, 12 SSP attachments | [Link](https://github.com/enechi-njeze/cloudvault-fedramp-ato) |
| cloudvault-nist-rmf | NIST RMF | All 6 RMF steps with full documentation | [Link](https://github.com/enechi-njeze/cloudvault-nist-rmf) |
| cloudvault-iso27001 | ISO 27001:2022 | ISMS, Annex A, SoA, risk treatment, internal audit | [Link](https://github.com/enechi-njeze/cloudvault-iso27001) |
| cloudvault-hipaa | HIPAA Security Rule | PHI inventory, safeguards, BAA, breach response | [Link](https://github.com/enechi-njeze/cloudvault-hipaa) |
| cloudvault-sox-itgc | SOX ITGC | RCM, IAM, change mgmt, computer ops, app controls | [Link](https://github.com/enechi-njeze/cloudvault-sox-itgc) |
| cloudvault-pci-dss | PCI-DSS v4.0 | CDE scope, requirements, network segmentation, SAQ | [Link](https://github.com/enechi-njeze/cloudvault-pci-dss) |
| cloudvault-privacy | Privacy / CCPA / GDPR | ROPA, DPIA, DSR, DPA templates, breach notification | [Link](https://github.com/enechi-njeze/cloudvault-privacy) |
| cloudvault-vuln-mgmt | NIST SP 800-40 | Asset inventory, scans, remediation, metrics | [Link](https://github.com/enechi-njeze/cloudvault-vuln-mgmt) |
| cloudvault-risk-governance | NIST SP 800-30 / ISO 31000 | Risk register, scoring, workflows, reporting | [Link](https://github.com/enechi-njeze/cloudvault-risk-governance) |
| cloudvault-master-controls | Cross-Framework Capstone | Unified controls matrix, mappings, executive summary | [Link](https://github.com/enechi-njeze/cloudvault-master-controls) |

---

## Professional Background: Enechi P.C. Njeze

Enechi P.C. Njeze is a senior cybersecurity GRC professional with more than 11 years of experience in information security, risk management, and compliance. His expertise spans federal government cybersecurity (FedRAMP, FISMA, NIST RMF), healthcare compliance (HIPAA, CMS), financial services controls (SOX, PCI-DSS), privacy frameworks (CCPA, GDPR-aligned), and enterprise risk governance.

He holds the following active certifications, each demonstrating a specific domain of GRC competency:

| Certification | Issuing Body | Domain |
|---|---|---|
| CGRC (Certified in Governance, Risk and Compliance) | ISC2 | Federal GRC, authorization, continuous monitoring |
| CISA (Certified Information Systems Auditor) | ISACA | IT audit, controls testing, risk-based audit |
| CISM (Certified Information Security Manager) | ISACA | Security management, governance, incident response |
| PMP (Project Management Professional) | PMI | Program management, delivery, stakeholder communication |
| PMI-RMP (Risk Management Professional) | PMI | Risk methodology, risk governance, treatment planning |
| CompTIA Security+ SY0-701 | CompTIA | Technical security foundations |
| CHP (Certified HIPAA Professional) | AAPC | HIPAA compliance, PHI protection, breach response |
| CSCS (Certified Security Compliance Specialist) | NCSA | Compliance program management, controls validation |
| CISSP (in progress) | ISC2 | Advanced security management and architecture |

---

## Contact and Portfolio Links

**LinkedIn:** [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
**GitHub Portfolio:** [github.com/enechi-njeze](https://github.com/enechi-njeze)

---

*Prepared by:* **Enechi P.C. Njeze**, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)
*Role:* ISSO / ISSM, CloudVault Federal Health Exchange
*LinkedIn:* [linkedin.com/in/enechi-njeze](https://linkedin.com/in/enechi-njeze)
*Portfolio:* [github.com/enechi-njeze](https://github.com/enechi-njeze)
