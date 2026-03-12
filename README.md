# Genie Space Monitoring Demo

A Databricks notebook that builds a monitoring solution for [AI/BI Genie](https://docs.databricks.com/en/genie/index.html) spaces by combining **audit logs** with the **Genie Conversations API**.

## What it does

| Data Source | What It Provides |
|---|---|
| `system.access.audit` | Timestamps, user identity, feedback events, action types |
| Genie Conversations API | Question text, generated SQL, response content |
| Combined Delta Table | Everything above, persisted long-term for analytics |

The notebook produces a `conversation_log` Delta table with ready-to-use queries for monitoring adoption, quality, and performance of your Genie spaces.

## Quick Start

1. In your Databricks workspace, go to **Workspace** > your user folder
2. Click **⋮** > **Import**
3. Paste this URL: `https://github.com/ffgdeo/genie-space-monitoring-demo/blob/master/genie_monitoring.ipynb`
4. Fill in the widget parameters (catalog, monitoring schema, Genie space ID)
5. Run all cells

## Prerequisites

- **CAN MANAGE** permission on the Genie space
- Access to **`system.access.audit`** (Unity Catalog with audit log system table enabled)
- A catalog and schema where you can create monitoring tables
