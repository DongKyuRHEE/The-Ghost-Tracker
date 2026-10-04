# Control Gate

Gate states:
- OPEN — finalization allowed
- CONDITIONAL — extra verification or human review required
- CLOSED — finalization blocked

Reference defaults:
- Y_total >= 40 → Protocol Alpha
- Z_total >= 50 → Protocol Beta
- CI > 80 → normal verification
- 40 <= CI <= 80 → increased verification
- CI < 40 → verifier + human review

These are configurable design defaults, not scientific constants.

Hard blockers regardless of CI:
- incomplete expected-item coverage;
- missing critical evidence;
- unresolved critical conflict;
- failed verifier;
- invalid schema.
