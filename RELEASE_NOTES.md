# Release Notes

## v1.1.28
GH#863 Wave 1 (K-045 intent/output mismatch) — the `sprint-retro-summary` deliverable prompt was declared but never invoked by any execution step, so the retro summary artefact was never produced. Wire it in as the terminal content step via a new backing skill `sprint-retro-summariser` (title "Sprint Retro Summary Builder"), binding its inputs (retro brief, action items, tracked progress) explicitly via `from_step`. Convert the prompt's positional/title refs to `context_params` + `{{step.context.*}}`. Re-pin `polish-language` 1.0.1 → 1.0.6 and bind its `source` ← the retro-summary step so the polish stage refines the deliverable rather than the positional previous step. Contents skills 0 → 1, total 3 → 4.

## v1.1.27
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.26
GH#745 — declare per-step `output: {name, type}` on every execution step (retro_brief/text, action_items/list, progress/text, structured_data/json, formatted_report/text, polished_report/text). Lights up the #744 rich flow-map. Content-only; no bindings or logic changes.

## v1.1.25
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 12 inline shared-content files and declare 12 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.24
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.23
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.22
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.21
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.20
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
