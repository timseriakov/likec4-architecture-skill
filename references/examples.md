# Examples

## Example 1: New architecture model

User request:
"Create a context and container architecture diagram for our billing platform."

Expected behavior:
- Create or update `.c4` files.
- Include context and container views.
- Add clear relationships and labels.
- Run `npx likec4 validate`.
- Return preview command.

## Example 2: Architecture update after code change

User request:
"We added an async worker and Redis queue. Update the architecture."

Expected behavior:
- Add worker and queue elements.
- Update relationships (`API -> Queue`, `Worker -> Queue`, `Worker -> DB`).
- Keep existing IDs stable when possible.
- Revalidate with CLI.

## Example 3: Export for docs

User request:
"Export architecture diagrams for docs and CI artifacts."

Expected behavior:
- Keep model unchanged unless needed.
- Provide `npx likec4 build -o ./dist`.
- Provide `npx likec4 export png -o ./assets/architecture`.
- Confirm validation status before export.
