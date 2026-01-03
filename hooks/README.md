# Hooks

This folder contains hook scripts that run before/after Claude executes tools.

**Modules:** 9-12 (Introducing, Defining, Implementing, Useful Hooks)

**How it works:**
- Scripts receive JSON via stdin with tool_name and input
- Exit 0 = allow, Exit 2 = block (pre-tool only)
- stderr output = feedback to Claude
- Configure in `.claude/settings.local.json`

**Planned hooks:**
- `read_hook.js` - Block access to .env files
- `typecheck_hook.js` - Run tsc after TypeScript edits
- `log_hook.js` - Debug logging for tool calls
