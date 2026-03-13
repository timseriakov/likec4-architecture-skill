# likec4-architecture Skill

This skill wraps the LikeC4 DSL so you can model, validate, and preview software architecture diagrams on demand. Use it whenever a task mentions architecture diagrams, C4/context/container/component views, system boundaries, dependency maps, or translating prose into executable architecture files.

## Overview

- Keep the model executable by focusing on specific views, reusing existing `.c4` or `.likec4` files, and validating every change with the CLI.
- Follow the workflow described in `SKILL.md`, commit only after validation passes, and use the provided starter kit when a view needs a fresh scaffold.

## Prerequisites

1. Install a Node.js runtime (v18 or newer recommended).
2. Make sure `npx likec4` is available (npm installs from the official `likec4` package).

## Installation

1. Clone this repository as the skill directory. The OpenCode/Codex Agent Skills registry looks under `~/.agents/skills/<name>/SKILL.md`, so the skill directory must be named `likec4-architecture`:
   ```sh
   git clone https://github.com/timseriakov/likec4-architecture-skill ~/.agents/skills/likec4-architecture
   ```
2. Confirm `~/.agents/skills/likec4-architecture/SKILL.md` exists; this is what OpenCode/Codex uses to detect metadata such as name, description, workflow, and commands.

## Usage

- Validate models before returning output:
  ```sh
  npx likec4 validate
  ```
- Preview the rendered architecture in the browser to check layout and labels:
  ```sh
  npx likec4 start
  ```
- When a user request wants finalized artifacts, capture them into distributable folders:
  ```sh
  npx likec4 build -o ./dist
  npx likec4 export png -o ./assets/architecture
  ```
  Use `build` to package text diagrams and `export` when the request expects PNG files.

## Repository layout

- `agents/` holds reusable helpers for jump-starting views and naming conventions.
- `assets/likec4-starter/` provides the bootstrap model template cited in `SKILL.md`; copy or customize it when no diagram yet exists.
- `references/likec4-checklist.md` lists the quality gates enforced by this skill.
- `scripts/bootstrap_likec4_starter.sh` seeds the starter model so you can quickly deliver consistent context and container diagrams.

## Skill discovery

OpenCode and Codex agents scan `~/.agents/skills/<name>/SKILL.md` whenever they look for a skill. Keeping `likec4-architecture/SKILL.md` in sync with this README ensures the metadata, workflow, and command list stay aligned for discovery, validation, and execution. Remember that the published repository is `timseriakov/likec4-architecture-skill`, but the skill name must remain `likec4-architecture` for toolchains to work.
