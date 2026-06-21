# Mock-Internal-Audit-Vantage
Multi-framework internal audit simulation — NIST 800-53, SOC 2, ISO 27001

# Mock Internal Audit — Vantage Cloud Solutions

A self-directed GRC project simulating a multi-framework internal audit conducted ahead of a company's first SOC 2 Type II and ISO 27001 certification cycle — the core audit methodology skill that underlies most GRC analyst roles.

## Project Summary

This project conducts an internal audit of **Vantage Cloud Solutions**, a fictional B2B SaaS company pursuing dual SOC 2 Type II and ISO 27001 certification. Rather than auditing against a single framework, the project deliberately cross-maps every control to **NIST 800-53**, **SOC 2 Common Criteria**, and **ISO 27001 Annex A** simultaneously — reflecting how companies pursuing multiple certifications in parallel actually structure their compliance evidence to avoid duplicating work. The project follows the full internal audit lifecycle:

1. **Control selection** — sampling 15 controls across 11 categories (access control, data protection, system operations, incident response, change management, business continuity, vendor risk, risk management, people security, physical security, and configuration management)
2. **Evidence review** — assigning each control a status (Compliant, Partially Implemented, Non-Compliant, or Not Applicable) based on specific, quantified evidence rather than impressionistic judgment
3. **Severity scoring** — rating each gap Critical, High, or Medium based on how much active exposure it represents, not just whether a policy document is missing
4. **Audit reporting** — a 2-page report summarizing scope, results, findings, and lessons learned
5. **Corrective Action Plan** — a phased, owner-assigned remediation roadmap sequenced by severity and dependency

## Deliverables

| File | Description |
|---|---|
| `Vantage_Internal_Audit_Checklist.xlsx` / `.pdf` | Full 15-control checklist with framework cross-mapping, evidence, status, findings, severity, and remediation, plus a summary statistics tab |
| `Vantage_Audit_Report_and_CAP.docx` / `.pdf` | 2-page audit report (scope, results, findings, lessons learned) plus a 3-phase Corrective Action Plan |

## What I Did

- Selected 15 controls deliberately spanning every control category that has appeared across this portfolio's other five projects, to demonstrate breadth rather than depth in only one area
- Cross-mapped every control to three frameworks at once (NIST 800-53, SOC 2, ISO 27001 Annex A), reflecting the real-world practice of dual/multi-framework certification rather than treating each framework as a separate exercise
- Wrote evidence statements with specific, quantified findings (e.g., "3 of 6 sampled vendors," "4 of 10 deployments," "2 of 14 hosts") rather than vague descriptions, since sample-based, numeric evidence is what makes an audit finding defensible
- Deliberately included one control (Physical & Environmental Access) scoped as Not Applicable, modeling a realistic audit scoping decision for a cloud-native company rather than forcing every control into the sample regardless of relevance
- Distinguished audit severity from risk severity: a finding's severity here reflects how much active exposure or certification risk it represents right now, which is a narrower and more audit-specific question than the likelihood/impact risk scoring used in this portfolio's risk register project
- Identified that Vantage's strongest controls were technical (encryption, RBAC, configuration management, training) while its weakest were governance/process controls requiring cross-functional ownership (vendor risk, change approval, data classification) — and used that pattern to inform how remediation was sequenced
- Built a 3-phase Corrective Action Plan (0-30, 31-60, 61-90 days) sequenced by severity and dependency, rather than listing all 10 findings as equally urgent
- Explicitly connected one finding (F-09, untested IR plan) back to the lessons learned in this portfolio's own Meridian Electronics incident response project, recognizing the same root-cause pattern recurring across independent work

## What I Learned

- **A finding is only as strong as its evidence sample.** Writing "access wasn't revoked timely" is an opinion. Writing "5 of 5 sampled offboarding tickets showed 3-9 day delays, with no documented SLA" is a finding an auditor can defend under challenge. The discipline of sampling and quantifying, rather than generalizing, was the single most important audit skill this project reinforced.
- **Audit severity and risk severity are related but distinct questions.** A risk register asks "how likely and how bad would this be if it happened." An audit finding's severity asks "how much does this threaten the certification, and how exposed are we right now." An untested backup (contained, not currently exploited) and an absent vendor review (active, current, unassessed exposure) can both be real gaps, but they don't deserve the same severity rating.
- **The most common real audit pattern is technical maturity outpacing governance maturity.** Encryption, access control, and configuration management are usually implemented correctly by engineers as a matter of course. Vendor risk management, data classification, and consistent change approval require a named process owner outside any one person's default responsibilities — and that ownership gap, not technical incompetence, is where most findings in this audit actually originated.
- **"Not Applicable" is a legitimate, defensible audit outcome, not a shortcut.** Scoping a control out because it genuinely doesn't apply (no physical infrastructure to protect) is different from skipping a control that's inconvenient to assess. Documenting *why* something is out of scope is itself part of a credible audit.
- **A Corrective Action Plan needs sequencing logic, not just a list.** Treating all 10 findings as equally urgent would be both unrealistic and unhelpful to the people who have to execute the remediation. Phasing by severity, while accounting for which fixes are quick wins versus longer efforts, is what turns a findings list into something an organization can actually act on.

## Real-World Application

Internal audits like this one are a recurring, core responsibility in GRC roles, particularly for organizations pursuing or maintaining certifications:

- **Pre-certification readiness** — companies almost universally run an internal audit before paying for an external SOC 2 or ISO 27001 audit, specifically to find and fix findings like these before an external auditor (and the company's own customers, who will eventually see the resulting report) finds them first
- **Continuous compliance maintenance** — SOC 2 Type II in particular requires controls to operate effectively over an observation period, meaning internal audits recur on a cycle (often quarterly or semi-annually) rather than happening once
- **Multi-framework efficiency** — most real companies pursuing both SOC 2 and ISO 27001 (or adding HIPAA, PCI-DSS, or FedRAMP later) build their control evidence to satisfy multiple frameworks simultaneously, exactly as modeled in this project's three-framework cross-mapping
- **Board and customer assurance** — the Corrective Action Plan format demonstrated here is what gets presented to leadership and, in redacted form, sometimes to enterprise customers who ask "what did your last audit find, and what are you doing about it" during their own vendor risk reviews — directly mirroring the vendor assessment work in this portfolio's Slack project, but from the other side of the relationship

## Conclusion

This project completes the portfolio by demonstrating the audit methodology that, in many ways, validates all the other work: a control matrix, a risk register, an incident response plan, and a vendor assessment are only as credible as an independent audit confirms them to be. Conducting this audit as a standalone exercise, rather than auditing this portfolio's own prior projects, was a deliberate choice to demonstrate genuine, unbiased evaluation rather than self-grading. The resulting findings reflect a realistic, common pattern — strong technical implementation paired with under-owned governance process — and the phased Corrective Action Plan reflects the actual deliverable a GRC analyst would be expected to produce and then track to closure. Together with the other five projects in this portfolio, this audit represents the full GRC analyst skill set: building compliance programs, managing risk, assessing vendors, planning for incidents, visualizing program health, and independently verifying that all of it actually works.

---
*This is a self-directed portfolio project using a fictional organization. It does not reflect any real company's audit results or certification status.*
