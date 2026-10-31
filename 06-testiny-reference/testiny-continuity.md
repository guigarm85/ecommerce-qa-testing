# Testiny migration and continuing test management

The original exercise was recorded in Jira/Xray. The continuity records document migration on 4 October 2026 after the decision to let the Xray trial expire without purchasing a subscription. Cases were imported into Testiny, and runs were reconstructed to preserve the historical outcomes. This migration is part of V1. Future exercises will use Testiny, with Jira stories and defects where applicable; Xray remains historical.

## Verified state

Read-only inspection on 31 October 2026 confirmed 12 cases, two closed runs, all 12 manual REQ/AC/TS/TC references, and the same results as the manual workbooks:

| Testiny run | Historical source | Passed | Failed | Blocked |
|---|---|---:|---:|---:|
| TR-1 | ECOM-23 / Cycle 01 | 8 | 3 | 1 |
| TR-2 | ECOM-27 / Cycle 02 | 6 | 0 | 0 |

TR-2 contains TC-2, TC-3, TC-4, TC-7, TC-8 and TC-9. These reconstruct the three retests, two selected login regression tests and one blocked-case re-execution. They do not add new application test executions to the 18 original attempts.

TR-1 links TC-4 to ECOM-24, TC-2 to ECOM-25 and TC-9 to ECOM-26. Comments retain the three simulated bug images and TC_REG_004 blocker image. Attachment names inside the historical system retain their original underscores; the public files use kebab-case. The matrix points to the public paths. No re-upload or rename of historical Testiny attachments was needed.

## Evidence

| Screenshot | What is visible |
|---|---|
| [Case inventory](01-testiny-test-case-inventory.png) | 12 cases, IDs TC-1 through TC-12; last-results display is not a replacement for individual run results |
| [TR-1 historical results](02-testiny-tr-1-historical-results.png) | Closed run, reconstruction description, 8 Passed / 3 Failed / 1 Blocked |
| [TR-2 historical results](03-testiny-tr-2-historical-results.png) | Closed run, reconstruction description, six Passed |
| [TC-4 manual references](04-testiny-tc-4-manual-traceability.png) | TC_CART_005 / REQ-001 / AC-001.5 / TS_005 in the imported precondition text |
| [TC-4 defect reference](05-testiny-tc-4-defect-link.png) | Jira defect reference, title, Done status and TR-1 link; some key text is visually truncated |
| [TC-4 imported references](06-testiny-tc-4-requirement-references.png) | Story ECOM-2 and a Bug reference in the Requirements tab |
| [TR-1 defect links](07-testiny-tr-1-defect-links.png) | Three Jira defect links associated with TC-4, TC-2 and TC-9; full keys verified in visible page links |

Screenshots are views captured on the verification date, not new test executions. Some tables and long text are truncated by the interface. All 12 case references and the six TR-2 members were also checked in the visible page text; a screenshot does not show every step or every result row at once. No generated or recreated screenshots are used.

## Reference interpretation

Jira references remain valid because Jira still identifies requirements/stories and defects. Testiny supplies case and run IDs; it does not replace ECOM-24 with a new defect ID. The historical import recorded 15 requirement references. They are not 15 business requirements: the exercise has three requirements and 12 acceptance criteria. The TC-4 Requirements tab includes a Bug reference as well as its Story; this is preserved as an import observation, not presented as a new requirement or silently corrected online.

The migration record notes fields without equivalent destinations and a Type mapping adjustment. Treat this as case migration plus historical run reconstruction, not a byte-for-byte restore of every Xray setting or audit record.

## Local documentation and future changes

Use the [Testiny traceability matrix](../07-traceability/traceability.md) to connect the historical documents to Testiny and locate source workbooks, case worksheets, bug reports and evidence. Existing workbook tabs retain their original names, formulas, fictional data, outcomes and checkpoint text.

Excel export was offered by the UI but required an upgrade in the account at verification time. No upgrade was purchased and no export was obtained. The Markdown matrix is a documentary reference, not a native Testiny export or complete service backup. The independent raw Xray backup stays private.

New test cases, runs and defects belong to separately versioned exercises. Use the IDs actually created in Testiny and Jira; do not repurpose the closed historical runs. No new case, run, result, attachment, requirement or integration was created or changed online during this verification.
