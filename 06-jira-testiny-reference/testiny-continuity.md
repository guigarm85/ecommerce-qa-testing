# Testiny continuity — E-Commerce QA Practice

Updated 02 November 2026. **Testiny** manages test cases and executions; **Jira** manages stories and defects. **Xray** is historical only. Defects and developer fixes described as simulations are educational records, not actual changes to AwesomeQA.

## Historical migration — Sprint 1

On 04 October 2026, the Jira/Xray exercise was migrated to Testiny after the decision not to renew the Xray trial. The 12 cases were imported; two closed Testiny runs **reconstructed** the original Xray execution results (not new application executions). The migration was checked on 31 October 2026.

| Run | Historical source | Cases/results | State |
|---|---|---|---|
| TR-1 | ECOM-23 / Cycle 01 | 12 cases: 8 Passed, 3 Failed, 1 Blocked | Closed |
| TR-2 | ECOM-27 / Cycle 02 | 6 cases: 6 Passed | Closed |

TR-2 contains TC-2, TC-3, TC-4, TC-7, TC-8 and TC-9: three defect retests, two Login regressions and one blocker re-execution. The source history therefore remains **12 unique cases and 18 recorded attempts**. The TR-1 defects link TC-4 → ECOM-24, TC-2 → ECOM-25 and TC-9 → ECOM-26; TC_REG_004 was an environment blocker, not a product defect. Source images, original attachment names, Xray aliases and manual workbook results remain historical.

The migration was not a byte-for-byte restoration of Xray configuration. Some fields required mapping adjustments; the historical TC-4 Requirements view also retained a Bug reference. The original verification noted 15 linked requirement references, not 15 separate business requirements. The independent Xray backup remains private; Testiny Excel export required a paid upgrade at the time of verification, and no export was obtained.

## Sprint 2 — Completed

Five new cases were created in Testiny (total **17 cases**), and three new runs were executed and closed:

| Run | Jira scope | Testiny cases / manual cases | Results | Status |
|---|---|---|---|---|
| TR-3 — Login Negative Testing | ECOM-28; REQ-002 / AC-002.3 | TC-13 / TC_LOGIN_004; TC-14 / TC_LOGIN_005 | 2 Passed | Closed |
| TR-4 — Shopping Cart Removal | ECOM-29; REQ-001 / AC-001.7–AC-001.9 | TC-15 / TC_CART_006; TC-16 / TC_CART_007; TC-17 / TC_CART_008 | 2 Passed; 1 Failed **(simulated, TC-17)** | Closed |
| TR-5 — Shopping Cart Retest & Regression | ECOM-29 / ECOM-30 | TC-15 and TC-16 (regression); TC-17 (retest) | 3 Passed | Closed |

**Defect chain:** `BUG_004_TC_CART_008` ↔ Jira **ECOM-30** ↔ TC-17. The original simulated Failed result is retained in TR-4, while the successful retest is recorded in TR-5. The defect is linked in the Testiny/Jira integration and ECOM-30 is **Done**. The failure and developer fix were simulated; actual manual checks on AwesomeQA passed and no application code was modified.

**Sprint 2 closure:** 5 distinct test cases, all **Passed** in their final validation. Across TR-3/4/5 there are **8 execution records: 7 Passed and 1 simulated Failed** (not eight distinct cases). ECOM-28, ECOM-29 and ECOM-30 are **Done**, and **ECOM Sprint 2 was closed on 02 November 2026**. Historical TR-1/TR-2 outcomes were not overwritten.

## Evidence and reference documents

- **Historical Testiny evidence** (files 01–07 in this folder): [case inventory](01-testiny-test-case-inventory.png), [TR-1](02-testiny-tr-1-historical-results.png), [TR-2](03-testiny-tr-2-historical-results.png), [TC-4 manual mapping](04-testiny-tc-4-manual-traceability.png), [TC-4 defect](05-testiny-tc-4-defect-link.png), [TC-4 requirements](06-testiny-tc-4-requirement-references.png), [TR-1 defect links](07-testiny-tr-1-defect-links.png).
- **Sprint 2 evidence:** [six Jira/Testiny screenshots](sprint-02/) covering TR-3, TR-4, TR-5, ECOM-30 closure and test-execution traceability, and the completed Sprint Report.
- **Source mapping:** [traceability.md](../07-traceability/traceability.md) connects REQ/AC/TS/manual TC IDs with Testiny cases, Jira work items, manual workbooks and defect reports. See also the [Sprint 2 Test Reporting v1.2](../04-test-reporting/sprint-02/e-commerce-qa-practice-test-reporting-sprint-02-v1.2.xlsx).

Screenshots document the visible system state; they are not native exports or backups. The original simulated failures and closed runs are retained to preserve the audit trail. New exercises should use new case/run records rather than rewriting historical results.
