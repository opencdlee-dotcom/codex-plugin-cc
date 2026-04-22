# Codex Plugin for Claude Code — Project Memory

## Quick Context

- **Project**: `@openai/codex-plugin-cc`
- **Type**: TypeScript plugin
- **Goal**: Let Claude Code invoke Codex for review and delegated task workflows
- **Location**: `/Users/user/Documents/Work & Projects/VSCode Projects/codex/codex-plugin-cc/`

## Architecture & Patterns

- **Build config**: `tsconfig.app-server.json`
- **Plugin payload**: `plugins/codex/` (commands, hooks, prompts, scripts, skills)
- **Generated types**: `plugins/codex/.generated/app-server-types/`
- **Tests**: `tests/*.test.mjs`
- **Docs**: [README.md](</Users/user/Documents/Work & Projects/VSCode Projects/codex/codex-plugin-cc/README.md>)

## Agent-Friendly Usage

- Install deps: `npm install`
- Build: `npm run build`
- Test: `npm test`
- Prebuild step generates app-server TS types before compilation

## Notes For LLM Agents

- This folder appears to be a standalone copy of the Codex plugin source; there is also a sibling checkout at `/Users/user/Documents/Work & Projects/VSCode Projects/codex-plugin-cc/`.
- Node 18.18+ is required.
- `npm run build` depends on the `codex` CLI being available on `PATH` because `prebuild` runs `codex app-server generate-ts`.
- When debugging build issues, check generated type output and the scripts under `plugins/codex/scripts/` first because that is the runtime heart of the plugin.
