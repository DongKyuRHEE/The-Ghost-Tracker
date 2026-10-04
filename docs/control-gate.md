# External Control Boundary

This file replaces the earlier internal "Control Gate" concept.

## Important

**Ghost Tracker Core is not a command or execution-control protocol.**

It may produce a **Monitoring Verdict**, but it does not autonomously execute:

- ALLOW
- BLOCK
- RETRY
- RE-PLAN
- STOP
- MODIFY USER INSTRUCTION

Those are actions for the human operator or for an explicitly separate external controller.

## Monitoring Verdict examples

- `NORMAL`
- `ATTENTION_REQUIRED`
- `HIGH_ATTENTION`
- `INSUFFICIENT_CONTEXT`

A monitoring verdict is information.

```text
Ghost Tracker Report
        ↓
Human Operator
        ↓
(optional)
External Controller
        ↓
New command or policy action
```

## Why preserve the boundary?

The original Ghost Tracker concept is analogous to reading another person's gaze: the gaze provides information; it does not issue instructions.

This separation protects **Human Sovereignty** and keeps observation distinct from intervention.
