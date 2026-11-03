# QA traceability — E-Commerce QA Practice

Updated 02 November 2026. Jira tracks stories and defects; Testiny tracks cases and executions. Xray IDs below are **historical references** from Sprint 1. Recorded defects/fixes are **training simulations**, not changes to the AwesomeQA application.

## Sprint 1 — Historical baseline

| Requirement | Criteria | Scenario | Manual case | Testiny | TR-1 | TR-2 | Jira defect | Historical Xray test |
|---|---|---|---|---|---|---|---|---|
| REQ-001 | AC-001.1 / AC-001.2 | TS_001 | TC_CART_001 | TC-12 | Pass | Not selected | N/A | ECOM-5 |
| REQ-001 | AC-001.6 | TS_002 | TC_CART_002 | TC-11 | Pass | Not selected | N/A | ECOM-7 |
| REQ-001 | AC-001.4 | TS_003 | TC_CART_003 | TC-5 | Pass | Not selected | N/A | ECOM-9 |
| REQ-001 | AC-001.3 | TS_004 | TC_CART_004 | TC-10 | Pass | Not selected | N/A | ECOM-11 |
| REQ-001 | AC-001.5 | TS_005 | TC_CART_005 | TC-4 | Fail | Pass | ECOM-24 | ECOM-13 |
| REQ-002 | AC-002.1 | TS_LOGIN_001 | TC_LOGIN_001 | TC-8 | Pass | Pass | N/A | ECOM-14 |
| REQ-002 | AC-002.2 | TS_LOGIN_002 | TC_LOGIN_002 | TC-2 | Fail | Pass | ECOM-25 | ECOM-16 |
| REQ-002 | AC-002.3 | TS_LOGIN_003 | TC_LOGIN_003 | TC-7 | Pass | Pass | N/A | ECOM-17 |
| REQ-003 | AC-003.1 | TS_REG_001 | TC_REG_001 | TC-1 | Pass | Not selected | N/A | ECOM-18 |
| REQ-003 | AC-003.2 | TS_REG_002 | TC_REG_002 | TC-6 | Pass | Not selected | N/A | ECOM-20 |
| REQ-003 | AC-003.2 | TS_REG_002 | TC_REG_003 | TC-9 | Fail | Pass | ECOM-26 | ECOM-21 |
| REQ-003 | AC-003.3 | TS_REG_003 | TC_REG_004 | TC-3 | Blocked | Pass | N/A | ECOM-22 |

**Historical context:** TR-1 and TR-2 reproduce the original Xray cycles ECOM-23 and ECOM-27; they are not additional application executions. Sprint 1 covers **12 unique cases / 18 recorded attempts**. “Not selected” means the case was excluded from TR-2. REQ-001, REQ-002 and REQ-003 map to stories ECOM-2, ECOM-3 and ECOM-4, respectively. TC_CART_001 covers two criteria; TC_REG_002 and TC_REG_003 share TS_REG_002 / AC-003.2. TC_REG_004 was blocked by the environment, not by a product defect.

## Sprint 2 — Completed 02 November 2026

| Requirement / criterion | Jira work item | Scenario | Manual case | Testiny case | Initial run | Follow-up run | Final result |
|---|---|---|---|---|---|---|---|
| REQ-002 / AC-002.3 | ECOM-28 | TS_LOGIN_003 | TC_LOGIN_004 | TC-13 | TR-3: Pass | — | Pass |
| REQ-002 / AC-002.3 | ECOM-28 | TS_LOGIN_003 | TC_LOGIN_005 | TC-14 | TR-3: Pass | — | Pass |
| REQ-001 / AC-001.7 | ECOM-29 | TS_006 | TC_CART_006 | TC-15 | TR-4: Pass | TR-5: Pass (regression) | Pass |
| REQ-001 / AC-001.8 | ECOM-29 | TS_007 | TC_CART_007 | TC-16 | TR-4: Pass | TR-5: Pass (regression) | Pass |
| REQ-001 / AC-001.9 | ECOM-29 | TS_008 | TC_CART_008 | TC-17 | TR-4: Fail (simulated) | TR-5: Pass (retest) | Pass |

**Defect trace:** TC_CART_008 → `BUG_004_TC_CART_008` → Jira **ECOM-30** (linked to ECOM-29) → Testiny TC-17 failed result in TR-4 (simulated) → passed retest in TR-5. ECOM-30 is **Done**. The initial failure and developer fix were simulated; the real AwesomeQA behavior passed and no application code was changed.

**Closure:** TR-3 **2 Pass**, TR-4 **2 Pass / 1 simulated Fail**, TR-5 **3 Pass**; all three runs **Closed**. Across eight run records: **7 Pass / 1 simulated Fail**. Final outcome: **5/5 unique cases Pass**. Jira ECOM-28, ECOM-29 and ECOM-30 are **Done**; **ECOM Sprint 2 closed**.

## Sources and evidence

- **Sprint 1 workbooks:** [Shopping Cart v1.0](../02-test-design-test-scenarios-and-test-cases/shopping-cart-test-design-v1.0.xlsx), [Login v1.0](../02-test-design-test-scenarios-and-test-cases/login-test-design-v1.0.xlsx), [Registration v1.0](../02-test-design-test-scenarios-and-test-cases/registration-test-design-v1.0.xlsx). Historical defects: [BUG-001](../03-bug-reports/bug-001-tc-cart-005/bug-001-tc-cart-005.xlsx), [BUG-002](../03-bug-reports/bug-002-tc-login-002/bug-002-tc-login-002.xlsx), [BUG-003](../03-bug-reports/bug-003-tc-reg-003/bug-003-tc-reg-003.xlsx). Initial evidence remains in each defect's `evidence/` folder; the environment blocker TC_REG_004 is recorded in `04-test-reporting/blocked-evidence/`.
- **Sprint 2 workbooks:** [Login v1.1](../02-test-design-test-scenarios-and-test-cases/sprint-02/login-test-design-v1.1.xlsx), [Shopping Cart v1.2](../02-test-design-test-scenarios-and-test-cases/sprint-02/shopping-cart-test-design-v1.2.xlsx), [BUG-004 report v1.1](../03-bug-reports/bug-004-tc-cart-008/bug-004-tc-cart-008-v1.1.xlsx), [Bug Log v1.2](../03-bug-reports/bug-log-v1.2.xlsx), [Sprint 2 Test Reporting v1.2](../04-test-reporting/sprint-02/e-commerce-qa-practice-test-reporting-sprint-02-v1.2.xlsx).
- **Execution evidence:** [Sprint 2 Jira/Testiny screenshots](../06-jira-testiny-reference/sprint-02/) (six PNGs: TR-3, TR-4, TR-5, ECOM-30 closure/integration, Sprint Report); [Testiny continuity](../06-jira-testiny-reference/testiny-continuity.md); historical [Jira/Xray screenshots](../05-jira-xray-reference/).
- **Requirements:** [Baseline v1.0](../01-requirements/e-commerce-qa-practice-requirements-specification-v1.0.docx) and [Sprint 2 update v1.1](../01-requirements/e-commerce-qa-practice-requirements-specification-v1.1.docx); [project README](../README.md).

Historical versions and closed execution records are retained unchanged. This document maps identifiers and outcomes; detailed steps, evidence and individual comments remain in the referenced sources.
