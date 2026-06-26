# Plugins

This directory hosts product-specific **plugins** — packaged Skills and (where
applicable) MCP servers — for Google products.

Plugins are surfaced to AI coding agents (Antigravity CLI, Claude Code, Codex)
through marketplace manifests at the root of this repository:

- [`plugins/`](../plugins/) — Antigravity CLI
- [`.claude-plugin/marketplace.json`](../.claude-plugin/marketplace.json) — Claude Code
- [`.agents/plugins/marketplace.json`](../.agents/plugins/marketplace.json) — Codex

## Installation

<details>
<summary><h3>Antigravity CLI</h3></summary>

Antigravity CLI installs plugins directly from remote GitHub repositories.

```bash
agy plugins install https://github.com/google/skills/plugins/<plugin>
```

</details>

<details>
<summary><h3>Claude Code</h3></summary>

Claude Code resolves plugins through a marketplace manifest. Install the
`google-plugins` marketplace once, then install any plugin from it:

```bash
# Step 1. Add the marketplace
## Option A — from the shell
claude plugin marketplace add google/skills

## Option B — from within Claude Code
/plugin marketplace add https://github.com/google/skills.git

# Step 2. Install a plugin
claude
/plugin install <plugin-name>@google-plugins

# Step 3. Reload plugins
/reload-plugins

# Optional. Update the marketplace
claude plugin marketplace update google-plugins
```

</details>

<details>
<summary><h3>OpenAI Codex</h3></summary>

Codex uses an equivalent marketplace mechanism:

```bash
# Step 1. Add the marketplace
codex plugin marketplace add google/skills

# Step 2. Install a plugin
codex plugin install <plugin-name>@google-plugins

# Optional. Update the marketplace
codex plugin marketplace upgrade google-plugins
```

</details>

## Individual Plugins

| Product | Upstream | Description |
| :--- | :--- | :--- |
| **Data Agent Kit Starter Pack** | [gemini-cli-extensions/data-agent-kit-starter-pack](https://github.com/gemini-cli-extensions/data-agent-kit-starter-pack) | Specialized suite of skills for data engineers and database practitioners on Google Cloud — architect data pipelines, transform data with dbt, write Spark and BigQuery SQL notebooks, and orchestrate end-to-end workflows. |
| **AlloyDB for PostgreSQL** | [gemini-cli-extensions/alloydb](https://github.com/gemini-cli-extensions/alloydb) | Create, connect, and interact with an AlloyDB for PostgreSQL database and data. |
| **AlloyDB Omni** | [gemini-cli-extensions/alloydb-omni](https://github.com/gemini-cli-extensions/alloydb-omni) | Create, connect, and interact with an AlloyDB Omni database and data. |
| **BigQuery** | [gemini-cli-extensions/bigquery-data-analytics](https://github.com/gemini-cli-extensions/bigquery-data-analytics) | Data Analytics skills for BigQuery. |
| **Bigtable** | [GoogleCloudPlatform/cloud-bigtable-ecosystem](https://github.com/GoogleCloudPlatform/cloud-bigtable-ecosystem) | Connect, query, and interact with Cloud Bigtable. |
| **Cloud SQL for MySQL** | [gemini-cli-extensions/cloud-sql-mysql](https://github.com/gemini-cli-extensions/cloud-sql-mysql) | Connect and interact with a Cloud SQL for MySQL database and data. |
| **Cloud SQL for PostgreSQL** | [gemini-cli-extensions/cloud-sql-postgresql](https://github.com/gemini-cli-extensions/cloud-sql-postgresql) | Create, connect, and interact with a Cloud SQL for PostgreSQL database and data. |
| **Cloud SQL for SQL Server** | [gemini-cli-extensions/cloud-sql-sqlserver](https://github.com/gemini-cli-extensions/cloud-sql-sqlserver) | Connect to Cloud SQL for SQL Server. |
| **Dataproc** | [gemini-cli-extensions/dataproc](https://github.com/gemini-cli-extensions/dataproc) | Skills for Dataproc. |
| **Firestore** | [gemini-cli-extensions/firestore-native](https://github.com/gemini-cli-extensions/firestore-native) | Connect and interact with Cloud Firestore. |
| **Google Cloud Storage** | [gemini-cli-extensions/google-cloud-storage](https://github.com/gemini-cli-extensions/google-cloud-storage) | Vetted Google Cloud Storage skills for your coding agent. |
| **Knowledge Catalog** | [gemini-cli-extensions/knowledge-catalog](https://github.com/gemini-cli-extensions/knowledge-catalog) | Skills for Knowledge Catalog. |
| **Looker** | [gemini-cli-extensions/looker](https://github.com/gemini-cli-extensions/looker) | Connect to Looker. |
| **Oracle Database** | [gemini-cli-extensions/oracledb](https://github.com/gemini-cli-extensions/oracledb) | Connect, query, and interact with Oracle Databases and their data. |
| **Spanner** | [gemini-cli-extensions/spanner](https://github.com/gemini-cli-extensions/spanner) | Connect and interact with Spanner data using natural language. |
