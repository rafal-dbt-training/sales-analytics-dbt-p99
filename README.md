# Sales Analytics — Native dbt on Snowflake

This is the single evolving project used throughout the nine-module course.

Project name: `sales_analytics`.

Each learner uses a unique, organiser-managed private GitHub repository.
For example, participant P01 uses `sales-analytics-dbt-p01`.

The instructor P99 reference uses `sales-analytics-dbt-p99`.

The dbt project lives at the repository root.

## Module 1 — Individual evidence

Complete the fields below using the seven-order K3 fixture.

Save your changes in your existing Git-connected Snowflake Workspace. Do not commit or push yet.

### M1-T1 — Fixture, DAG and grain

- Included valid order IDs: TODO
- Excluded order IDs and individual reasons: TODO
- Overall valid order count: TODO
- Overall valid revenue: TODO
- NORTH valid order count and revenue: TODO
- SOUTH valid order count and revenue: TODO
- Immediate parents of `fct_order`: TODO
- Direct downstream model of `fct_order`: TODO
- Grain of `fct_order`: TODO
- Grain of `mart_revenue_by_region`: TODO

### M1-Q — Knowledge check

- Q1 choice: TODO
- Q2 choice: TODO
- Q3 choice: TODO
- Q4 matching — W, P, R: TODO

## Module 2 starting files

- `dbt_project.yml`
- `profiles.yml`
- `models/sources.yml`

The organiser generates `profiles.yml` with the actual participant's
development role and schema.

The initial profile contains only the `dev` target.

## First model

In Module 2, personally create:

`models/staging/stg_customers.sql`

Required result:

- Snowflake VIEW in your assigned development schema.
- Exactly three customer rows.
- Exactly three columns: customer_id, customer_name, region.

The completed model SQL is not provided in the initial participant repository.

## Execution

In Snowflake Workspaces select:

- Project: `sales_analytics`
- Target: `dev`
- Runtime: dbt Core 1.12.3

Compile:

`dbt compile --select stg_customers --target dev`

Run:

`dbt run --select stg_customers --target dev`

## Git convention

Keep work in the existing Git-connected Workspace.

Do not commit or push during Modules 2–5.

Module 6 introduces `feature/initial-pipeline`, commit, push,
pull request, peer review and merge.

Do not create an unrelated repository or replacement project.

## Later stages

M3: Complete the five-model Sales Analytics pipeline.

M4: Data testing and troubleshooting.

M5: Documentation and lineage.

M6: Git collaboration.

M7: GitHub Actions CI.

M8: Production deployment and change management.

M9: End-to-end capstone.

## Security

Never commit credentials, private keys, passwords or access tokens.

The native dbt profile contains no real account, user or authentication secret; `account` and `user` hold the placeholder `not_needed`.

RAW tables are read-only.

Use only your assigned development schema.
