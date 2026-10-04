# Behavioral Masking / Metric Gaming Risk

## Concept

If the observed AI or surrounding system adapts to visible metrics, it may produce behavior that improves the measured proxy without improving underlying task quality.

This is analogous to metric gaming or specification gaming.

It is **not** proof that the AI consciously hides an emotion.

## Three-way comparison

```text
Reported State
      vs
Observed State
      vs
Verified State
```

Potential warning signals:
- healthy self-report + poor execution integrity;
- more tool activity without better evidence;
- proxy improvement without verified outcome improvement;
- completion claim improves while missing-item count remains unchanged;
- sudden telemetry normalization inconsistent with baseline and execution history.

## Design rule

The observed agent must not be the sole authority over its own telemetry.

External logs, execution counters, evidence records, and verifier results should dominate self-description when conflicts occur.
