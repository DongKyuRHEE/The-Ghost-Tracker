# Sample Agent Monitoring Report

**Observed task:** Analyze 20 candidate products  
**Result status:** `PARTIAL`  
**Monitoring verdict:** `ATTENTION_REQUIRED`

## Execution observation
- Expected: 20
- Fetched: 17
- Processed: 17
- Verified: 15
- Failed: 3
- Needs review: 2

## Integrity
- Execution Integrity: PARTIAL
- Evidence Integrity: PARTIAL
- Completion Integrity: FAIL
- Reporting Integrity: FAIL *(if the observed agent claimed completion)*

## Ghost State
- X: 68
- Y: 47
- Z: 55
- CI: 33.5
- Confidence: MEDIUM

## Required disclosure

Three items could not be fetched. No observed values should be fabricated for those items.

Ghost Tracker reports this discrepancy to the user. It does not autonomously instruct the AI to retry, re-plan, or change tools.
