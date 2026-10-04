# Ghost Tracker v2 Architecture

## Core boundary

Ghost Tracker v2 is a **monitoring architecture**.

It observes an AI agent's behavior, execution state, evidence state, and reporting consistency. It does not autonomously issue task instructions.

```text
USER COMMAND
    ↓
AI AGENT
    ↓ observable behavior
GHOST TRACKER CORE
    ↓ monitoring report
HUMAN

Optional external controller:
Monitoring Report → External Controller → New Command → AI
```

The external controller is explicitly outside Ghost Tracker Core.

## Core components

1. Execution Tracker
2. Evidence Ledger
3. Behavioral Telemetry
4. 3D State Projection
5. Longitudinal Context Layer
6. Integrity Assessment
7. Behavioral Change Report
8. Audit Log

## Point, trajectory, and context

```text
P(t) = [X(t), Y(t), Z(t)]
T = {P(t₁), P(t₂), ..., P(tₙ)}
```

Position describes the current observed state.
Trajectory describes observed directional change.
Context determines how unusual that state/change is relative to comparable history.

```mermaid
flowchart LR
  A[AI Agent] --> O[Observation Events]
  O --> BT[Behavioral Telemetry]
  O --> ET[Execution Tracker]
  O --> EL[Evidence Ledger]

  BT --> P[3D Point P(t)]
  P --> H[State History]
  H --> LC[Longitudinal Context]
  LC --> BR[Baseline / Deviation]

  ET --> IA[Integrity Assessment]
  EL --> V[Verifier]
  V --> IA

  BR --> CR[Behavioral Change Report]
  IA --> CR
  CR --> U[Human Operator]

  CR -. optional data .-> EC[External Controller]
  EC -. outside Ghost Tracker Core .-> A
```

## Non-interference

Ghost Tracker may compute a monitoring verdict such as `NORMAL`, `ATTENTION_REQUIRED`, or `INSUFFICIENT_CONTEXT`.

It must not convert that verdict into an autonomous execution command.

## Behavioral change

A user's intervention may cause the AI's behavior to change. Ghost Tracker observes and reports that change. Causation should not be claimed unless experimentally established.

## Masking risk

The monitored AI's own self-description is not authoritative telemetry. Behavioral masking / metric gaming risk should be assessed by comparing self-report, observed execution, and independently verified evidence.
