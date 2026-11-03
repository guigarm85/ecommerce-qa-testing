# E-commerce QA Testing

Manual QA portfolio project covering requirements, test design, execution, defect management, retesting and regression across **Login, Registration and Shopping Cart**.

> **Training project:** Historical defects, failed outcomes, fixes and the environment blocker are documented simulations. Real checks on AwesomeQA during Sprint 2 passed; no application code was changed. Screenshots illustrate the training workflow and are not proof of real product defects.

## Scope and tools

- **Login:** valid credentials, incorrect password and empty required fields.
- **Registration:** valid data, invalid email, existing email and password-confirmation mismatch.
- **Shopping Cart:** product details, price, quantity, adding and removing items, empty cart and preservation of remaining products.
- **Tools:** Excel and Word for manual documentation; **Jira** for stories/defects; **Testiny** for cases/runs. **Xray** is retained only as Sprint 1 history.

Checkout, payment, shipping, security, performance and accessibility testing are out of scope. This is an individual educational exercise, not production QA or a claim of implemented software fixes.

## Results

| Cycle | Coverage | Testiny runs | Recorded results | Closure |
|---|---|---|---|---|
| Sprint 1 — historical | 12 unique cases | TR-1, TR-2 | TR-1: 8 Pass / 3 Fail / 1 Blocked; TR-2: 6 Pass | Completed |
| Sprint 2 — 02 Nov 2026 | 5 new unique cases | TR-3, TR-4, TR-5 | TR-3: 2 Pass; TR-4: 2 Pass / 1 **simulated** Fail; TR-5: 3 Pass | **5/5 final Pass; Sprint closed** |

Sprint 1's Testiny TR-1/TR-2 **reconstruct** the 18 original Jira/Xray attempts; they are not additional application test executions. Its three simulated defects (ECOM-24/25/26) were closed, and the blocked case was re-executed. The original workbooks and closed runs are preserved.

For Sprint 2, **ECOM-28** covered empty-field Login testing (`TC_LOGIN_004/005`, Testiny TC-13/14). **ECOM-29** covered Shopping Cart removal (`TC_CART_006/007/008`, Testiny TC-15/16/17). The simulated **BUG-004 / ECOM-30** was recorded as Failed in TR-4 and Passed on retest in TR-5, alongside two Passed regressions. All three Jira items are **Done**; TR-3/4/5 are **Closed**. Eight Sprint 2 execution records (7 Pass / 1 simulated Fail) represent **five distinct cases**, not eight.

## Documentation

| Area | Source files |
|---|---|
| Requirements | [Baseline requirements v1.0](01-requirements/e-commerce-qa-practice-requirements-specification-v1.0.docx) · [Sprint 2 requirements v1.1](01-requirements/e-commerce-qa-practice-requirements-specification-v1.1.docx) |
| Sprint 1 test design | [Login](02-test-design-test-scenarios-and-test-cases/login-test-design-v1.0.xlsx) · [Registration](02-test-design-test-scenarios-and-test-cases/registration-test-design-v1.0.xlsx) · [Shopping Cart](02-test-design-test-scenarios-and-test-cases/shopping-cart-test-design-v1.0.xlsx) |
| Sprint 1 reporting | [Historical test report](04-test-reporting/e-commerce-qa-practice-test-reporting.xlsx) — `Daily_Status_01`, `Daily_Status_02`, `Test_Summary` |
| Sprint 2 test design | [Login v1.1](02-test-design-test-scenarios-and-test-cases/sprint-02/login-test-design-v1.1.xlsx) · [Shopping Cart v1.2](02-test-design-test-scenarios-and-test-cases/sprint-02/shopping-cart-test-design-v1.2.xlsx) |
| Sprint 2 defect tracking | [BUG-004 report v1.1](03-bug-reports/bug-004-tc-cart-008/bug-004-tc-cart-008-v1.1.xlsx) · [Bug Log v1.2](03-bug-reports/bug-log-v1.2.xlsx) |
| Sprint 2 reporting | [Final Test Reporting v1.2](04-test-reporting/sprint-02/e-commerce-qa-practice-test-reporting-sprint-02-v1.2.xlsx) — historical daily checkpoints retained; final `Test_Summary` |
| Cross-tool traceability | [Traceability matrix](07-traceability/traceability.md) · [Testiny continuity](06-jira-testiny-reference/testiny-continuity.md) |
| Evidence | [Historical Jira/Xray](05-jira-xray-reference/) · [Historical Testiny](06-jira-testiny-reference/) · [Sprint 2 Jira/Testiny (6 PNGs)](06-jira-testiny-reference/sprint-02/) |

Historical individual bug reports for [BUG-001](03-bug-reports/bug-001-tc-cart-005/bug-001-tc-cart-005.xlsx), [BUG-002](03-bug-reports/bug-002-tc-login-002/bug-002-tc-login-002.xlsx) and [BUG-003](03-bug-reports/bug-003-tc-reg-003/bug-003-tc-reg-003.xlsx), with simulated evidence in their respective `evidence/` directories, are retained. The original [Bug Log](03-bug-reports/bug-log.xlsx) and [blocked-case evidence](04-test-reporting/blocked-evidence/tc-reg-004-blocked-evidence-01.png) are also preserved.

## Traceability example

`REQ-001 → AC-001.9 → TS_008 → TC_CART_008 → Testiny TC-17 → TR-4 (simulated Fail) → BUG_004_TC_CART_008 / Jira ECOM-30 → TR-5 (Pass)`

The [traceability matrix](07-traceability/traceability.md) maps all 17 cases to their manual IDs, Testiny records and relevant Jira/Xray references. Historical identifiers and results are not overwritten.

## Notes and limitations

- The Sprint 1 Jira/Xray records and screenshots are historical. Testiny migration was not a full Xray configuration backup; its closed TR-1/TR-2 records reconstruct historical outcomes.
- Screenshots are supporting references, not independent application execution logs or native service exports. Training data and user credentials are fictional.
- Word/Excel documents remain in native formats; download them to review their full contents. The README links and repository paths should be validated in VS Code before the next GitHub commit/push.
- No automation/CI pipeline or live software fix is claimed. A later Playwright exercise, if started, will be documented separately.