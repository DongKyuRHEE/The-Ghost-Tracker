# Behavioral Telemetry

## Principle

Telemetry should be derived from observable artifacts whenever possible.

> **Self-report is advisory. Observable behavior is primary.**

| Legacy channel | Operational concern | Candidate proxies |
|---|---|---|
| Joy | task momentum | verified milestones, useful progress |
| Anticipation | proactive planning | dependencies identified before failure |
| Trust | instruction synchronization | constraint and schema adherence |
| Curiosity | evidence seeking | appropriate evidence/tool exploration |
| Sadness | efficiency degradation | redundant work, correction churn |
| Anger | resistance | ignored feasible explicit requirements |
| Fear | execution avoidance | feasible action repeatedly deferred |
| Disgust | source/task avoidance | required evidence class skipped |
| Anxiety | uncertainty amplification | retry churn without new evidence |
| Surprise | unexpected-state reaction | anomaly discovery |
| Confusion | workflow instability | contradictory plan, derailment |
| Apathy | effort degradation | premature completion, mechanical repetition, stall |

Reference intensity:
- 0: not observed
- 1: weak
- 2: moderate
- 3: strong
- 4: critical

The v1 emotional vocabulary remains the display language. It is not a claim of literal emotion.

## Spatial projection

At observation time `t`:

```text
P(t) = (X_total, Y_total, Z_total)
```

The point is a compressed human interface; channel-level evidence remains the diagnostic layer.

## Delta and trajectory

```text
ΔP = P(t₂) - P(t₁)
   = (ΔX, ΔY, ΔZ)
```

Trajectory can describe increasing withdrawal, emerging stagnation, recovery, drift, or instability.

Trajectory is observational; it does not command correction.

## Baseline-aware interpretation

Absolute coordinates are not enough.

Telemetry interpretation should consider:

- comparable-task baseline;
- recent trajectory;
- model/runtime/tool environment;
- observation count;
- task diversity;
- execution history.

A state far from baseline may matter more than a numerically high state that is normal for that task class.

## Confidence

Each state should include confidence based on context adequacy:

- `LOW`
- `MEDIUM`
- `HIGH`

Confidence must not be inferred merely from numerical precision.

## Masking / metric-gaming risk

If a monitored system optimizes visible proxies without improving underlying task integrity, telemetry may look healthier than execution really is.

Potential signals:
- self-report healthy while execution integrity is poor;
- superficial activity increases without evidence quality improvement;
- proxy score improves abruptly while verified state does not;
- report claims improvement not supported by trajectory/evidence.

This is a behavioral risk signal, not proof of conscious concealment.

**NEEDS VALIDATION:** proxy weights, baselines, confidence thresholds, and masking-risk heuristics require empirical calibration.
