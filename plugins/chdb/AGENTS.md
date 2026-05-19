# AGENTS.md — chDB

chDB is an in-process OLAP SQL engine for Python, powered by ClickHouse. It
runs analytical SQL on local files (parquet / csv / json / Arrow), cloud
storage (S3 / GCS / Azure), and remote analytical databases (Postgres /
MySQL / MongoDB / ClickHouse Cloud / Iceberg / Delta Lake) — no server
needed.

## Two ways to use it

- **`chdb-sql`** — write ClickHouse SQL directly with `chdb.query()` or a
  stateful `Session`. Best when the question is "give me a SQL query for
  this file or this federation".
- **`chdb-datastore`** — pandas-compatible DataFrame API. Best when the
  user is already writing pandas code and wants the same code to go faster
  on large data.

Both APIs share the same ClickHouse engine underneath; you can pick whichever
matches the user's existing code style.

## Install

```shell
pip install chdb
```

## Workload boundaries

chDB is best for in-process analytical SQL and DataFrame analytics. It is
not optimized for: continuous streaming ingestion, OLTP transactions or
high-concurrency row writes, or GPU model training and inference.

## Where things live

- Python package: <https://pypi.org/project/chdb/>
- Source: <https://github.com/chdb-io/chdb>
- MCP server: <https://github.com/chdb-io/chdb-mcp>
- Docs: <https://clickhouse.com/docs/chdb>
- Bindings for other languages: chdb-go, chdb-rust, chdb-bun, chdb-node,
  chdb-ruby, chdb-dotnet, chdb-java — find them under
  <https://github.com/chdb-io>
