# Alice AI

Alice AI is a standalone extraction of the Alice phase-1 land research product line from the merged DoWhiz PR `#1379`.

It packages the original skill contracts, schemas, registry data, scripts, references, and example workspaces into an isolated repository so the Alice product can evolve without changing the main DoWhiz codebase.

## What is included

- Buyer-side U.S. land acquisition and public-data-first due diligence skill contracts
- Structured schemas for request normalization, subject resolution, parcel research, recommendation, and evaluation artifacts
- County/source registry foundations
- Phase-1 research, rendering, screening, shortlist, and evaluation scripts
- Fixture-backed example workspaces and the committed evaluation artifact

## Repository layout

The original path is preserved intentionally so the phase-1 scripts continue to work without invasive rewrites:

```text
DoWhiz_service/skills/alice-ai/
```

Important entrypoints:

- `DoWhiz_service/skills/alice-ai/SKILL.md`
- `DoWhiz_service/skills/alice-ai/scripts/validate_step11.py`
- `DoWhiz_service/skills/alice-ai/docs/alice_phase1_output.md`
- `DoWhiz_service/skills/alice-ai/docs/alice_phase2_backlog.md`

## Validation

From the repository root:

```bash
python3 DoWhiz_service/skills/alice-ai/scripts/validate_step11.py
```

If the committed normalized evaluation artifact needs to be refreshed:

```bash
python3 DoWhiz_service/skills/alice-ai/scripts/validate_step11.py --write-example
```

## Scope notes

- This is a phase-1 package, not a finished end-user product.
- The research flow is public-data-first and intentionally explicit about missing or conflicting evidence.
- Recommendation outputs rank only within the observed candidate universe captured by the examples and pipeline.
