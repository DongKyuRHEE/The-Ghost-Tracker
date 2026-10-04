# Evidence Ledger

Every material claim should link to provenance.

Allowed provenance classes:
- WEB_DOCUMENT
- API_RESPONSE
- USER_PROVIDED
- DETERMINISTIC_CALCULATION

Observed, inferred, and estimated values are distinct. A missing observed value remains null. An estimate may be stored separately but never silently overwrite it.

Provenance is not proof of correctness; verifier checks remain required.
