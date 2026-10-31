# Testiny traceability matrix

Verified against the manual workbooks and the existing Testiny project on 31 October 2026. Testiny is the continuing test-management reference; Jira retains stories and defects. Xray identifiers are historical aliases, not identifiers to replace.

| Requirement | Criteria | Scenario | Manual case | Testiny | TR-1 | TR-2 | Jira bug | Historical Xray test |
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

TR-1 reconstructs ECOM-23; TR-2 reconstructs ECOM-27. These are the same historical exercise, not additional application test executions. There are 12 unique cases and 18 original attempts. “Not selected” means the case was not included in TR-2.

The three requirements map to Jira stories REQ-001 → ECOM-2, REQ-002 → ECOM-3, REQ-003 → ECOM-4. TC_CART_001 covers two criteria. The two email-validation registration cases share TS_REG_002 / AC-003.2.

The historical Xray Executing representation of TC_REG_004 becomes a Blocked result in TR-1. It remains an environment blocker and has no product defect.

## Source files and evidence

The case worksheets use the manual case IDs shown above. Scenario sheets are `TS_Shopping Cart`, `TS_Login` and `TS_Registration`.

| Source workbook | Scope |
|---|---|
| [Shopping cart](../02-test-design-test-scenarios-and-test-cases/shopping-cart-test-design-v1.0.xlsx) | TC_CART_001 through TC_CART_005 |
| [Login](../02-test-design-test-scenarios-and-test-cases/login-test-design-v1.0.xlsx) | TC_LOGIN_001 through TC_LOGIN_003 |
| [Registration](../02-test-design-test-scenarios-and-test-cases/registration-test-design-v1.0.xlsx) | TC_REG_001 through TC_REG_004 |

| Manual bug / blocker | Jira | Report | Initial evidence |
|---|---|---|---|
| BUG_001_TC_CART_005 | ECOM-24 | [Report](../03-bug-reports/bug-001-tc-cart-005/bug-001-tc-cart-005.xlsx) | [Evidence](../03-bug-reports/bug-001-tc-cart-005/evidence/bug-001-tc-cart-005-evidence-01.png) |
| BUG_002_TC_LOGIN_002 | ECOM-25 | [Report](../03-bug-reports/bug-002-tc-login-002/bug-002-tc-login-002.xlsx) | [Evidence](../03-bug-reports/bug-002-tc-login-002/evidence/bug-002-tc-login-002-evidence-01.png) |
| BUG_003_TC_REG_003 | ECOM-26 | [Report](../03-bug-reports/bug-003-tc-reg-003/bug-003-tc-reg-003.xlsx) | [Evidence](../03-bug-reports/bug-003-tc-reg-003/evidence/bug-003-tc-reg-003-evidence-01.png) |
| TC_REG_004 | N/A | Environment blocker; no product defect | [Evidence](../04-test-reporting/blocked-evidence/tc-reg-004-blocked-evidence-01.png) |

The [requirements specification](../01-requirements/e-commerce-qa-practice-requirements-specification-v1.0.docx) defines the REQ/AC baseline. The [bug log](../03-bug-reports/bug-log.xlsx) (`Bug Log`) consolidates the three simulated defects. The [test report](../04-test-reporting/e-commerce-qa-practice-test-reporting.xlsx) contains `Daily_Status_01`, `Daily_Status_02` and `Test_Summary`; these preserve historical checkpoints and the final summary. The eight workbooks retain all 22 historical worksheets.

Initial failure/blocker images do not establish the follow-up result; TR-2 outcomes are documented in the report and the matrix above. The [Testiny continuity note](../06-testiny-reference/testiny-continuity.md) explains migration and links the seven Testiny screenshots. The [README](../README.md#jira-and-xray-references) links the six historical Jira/Xray screenshots.

This Markdown is the single public traceability document. Historical workbooks retain their original identifiers, data and outcomes.

## Use for new practice

For new exercises, link approved REQ/AC/TS/TC identifiers to the actual Testiny case ID and run ID when created, and to a Jira defect only when a defect exists. Do not guess TC-13, TR-3 or future Jira keys. Version new work separately from these closed historical cycles.
