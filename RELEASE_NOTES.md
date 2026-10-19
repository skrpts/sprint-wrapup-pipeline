# Release Notes

## v1.1.30
GH#1044 — document the inputs this workflow's prompts REQUIRE but its Inputs table never listed. A user supplying exactly what the table asked for was running with required parameters unsatisfied — a silent wrong run, not a documentation nicety. documented 1 input(s): sprint_notes. Every row is generated from the requiring prompt's own declared description, example and required flag — none invented. No behaviour change; documentation only.

## v1.1.29
GH#1011 — 1 step(s) that declared the non-existent `local.transform` now declare the LLM step type they were already dispatched as, and reference the shared prompt their skill never had: `format-conversion` → `content`. The `format-conversion` step declares `context.target_format: "markdown"` — the skill supports six formats, so the format belongs to the step rather than to the shared prompt.

These steps had no `prompt:` because `local.*` types need none, so the engine's LLM default had nothing to send: the author saw the model complaining about a prompt nobody wrote. **Output changes** — from a complaint to the thing the skill describes. Shared deps re-pinned to 1.0.4 with the published bundle checksum.

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
