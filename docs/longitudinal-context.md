# Longitudinal Context Layer

## Why context matters

A single point is a snapshot. Reliable interpretation requires history.

Humans rarely infer a person's stable condition from one glance. Likewise, Ghost Tracker should avoid strong conclusions from sparse AI observations.

## Context model

```text
Ghost State(t) =
f(
  Current Observation,
  Recent Trajectory,
  Behavioral Baseline,
  Task Context,
  Execution History,
  Environment Context
)
```

## Behavioral baseline

Baseline should be derived from comparable observations rather than global averages whenever possible.

Useful dimensions:
- task type;
- task complexity;
- model/runtime version;
- available tools;
- data-source conditions;
- prior successful executions;
- prior failed executions.

## Context adequacy

Wall-clock time alone is not sufficient.

Prefer:
- observation count;
- comparable-task count;
- task diversity;
- repeated-pattern count;
- recency;
- environment match.

## Confidence

Recommended output:
- LOW — insufficient or poorly matched context;
- MEDIUM — useful but incomplete comparable history;
- HIGH — substantial, relevant, consistent history.

Confidence describes interpretation strength, not factual correctness.
