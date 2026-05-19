# chdb plugin

Bundled chDB agent assets — skills, MCP server config, and project-level
`AGENTS.md`. Installed automatically when you add this plugin from the
parent marketplace.

## Contents

- `skills/chdb-datastore/` — pandas-API DataFrame analytics on the
  ClickHouse engine (synced from chdb-io/chdb)
- `skills/chdb-sql/` — embedded ClickHouse SQL on files, cloud storage,
  and remote databases (synced from chdb-io/chdb)
- `mcp/chdb-mcp.json` — `chdb-mcp` server config (`pip install chdb-mcp`
  then point your agent at this config)
- `AGENTS.md` — project-level agent instructions

## Status

🚧 Skill content and MCP wiring are placeholders — initial sync from
`chdb-io/chdb` and `chdb-io/chdb-mcp` is the next step.

See the [parent README](../../README.md) for install commands across IDEs.
