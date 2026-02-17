# likec4-architecture-skill

Reusable Agent Skill for architecture-as-code workflows with [LikeC4](https://likec4.dev/).

## What this skill does

- Creates and updates LikeC4 models (`.c4`/`.likec4`)
- Enforces validation-first workflow (`npx likec4 validate`)
- Produces preview/build/export commands for delivery
- Includes starter template and bootstrap script

## Skill structure

- `SKILL.md` - core instructions and trigger metadata
- `references/likec4-checklist.md` - quality checklist
- `references/examples.md` - concrete usage examples
- `assets/likec4-starter/docs/architecture/model.c4` - starter model
- `scripts/bootstrap_likec4_starter.sh` - copy starter into a repo
- `agents/openai.yaml` - optional UI metadata

## Quick use

```sh
# copy starter model into current project
./scripts/bootstrap_likec4_starter.sh .

# validate
npx likec4 validate

# preview
npx likec4 start
```

## Evaluations

See `evaluations/` for example evaluation scenarios to test behavior quality.

## License

MIT
