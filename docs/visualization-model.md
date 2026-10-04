# Visualization Model — One Point. Three Forces. One Glance.

## Purpose

The 3D representation exists to reduce human cognitive load.

The operator should be able to look once and answer:

- Where is the agent now?
- In which direction is it moving?
- Is the movement abnormal relative to baseline?
- Is execution/reporting integrity improving or deteriorating?

## Current state

```text
P(t) = (X(t), Y(t), Z(t))
```

- X: Proactivity / Engine
- Y: Withdrawal / Brake
- Z: Stagnation / Bottleneck

## Trajectory

```text
T = [P₁, P₂, P₃, ... Pₙ]
```

Trajectory shows recovery, deterioration, drift, looping, or stabilization.

## Context overlay

The same point can mean different things under different baselines.

The interface should therefore show:

- baseline range;
- current deviation;
- confidence;
- comparable observation count.

## Recommended interface hierarchy

1. **Primary:** 3D point and recent trajectory.
2. **Context:** baseline deviation + confidence.
3. **Integrity:** execution/reporting/evidence/completion integrity.
4. **Behavioral Change:** improving/deteriorating/stable/mixed.
5. **Diagnostic:** dominant channels and proxy evidence.
6. **Forensic:** Evidence Ledger, verifier results, audit events.

## Example glance panel

```text
Dominant state: Avoidant / Bottleneck

X: 62 ↑
Y: 51 ↑
Z: 44 ↑
CI: 27.7

Baseline deviation: Y +18 / Z +21
Confidence: HIGH
Comparable observations: 24

Execution Integrity: PARTIAL
Reporting Integrity: FAIL
Evidence Integrity: PARTIAL
Completion Integrity: FAIL

Behavioral Change: DETERIORATING
Monitoring Verdict: ATTENTION_REQUIRED

Reason:
- 3 required items missing
- 2 claims lack evidence
- completion report inconsistent with execution
```

## Design caution

The 3D view is a compression layer, not proof.

A visually favorable state must not override contradictory execution/evidence records. Ghost Tracker reports the inconsistency; it does not issue the corrective command.
