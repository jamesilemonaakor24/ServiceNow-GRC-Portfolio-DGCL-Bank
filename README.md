# ServiceNow GRC Portfolio - DGCL Bank

A hands-on **Governance, Risk and Compliance (GRC)** portfolio built in a **ServiceNow Personal Developer Instance (PDI)**. Across three connected case studies, I used ServiceNow to structure risk, assess third parties, test controls, manage findings and remediation, and present management-level GRC metrics.

> **Portfolio disclaimer**
>
> **DGCL Bank is a fictional organisation used solely for this independent ServiceNow GRC case study. It is not a real financial institution and does not represent Digital Cloud Academy, its clients, systems, or any production environment. All organisations, risks, controls, findings and remediation activities shown here are simulated for educational and portfolio purposes.**

---

## Portfolio at a glance

This repository demonstrates how I move from a GRC scenario to a traceable workflow inside ServiceNow rather than treating risk, compliance and audit as separate spreadsheet exercises.

| Area | What I demonstrated |
|---|---|
| Enterprise Risk Management | Risk identification, entity scoping, inherent/residual assessment, treatment selection, mitigation ownership and monitoring |
| Third-Party Risk Management | Vendor onboarding, engagement scoping, security questionnaire, assessment, issue creation, vendor remediation and internal review |
| Governance, Compliance & Audit | Audit engagement, risk/control linkage, control testing, finding management, remediation, approval and closure |
| Executive Reporting | Management dashboard covering audit completion, high-priority findings, ineffective control tests and completed remediation |

### Selected outcomes

- Assessed an unauthorised-access risk from **4 - High inherent risk** to **2 - Low residual risk**
- Managed a **CloudPay Technologies** third-party security assessment through issue and remediation workflow
- Tested privileged-access MFA across **20 accounts**, with **18 compliant and 2 exceptions**
- Raised a **Priority 2 - High** audit finding and tracked remediation to closure
- Completed the audit engagement with **100% fieldwork**
- Built a four-metric **ServiceNow Platform Analytics** executive GRC dashboard

### Environment and tools

- ServiceNow Personal Developer Instance (PDI)
- ServiceNow GRC / Integrated Risk Management capabilities
- Risk Management
- Third-Party Risk / Vendor Risk workflows
- Audit Management
- Controls, test plans and control tests
- Issue and remediation workflows
- Platform Analytics dashboards

---

# Project 1 - Enterprise Risk Management

## Scenario

DGCL Bank's fictional **Digital Banking Service** was assessed for the risk of **unauthorised access to digital banking services**. The scenario considered compromised customer or privileged-user credentials that could result in fraudulent transactions, exposure of customer information and service disruption.

## What I implemented

I linked the risk to the **DGCL Bank - Digital Banking Service** entity, assessed inherent and residual exposure, selected **Mitigate** as the treatment response, and tracked an MFA-focused mitigation through closure.

The risk was then placed in **Monitor** rather than retired because the control reduced the exposure without removing the underlying access risk.

### Risk assessment outcome

| Measure | Result |
|---|---:|
| Inherent impact | 4 - High |
| Inherent likelihood | 5 - Extremely Likely |
| Inherent ALE | $20,000,000 |
| Inherent risk score | 4 - High |
| Residual impact | 3 - Moderate |
| Residual likelihood | 2 - Unlikely |
| Residual ALE | $4,000,000 |
| Residual risk score | 2 - Low |
| Treatment | Mitigate |
| Final risk posture | Monitor |

The mitigation focused on enforcing **Multi-Factor Authentication (MFA)** for privileged and administrative access and reviewing privileged accounts.

### Evidence

![DGCL Bank entity linked into the GRC workflow](images/01-enterprise-risk-management/01-dgcl-digital-banking-entity-linked.png)

*The Digital Banking Service entity provides the business context for the risk and is reused later in the audit workflow.*

![Unauthorised-access risk linked to the entity](images/01-enterprise-risk-management/02-unauthorized-access-risk-linked.png)

*The unauthorised-access risk is linked to the Digital Banking Service, supporting traceability between the business service, risk and later assurance activity.*

![Closed MFA risk mitigation](images/01-enterprise-risk-management/03-mfa-risk-mitigation-closed.png)

*The MFA-focused mitigation reached Closed Complete with defined assignment and review ownership.*

### What this demonstrates

- Translating a business scenario into a structured risk record
- Scoping risk to a specific business service/entity
- Distinguishing inherent from residual risk
- Selecting and documenting a risk treatment
- Assigning mitigation ownership and review responsibility
- Monitoring residual exposure after mitigation
- Reusing the same risk context during later audit activity

---

# Project 2 - Third-Party Risk Management: CloudPay Technologies

## Scenario

DGCL Bank considered **CloudPay Technologies** for an online payment-processing service. Because the engagement could affect customer and transaction-related information, I used ServiceNow to structure a pre-onboarding third-party security assessment.

## What I implemented

I created the vendor profile and engagement, configured a vendor-security questionnaire, launched an external assessment, reviewed the vendor response, raised an MFA-related third-party risk issue, captured the vendor's remediation response, and completed internal review of the corrective action.

The key exception was **partial MFA coverage for privileged accounts**. Instead of treating the questionnaire as the end of the assessment, the exception became a trackable issue with ownership, recommendation, remediation and review.

### Assessment outcome

- Vendor: **CloudPay Technologies**
- Engagement: **CloudPay Online Payment Processing Service**
- Third-party tier: **2 - High**
- Finding: **Incomplete MFA Coverage for Privileged Accounts**
- Finding priority observed in the lab: **4 - Low**
- Final engagement risk rating observed: **4 - Low**

The final rating reflects the configured ServiceNow assessment used in this case study.

### Core evidence

![CloudPay vendor profile](images/02-third-party-risk/01-cloudpay-vendor-profile.jpg)

*CloudPay is established as a third party with ownership and tiering information inside the GRC platform.*

![External assessment created](images/02-third-party-risk/05-external-assessment-created.jpg)

*The assessment is linked to the vendor and the specific payment-processing engagement.*

![Assessment submitted to third party](images/02-third-party-risk/06-assessment-submitted-to-third-party.jpg)

*The assessment moves from Draft into the formal third-party response workflow.*

![Vendor portal questionnaire](images/02-third-party-risk/07-cloudpay-vendor-portal-questionnaire.jpg)

*CloudPay receives the security questionnaire through the third-party portal.*

![MFA coverage issue](images/02-third-party-risk/08-mfa-coverage-risk-issue.jpg)

*Partial privileged-account MFA coverage is converted into a formal third-party risk issue.*

![Vendor remediation response](images/02-third-party-risk/09-vendor-remediation-response.jpg)

*The vendor records corrective action for review.*

![Internal review](images/02-third-party-risk/10-internal-review-of-vendor-finding.jpg)

*The internal review step preserves independent oversight rather than allowing the vendor to self-close the issue.*

![Final engagement risk rating](images/02-third-party-risk/12-final-engagement-risk-rating.jpg)

*The resulting engagement-level risk rating is visible after the assessment workflow.*

<details>
<summary><strong>Additional third-party risk evidence</strong></summary>

### Engagement and contact relationship

![CloudPay engagement and contact](images/02-third-party-risk/02-cloudpay-engagement-and-contact.jpg)

### Vendor security questionnaire template

![Vendor security questionnaire](images/02-third-party-risk/03-vendor-security-questionnaire-template.jpg)

### Assessment-question scoring design

![Questionnaire scoring design](images/02-third-party-risk/04-questionnaire-scoring-design.jpg)

### Closed issue visible in engagement workflow

![Vendor issue closure list](images/02-third-party-risk/11-vendor-issue-closure-list.jpg)

</details>

### What this demonstrates

- Third-party/vendor onboarding and engagement scoping
- Security-questionnaire design and assessment workflow
- Converting vendor exceptions into formal findings
- Assigning ownership and remediation expectations
- Tracking vendor corrective action
- Separating vendor response from internal review
- Maintaining an auditable third-party risk trail

---

# Project 3 - Governance, Compliance & Audit: Privileged Access MFA

## Audit objective

The **DGCL Bank Privileged Access Compliance Audit** assessed whether privileged and administrative accounts supporting the Digital Banking Service were properly authorised, reviewed and protected with MFA.

The audit reused the existing entity and risk, then introduced a dedicated control and test plan. This created a traceable chain from:

**Business Service -> Risk -> Control -> Control Test -> Finding -> Remediation -> Approval -> Closure**

## Audit roles

| Role | ServiceNow user |
|---|---|
| Engagement lead | DGCL Audit Manager |
| Auditor | DGCL Internal Auditor |
| Approver | System Administrator |
| Remediation owner | System Administrator |

## Control test result

The operating test reviewed **20 privileged and administrative accounts**:

- **18** had MFA correctly enabled
- **2** did not have MFA enabled
- Operating effectiveness was assessed as **Ineffective**
- A **Priority 2 - High** finding was raised
- A remediation task was assigned to the System Administrator
- MFA was enabled on the two non-compliant accounts and the population was reviewed
- The finding moved through review and the engagement reached **Closed Complete**

### Core evidence

![Audit engagement validation](images/03-audit-compliance/01-audit-engagement-validate.png)

*The engagement shows defined lead, auditor and approver roles together with its audit purpose and objectives.*

![Privileged Access MFA control](images/03-audit-compliance/02-privileged-access-mfa-control.png)

*The control formalises the MFA requirement for privileged and administrative access to the Digital Banking Service.*

![MFA control test plan](images/03-audit-compliance/04-mfa-control-test-plan.png)

*The test plan defines how the control will be assessed before fieldwork begins.*

![Generated control test](images/03-audit-compliance/05-generated-control-test.png)

*The generated test is linked to the engagement, control and test plan and assigned to the internal auditor.*

![High-priority MFA finding](images/03-audit-compliance/07-high-priority-mfa-finding.png)

*The finding documents the 20-account sample, 18 compliant accounts and two MFA exceptions with Priority 2 - High.*

![Finding recommendation and control relationship](images/03-audit-compliance/08-finding-recommendation-and-control-link.png)

*The finding remains traceable to the control/risk context and records the recommended corrective action.*

![Remediation task](images/03-audit-compliance/09-remediation-task-created.png)

*Corrective action becomes an owned remediation task rather than an informal recommendation.*

![Remediation evidence](images/03-audit-compliance/10-remediation-work-notes.png)

*Work notes document completion of MFA remediation and review of the privileged-account population.*

![Finding response](images/03-audit-compliance/11-finding-response-remediate.png)

*The issue response records remediation and submission for verification before closure.*

![Closed audit engagement](images/03-audit-compliance/14-audit-engagement-closed-complete.png)

*The engagement reached Closed Complete with fieldwork at 100% after remediation and approval.*

<details>
<summary><strong>Additional audit evidence</strong></summary>

### Control linked into the engagement

![Control linked to engagement](images/03-audit-compliance/03-control-linked-to-engagement.png)

### Operating-test procedure

![Operating test procedure](images/03-audit-compliance/06-operation-test-procedure.png)

### Finding at Review stage

![Finding review](images/03-audit-compliance/12-finding-review.png)

### Engagement at 100% awaiting approval

![Engagement awaiting approval](images/03-audit-compliance/13-engagement-awaiting-approval-100-percent.png)

</details>

### What this demonstrates

- Risk-based audit scoping
- Entity, risk and control relationship management
- Control design and operating-effectiveness testing
- Sampling and exception documentation
- Audit finding creation and prioritisation
- Remediation ownership and evidence capture
- Independent review before closure
- Approval workflow and audit completion
- Separation of audit, management and remediation responsibilities

---

# Executive GRC Dashboard

The final stage turned individual GRC records into a management view using **ServiceNow Platform Analytics**.

| Management indicator | Result |
|---|---:|
| Completed Audit Engagements | 1 |
| High-Priority Audit Issues Identified | 1 |
| Ineffective Control Tests Identified | 1 |
| Completed Remediation Tasks | 1 |

![Final DGCL Bank GRC Executive Dashboard](images/04-executive-dashboard/03-final-grc-executive-dashboard.png)

*The dashboard gives management a concise view of audit completion, material findings, control-test effectiveness and remediation progress.*

<details>
<summary><strong>Dashboard build evidence</strong></summary>

### Dashboard definition

![Dashboard created](images/04-executive-dashboard/01-dashboard-created.png)

### Audit engagement table used as a data source

![Engagement data source](images/04-executive-dashboard/02-engagement-data-source.png)

</details>

---

# GRC capabilities demonstrated across the portfolio

This case study shows practical understanding of several activities commonly expected in GRC, Technology Risk, IT Audit and Cybersecurity Compliance roles:

1. **Risk identification and scoping** — connecting a risk to a defined business service.
2. **Inherent and residual risk assessment** — showing how controls change exposure without eliminating the underlying risk.
3. **Risk treatment and ownership** — assigning accountable mitigation work and tracking completion.
4. **Third-party due diligence** — assessing a vendor before onboarding and converting exceptions into managed issues.
5. **Control design and operating effectiveness** — defining what a control should do and testing whether it actually operates as expected.
6. **Exception and finding management** — documenting evidence, impact, priority and recommended corrective action.
7. **Remediation governance** — assigning corrective action, documenting completion and requiring review before closure.
8. **Audit workflow management** — moving an engagement through validation, fieldwork, approval and closure.
9. **Traceability** — linking entities, risks, controls, tests, issues and remediation instead of managing them as isolated records.
10. **Management reporting** — converting detailed GRC records into concise executive indicators.

---

# Role alignment

| Role | Evidence from this portfolio |
|---|---|
| GRC / Cybersecurity GRC Analyst | Risk register, controls, issues, remediation, governance workflow and reporting |
| Technology Risk Analyst | Inherent/residual risk assessment, treatment, ownership, monitoring and executive metrics |
| Cybersecurity Compliance Analyst | MFA control requirements, control testing, exception management and remediation verification |
| Junior IT Auditor / Technology Auditor | Audit engagement, test plan, operating-effectiveness testing, finding and closure workflow |
| Third-Party Risk / Vendor Risk Analyst | Vendor profile, engagement, questionnaire, assessment, issue, remediation and internal review |
| ServiceNow GRC / IRM Analyst | Hands-on configuration and execution of connected GRC records and workflows inside ServiceNow |
| Security Risk Analyst | Security-risk scenario analysis, control evaluation, mitigation and residual-risk thinking |

---

# Repository structure

```text
ServiceNow-GRC-Portfolio-DGCL-Bank/
├── README.md
└── images/
    ├── 01-enterprise-risk-management/
    ├── 02-third-party-risk/
    ├── 03-audit-compliance/
    └── 04-executive-dashboard/
```
