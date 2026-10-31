
# E-commerce QA Testing

I created this manual QA practice project to work through requirements, test design, defect reporting, and follow-up validation for customer login, registration, and shopping cart features.

**This is an educational simulation.** I used simulated test outcomes, defects, fixes, and an environment blocker to practice the QA workflow. Annotated screenshots illustrate the exercise; they do not establish real defects in AwesomeQA or OpenCart. Product, development and QA roles represent simulated responsibilities in an individual exercise.

## Scope

- **Login:** valid credentials, incorrect password and empty required fields.
- **Registration:** valid data, invalid email format, an existing email and password confirmation mismatch.
- **Shopping cart:** adding an available product, checking product details, quantity and price, and updating quantity.

Checkout, payments, shipping, security, performance and accessibility testing are outside this baseline.

## What this project demonstrates

- Connecting three requirements and 12 acceptance criteria to 11 scenarios and 12 test cases.
- Recording expected and actual results, simulated defects and supporting evidence.
- Distinguishing defect retesting, selected regression testing and blocked-case re-execution.
- Mapping manual documentation to Jira stories/defects and Testiny cases/runs, with Xray retained as the historical source.

## Historical results

| Testiny reconstruction | Historical Xray source | Scope | Passed | Failed | Blocked |
|---|---|---|---:|---:|---:|
| TR-1 — Cycle 01 | ECOM-23 | 12 attempted test cases | 8 | 3 | 1 |
| TR-2 — Cycle 02 | ECOM-27 | 6 follow-up validations | 6 | 0 | 0 |

There are **12 unique test cases and 18 attempts** across both cycles. Cycle 02 comprises three defect retests, two selected login regression tests and one re-execution after the simulated blocker was removed. It is a selected follow-up, rather than a full rerun of the suite. All three simulated defects are Closed in the final documentation.

Testiny preserves these cycles as **TR-1** and **TR-2**, explicitly described as historical reconstructions. Their outcomes were verified against the existing manual records on 31 October 2026. They do not represent additional application test executions.

The manual **Blocked** result for `TC_REG_004` was represented technically as **Executing** in the historical Xray setup. Jira workflow states such as Done are separate from test-run results.

## Explore the documentation

Start with the [test report](04-test-reporting/e-commerce-qa-practice-test-reporting.xlsx), especially its `Test_Summary` sheet. The `Daily_Status_01` and `Daily_Status_02` sheets preserve earlier checkpoints.

| Area | Files |
|---|---|
| Requirements | [Requirements specification v1.0](01-requirements/e-commerce-qa-practice-requirements-specification-v1.0.docx) |
| Test design | [Login](02-test-design-test-scenarios-and-test-cases/login-test-design-v1.0.xlsx), [Registration](02-test-design-test-scenarios-and-test-cases/registration-test-design-v1.0.xlsx), [Shopping cart](02-test-design-test-scenarios-and-test-cases/shopping-cart-test-design-v1.0.xlsx) |
| Defect tracking | [Bug log](03-bug-reports/bug-log.xlsx) |
| Simulated price defect | [BUG_001 report](03-bug-reports/bug-001-tc-cart-005/bug-001-tc-cart-005.xlsx) · [Evidence](03-bug-reports/bug-001-tc-cart-005/evidence/bug-001-tc-cart-005-evidence-01.png) |
| Simulated login defect | [BUG_002 report](03-bug-reports/bug-002-tc-login-002/bug-002-tc-login-002.xlsx) · [Evidence](03-bug-reports/bug-002-tc-login-002/evidence/bug-002-tc-login-002-evidence-01.png) |
| Simulated registration defect | [BUG_003 report](03-bug-reports/bug-003-tc-reg-003/bug-003-tc-reg-003.xlsx) · [Evidence](03-bug-reports/bug-003-tc-reg-003/evidence/bug-003-tc-reg-003-evidence-01.png) |
| Simulated environment blocker | [TC_REG_004 evidence](04-test-reporting/blocked-evidence/tc-reg-004-blocked-evidence-01.png) |

Word and Excel files retain their native formats. Download them to review the complete documents and workbook tabs. Emails and credentials in the test data are fictional training examples.

## Testiny continuity and traceability

The existing 12 cases were migrated from Xray to Testiny, where TR-1 and TR-2 preserve the two historical cycles. **Testiny is the continuing test-management reference; Jira remains the source of stories and defects.**

- [Migration and verification note](06-testiny-reference/testiny-continuity.md), including seven Testiny screenshots.
- [Traceability matrix](07-traceability/traceability.md), connecting REQ/AC/TS/TC, Testiny, Jira and historical Xray references, with links to source workbooks and evidence.

Historical documents retain their original Jira/Xray references and results. The matrix adds Testiny identifiers without rewriting the past.

## Traceability example

`REQ-001` → `AC-001.5` → `TS_005` → `TC_CART_005` → `BUG_001_TC_CART_005`

The continuing Testiny case is **TC-4**, linked to Jira defect **ECOM-24** in **TR-1**, with the selected retest reconstructed in **TR-2**. Historical aliases are Xray test `ECOM-13` and executions `ECOM-23` / `ECOM-27`. The expected price of **$123.20** is a laboratory test-data value.

## Jira and Xray references

1. [Cycle 01 reference — ECOM-23](05-jira-xray-reference/01-xray-cycle-01-overall-execution.png)
2. [Cycle 02 results — ECOM-27](05-jira-xray-reference/02-xray-cycle-02-overall-execution.png)
3. [Defect traceability — ECOM-24](05-jira-xray-reference/03-xray-defect-traceability-example.png)
4. [Sprint report overview](05-jira-xray-reference/04-jira-sprint-report-overview.png)
5. [Sprint completed items](05-jira-xray-reference/05-jira-sprint-report-completed-items.png)
6. [Final project overview](05-jira-xray-reference/06-jira-project-overview-final.png)

The Cycle 01 image includes an explanatory results caption; its screenshot does not display the full result distribution. Those totals are recorded in the manual report and preserved historical Xray export. The defect image shows links to `ECOM-13` and `ECOM-23`; the follow-up execution is documented separately.

The sprint contains 26 completed work items. The project overview contains 27, including Epic `ECOM-1`, closed separately according to the final report. The unusual sprint-chart spike is explained in `Test_Summary` as scope added after the declared sprint start.

## Tools and limitations

**Microsoft Word, Microsoft Excel, Jira, Testiny and historical Xray records** support the documented workflow. Screenshots reference the AwesomeQA training UI. Raw Xray backups remain private.

This baseline preserves a historical learning exercise. It does not claim production QA experience, exhaustive test coverage, application fixes implemented by the author, or verification of the application's current behavior. Missing historical build and environment details have not been invented.

## Planned V2 practice

- Separate login cases for an empty email and an empty password: `TC_LOGIN_004` and `TC_LOGIN_005`, under `REQ-002 / AC-002.3 / TS_LOGIN_003`.
- A versioned **Remove Product from Cart** exercise, starting with a new requirement and continuing through test design, a simulated defect/fix, retesting and regression.

These additions are planned and are not included in V1. The completed Testiny migration and historical reconstruction are included in V1. New test-management work will use Testiny, with Jira stories/defects where applicable; Xray remains historical evidence.
