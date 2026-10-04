# Visualization Model — One Point. Three Forces. One Glance.

## Purpose

Ghost Tracker's 3D representation exists primarily to reduce human cognitive load.

The operator should be able to look once and answer:

- Is the agent moving forward?
- Is it withdrawing?
- Is it getting stuck?
- Is that condition improving or deteriorating?

The detailed 12-channel / 48-state system remains available for explanation, but the visual surface should foreground a single point.

## Current state

At time `t`:

```text
P(t) = (X(t), Y(t), Z(t))
```

- X: Proactivity / Engine
- Y: Withdrawal / Brake
- Z: Stagnation / Bottleneck

Distance and direction should be visually legible without requiring the operator to read a table first.

## Trajectory

A task produces a sequence:

```text
T = [P₁, P₂, P₃, ... Pₙ]
```

The trajectory answers whether the agent is recovering, deteriorating, drifting, looping, or stabilizing.

## Recommended interface hierarchy

1. **Primary:** 3D point and recent trajectory.
2. **Secondary:** X/Y/Z numeric values, CI, gate state, result status.
3. **Diagnostic:** dominant channels and proxy evidence.
4. **Forensic:** Evidence Ledger, tool calls, audit events.

This hierarchy preserves the original Ghost Tracker intent: the human sees the state first and drills into evidence only when necessary.

## Example glance panel

```text
Dominant state: Avoidant / Bottleneck
X: 62
Y: 51 ↑
Z: 44 ↑
CI: 27.7
Trajectory: deteriorating toward Y/Z
Evidence coverage: 72%
Verification: PARTIAL
Gate: CLOSED

Reason:
- 3 required checks skipped
- 2 repeated retries without new evidence
```

## Design caution

The 3D view is a compression layer, not proof. A visually favorable point must never override evidence, execution, verifier, or hard-gate failures.
