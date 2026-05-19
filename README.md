# chdb-agent-plugin

Cross-IDE agent plugin bundle for [chDB](https://chdb.io) — an in-process
ClickHouse SQL engine for Python. One repo distributes the chDB skill set,
MCP server, and project-level `AGENTS.md` to every major coding-agent IDE.

## Install

Pick your IDE — one command, same plugin:

```shell
# Claude Code
/plugin marketplace add chdb-io/chdb-agent-plugin
/plugin install chdb@chdb-agent-plugin

# Codex CLI (v0.121+)
codex marketplace add chdb-io/chdb-agent-plugin

# Copilot CLI
copilot plugin marketplace add chdb-io/chdb-agent-plugin

# Droid
droid plugin marketplace add chdb-io/chdb-agent-plugin
```

## What's inside

```
chdb-agent-plugin/
├── .claude-plugin/marketplace.json    # Anthropic Skills marketplace catalog
├── .codex-plugin/plugin.json          # OpenAI Codex Plugin Directory manifest
└── plugins/chdb/
    ├── plugin.json                    # Plugin metadata
    ├── AGENTS.md                      # Project-level agent instructions
    ├── skills/                        # chdb-datastore + chdb-sql skills
    └── mcp/                           # bundled chdb-mcp server config
```

The packaged plugin gives agents:

- **`chdb-sql`** — embedded ClickHouse SQL on parquet / csv / S3 / Postgres /
  MongoDB / ClickHouse Cloud / Iceberg / Delta Lake, with 1000+ functions
  (windowFunnel, geoToH3, JSON path ops, Session, parametrized queries) and
  cross-source joins via `s3()` / `mysql()` / `postgresql()` / `iceberg()` /
  `deltaLake()` / `remoteSecure()` table functions.
- **`chdb-datastore`** — pandas-API drop-in backed by the ClickHouse engine
  for DataFrame / parquet / csv / Arrow analytics with cross-source joins.
- **`chdb-mcp`** — MCP server exposing chDB query, file-attach, and remote
  ClickHouse Cloud federation tools.
- **`AGENTS.md`** — concise project-level instructions agents read at the
  start of every session.

## Status

🚧 Initial scaffold. Skill content and MCP wiring will be synced from
[`chdb-io/chdb`](https://github.com/chdb-io/chdb) and
[`chdb-io/chdb-mcp`](https://github.com/chdb-io/chdb-mcp) in follow-up PRs.

## License

Apache 2.0 — see [LICENSE](LICENSE).
