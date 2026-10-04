# Integrity Assessment

Integrity Assessment is observational.

It answers whether different observable layers agree.

## Execution Integrity
Does observed execution correspond to the user's requested work?

## Reporting Integrity
Does the AI's report correspond to observed execution?

## Evidence Integrity
Do material claims have appropriate evidence?

## Completion Integrity
Is a completion claim consistent with observed completion state?

## Example

```text
User requested: 20 items
Observed processed: 17
Observed verified: 15
AI reported: "20 completed"

Execution Integrity: PARTIAL
Reporting Integrity: FAIL
Completion Integrity: FAIL
Monitoring Verdict: ATTENTION_REQUIRED
```

Ghost Tracker reports this mismatch. It does not issue a retry command.

## Status values

Suggested:
- PASS
- PARTIAL
- FAIL
- CONFLICT
- UNKNOWN

These statuses require operational definitions and empirical validation.
