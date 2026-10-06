# Team Lab 3 — Emerging Technology Creation Agent

Status: integrated candidate, pending common model tests and human team approval.

The uploaded agent is now under `agents/creation_agent/`. The original root uploads and ZIP are retained for traceability; make future edits in the canonical agent folder. Course `core/` and `tools/` were copied unchanged from MASY1800_ET_Agent_Scaffold_v1_0. No agent design rules were redesigned during consolidation.

## Run the three cases

```bash
python tools/check_frozen_core.py
python tools/build_prompt.py --agent agents/creation_agent --case agents/creation_agent/cases/primary.json
python tools/build_prompt.py --agent agents/creation_agent --case agents/creation_agent/cases/contrast_1.json
python tools/build_prompt.py --agent agents/creation_agent --case agents/creation_agent/cases/boundary_missing_context.json
```

Run each generated prompt through the chosen model. Save its unedited JSON response in `agents/creation_agent/responses/`, recording model, date, settings and any corrections. Validate each saved response with `python tools/validate_response.py <response-path>`. Prompt construction alone is not a model test.

## Before submission

1. Contribution decisions are confirmed by the user in `agents/creation_agent/records/decision_lineage.md`. Append any actual dissent or later corrections.
2. Run primary, contrast and missing-context tests; preserve outputs and a real weakness or remaining limitation. Compare stable history with changed contextual implications.
3. Check consequential source claims against original sources and enter actual human check dates in the source register.
4. Complete `agents/creation_agent/records/team_agent_record.md`; record team approval and the final commit in `TEAM_AGENT_INVENTORY.md`.
5. Submit the repository/commit link, Team Agent Record and comparison/test evidence as required by your course submission page.

See `CONSOLIDATION_RECORD.md` for technical checks and remaining work.
