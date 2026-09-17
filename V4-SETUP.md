# V4 Setup

## Requirements

OpenCode 1.18.9 and these model IDs:

- 9router/combo-opus
- 9router/combo-sonnet
- 9router/combo-gemini
- 9router/combo-free

## Install

Copy:
- `opencode.jsonc`
- `AGENTS.md`
- `.opencode/`

into the project root.

## Verify

```bash
opencode --version
opencode models 9router
opencode .
```

Inside OpenCode:

```text
/route Add a validation rule to the checkout API
```

Then:

```text
/feature Add a validation rule to the checkout API
```

## Important

The orchestrator is intentionally responsible for selecting which specialist agents to invoke. It should NOT invoke every specialist for every task.

Use the routing matrix in `.opencode/routing/ROUTING-MATRIX.md`.
