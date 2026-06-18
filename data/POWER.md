---
name: "Data"
displayName: "Data"
description: "Transform your AI assistant into a data analyst collaborator. SQL queries, data exploration, visualization, dashboards, and insight generation across any data warehouse or analytics stack."
keywords: ["data", "sql", "analytics", "warehouse", "visualization", "dashboard", "bigquery", "snowflake", "postgres", "databricks", "redshift", "charts", "statistics", "data-quality"]
author: "NUX DESIGN"
---

# Data Analyst Power

Transform your AI assistant into a data analyst collaborator. SQL queries, data exploration, visualization, dashboards, and insight generation. Works with any data warehouse, any SQL dialect, and any analytics stack.

## Available Steering Files

- **sql-and-analysis.md** - SQL best practices across dialects, query writing, data exploration, and analysis workflows
- **visualization-and-dashboards.md** - Chart selection, Python viz patterns, interactive HTML dashboard construction
- **validation-and-statistics.md** - Pre-delivery QA, statistical methods, outlier detection, hypothesis testing

## Available MCP Servers

### Data Warehouse Connections

This power works best when connected to your data infrastructure. Configure MCP servers for:

- **Data Warehouse**: Snowflake, Databricks, BigQuery, Definite, PostgreSQL, Redshift
- **Product Analytics**: Amplitude, Mixpanel
- **Project Tracker**: Atlassian (Jira/Confluence)
- **Notebooks**: Hex, Jupyter

## Configuration

### MCP Servers

Pre-configured servers are in `mcp.json`. Add your data warehouse URL or configure additional servers as needed.

| Server | URL | Notes |
|--------|-----|-------|
| BigQuery | `https://bigquery.googleapis.com/mcp` | Google Cloud |
| Amplitude | `https://mcp.amplitude.com/mcp` | US region |
| Amplitude EU | `https://mcp.eu.amplitude.com/mcp` | EU region |
| Atlassian | `https://mcp.atlassian.com/v1/mcp` | Jira/Confluence |
| Hex | `https://app.hex.tech/mcp` | Notebooks |
| Definite | `https://api.definite.app/v3/mcp/http` | Analytics |
| Snowflake | *(configure your URL)* | |
| Databricks | *(configure your URL)* | |

### Without a Data Warehouse Connection

Paste SQL results or upload CSV/Excel files for analysis and visualization. The agent can write SQL queries for you to run manually, then analyze the results you provide.

## Quick Start

1. Connect your data warehouse MCP server (or work with pasted data)
2. Ask questions naturally:
   - "What was our monthly revenue trend for the past 12 months?"
   - "Explore the users table"
   - "Write a cohort retention query for Snowflake"
   - "Build a sales dashboard from this CSV"
   - "Validate my analysis before I present it"


