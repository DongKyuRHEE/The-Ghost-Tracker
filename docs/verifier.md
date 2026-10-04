# Verifier Layer

The Verifier is logically separate from the Worker Agent.

Required checks include:
- requested count vs processed count;
- source/reference integrity;
- deterministic recomputation;
- required-field completeness;
- unsupported numeric claims;
- evidence conflicts;
- status correctness;
- completion predicate.

Do not verify solely by asking the Worker whether its own answer is correct. Prefer source re-reading or recomputation.
