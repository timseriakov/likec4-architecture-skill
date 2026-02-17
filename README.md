# likec4-architecture-skill

Agent Skill for architecture-as-code workflows with [LikeC4](https://likec4.dev/).

## Installation

### Option 1: Vercel Skills (`npx skills`)

```sh
npx skills add timseriakov/likec4-architecture-skill
```

### Option 2: Context7 Skills (`ctx7 skills`)

```sh
# inspect available skills in this repo
npx ctx7 skills info /timseriakov/likec4-architecture-skill

# install this skill
npx ctx7 skills install /timseriakov/likec4-architecture-skill likec4-architecture --universal
```

## What this skill does

- Creates and updates LikeC4 models (`.c4`/`.likec4`)
- Includes DSL quickstart and architecture patterns for model authoring
- Enforces validation-first workflow (`npx likec4 validate`)
- Produces preview/build/export commands for delivery
- Includes starter model template

## Skill structure

- `SKILL.md` - core instructions and trigger metadata
- `references/likec4-dsl-quickstart.md` - syntax and minimal examples
- `references/likec4-patterns.md` - practical architecture templates
- `references/likec4-capabilities-reference.md` - capability map + official docs index
- `references/likec4-checklist.md` - quality checklist
- `references/examples.md` - concrete usage examples
- `assets/likec4-starter/docs/architecture/model.c4` - starter model
- `agents/openai.yaml` - optional UI metadata

## Quick use

```sh
# copy starter model into current project
mkdir -p ./docs/architecture
cp ./assets/likec4-starter/docs/architecture/model.c4 ./docs/architecture/model.c4

# validate
npx likec4 validate

# preview
npx likec4 start
```

## Evaluations

See `evaluations/` for example evaluation scenarios to test behavior quality.

## License

MIT
