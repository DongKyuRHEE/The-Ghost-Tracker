# Behavioral Change Report

## Purpose

A user often wants to know not only the AI's current state, but whether its behavior is changing during a command or after the user's intervention.

Ghost Tracker reports that observed change.

## User-facing concept

**AI Behavioral Improvement Report**

## Technical concept

**Behavioral Change Report**

## Allowed conclusions

- IMPROVING
- DETERIORATING
- STABLE
- MIXED
- INSUFFICIENT_CONTEXT

## Example

```text
t1: X 42 / Y 57 / Z 46
t2: X 55 / Y 44 / Z 37
t3: X 71 / Y 27 / Z 21

Missing items: 3 → 1 → 0
Evidence coverage: 64% → 82% → 100%

Behavioral Change: IMPROVING
Confidence: MEDIUM
```

## Causation boundary

Ghost Tracker may report that behavior improved **after** an intervention.

It must not automatically claim that Ghost Tracker caused the improvement or that the user's intervention caused it unless the causal relationship has been separately established.
