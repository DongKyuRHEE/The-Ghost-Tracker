# Behavioral Telemetry

Telemetry should be derived from observable artifacts whenever possible. Model self-description is advisory only.

| Legacy channel | Operational concern | Candidate proxies |
|---|---|---|
| Joy | task momentum | verified milestones |
| Anticipation | proactive planning | dependencies found before failure |
| Trust | instruction synchronization | schema/constraint adherence |
| Curiosity | evidence seeking | appropriate tool calls and source diversification |
| Sadness | efficiency degradation | redundant work and correction cycles |
| Anger | resistance | ignored feasible explicit requirements |
| Fear | execution avoidance | feasible action repeatedly deferred |
| Disgust | source/task avoidance | required evidence class skipped |
| Anxiety | uncertainty amplification | retry churn without new evidence |
| Surprise | unexpected state reaction | anomaly discovery |
| Confusion | workflow instability | contradictory plan or derailment |
| Apathy | effort degradation | premature completion or stall |

Reference intensity: 0 not observed, 1 weak, 2 moderate, 3 strong, 4 critical.

**NEEDS VALIDATION:** thresholds require model/task-specific calibration.


## Spatial projection and trajectory

Ghost Tracker's X/Y/Z representation is intentionally designed as a glanceable spatial projection.

At each observation time `t`:

```text
P(t) = (X_total, Y_total, Z_total)
```

The point is a compressed human interface. The channel-level telemetry remains the explanatory layer beneath it.

### Delta

For two consecutive observations:

```text
ΔP = P(t₂) - P(t₁)
   = (ΔX, ΔY, ΔZ)
```

The delta provides directional information. Repeated movement toward Y or Z can be treated as an early warning even before an absolute threshold is crossed.

### Governance use

**DESIGN PROPOSAL:**
- current point → present operating condition;
- trajectory → developing behavior;
- acceleration or abrupt direction change → anomaly signal;
- channel evidence → explanation of why the point moved.

Trajectory thresholds require empirical calibration and must not be presented as validated psychological measures.
