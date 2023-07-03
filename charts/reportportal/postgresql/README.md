# reportportal-postgresql

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

ReportPortal: Postgresql for Catena-X Portal

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://raw.githubusercontent.com/bitnami/charts/archive-full-index/bitnami | postgresql | 10.9.4 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| postgresql.fullnameOverride | string | `"reportportal-postgresql"` |  |
| postgresql.serviceAccount.enabled | bool | `true` |  |
| postgresql.global.postgresql.postgresqlUsername | string | `"rpuser"` |  |
| postgresql.global.postgresql.postgresqlDatabase | string | `"reportportal"` |  |
| postgresql.global.postgresql.existingSecret | string | `"reportportal-postgresql"` |  |
| postgresql.initdbScripts."init_postgres.sh" | string | `"#!/bin/sh\n/opt/bitnami/postgresql/bin/psql -U postgres -d ${POSTGRES_DB} -c 'CREATE EXTENSION IF NOT EXISTS ltree; CREATE EXTENSION IF NOT EXISTS pgcrypto; CREATE EXTENSION IF NOT EXISTS pg_trgm;'\n"` |  |
| secrets.auth.existingSecret.postgresPassword | string | `"<path:portal/data/reportportal/postgresql#postgresPassword>"` |  |
| secrets.auth.existingSecret.password | string | `"<path:portal/data/reportportal/postgresql#password>"` |  |

