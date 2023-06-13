# ReportPortal for Catena-X Portal

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

## Requirements

| Repository                                                                  | Name          | Version |
|-----------------------------------------------------------------------------|---------------|---------|
| https://reportportal.github.io/kubernetes                                   | reportportal  | 5.7.4   |
| https://helm.elastic.co                                                     | elasticsearch | 8.5.1   |
| https://charts.bitnami.com/bitnami                                          | minio         | 12.6.4  |
| https://raw.githubusercontent.com/bitnami/charts/archive-full-index/bitnami | postgresql    | 12.5.6  |
| https://charts.bitnami.com/bitnami                                          | rabbitmq      | 12.0.0  |

## Values ReportPortal

| Key                                                            | Type   | Default                                                             | Description |
|----------------------------------------------------------------|--------|---------------------------------------------------------------------|-------------|
| reportportal.secret.password                                   | string | `""`                                                                |  |
| reportportal.existingSecret                                    | string | `"secret-reportportal"`                                             |  |
| reportportal.ingress.enabled                                   | bool   | `false`                                                             |  |
| reportportal.ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"`                                                           |  |
| reportportal.ingress.hosts[0].host                             | string | `"portal-reportportal.dummy"`                                       |  |
| reportportal.ingress.hosts[0].paths[0].path                    | string | `"/"`                                                               |  |
| reportportal.ingress.hosts[0].paths[0].pathType                | string | `"Prefix"`                                                          |  |
| reportportal.ingress.tls[0].hosts[0]                           | string | `"portal-reportportal.dummy"`                                       |  |
| reportportal.ingress.tls[0].secretName                         | string | `"tls-secret"`                                                      |  |
| reportportal.rabbitmq.Secretname                               | string | `"reportportal-rabbitmq"`                                           |  |
| reportportal.rabbitmq.endpoint.address                         | string | `"reportportal-rabbitmq"`                                           |  |
| reportportal.rabbitmq.endpoint.user                            | string | `"rabbitmq"`                                                        |  |
| reportportal.rabbitmq.endpoint.apiuser                         | string | `"rabbitmq"`                                                        |  |
| reportportal.postgresql.Secretname                             | string | `""`                                                                |  |
| reportportal.postgresql.endpoint.address                       | string | `"reportportal-postgresql"`                                         |  |
| reportportal.postgresql.endpoint.password                      | string | `""`                                                                |  |
| reportportal.elasticsearch.endpoint                            | string | `"http://elasticsearch-master.reportportal.svc.cluster.local:9200"` |  |
| reportportal.minio.secretName                                  | string | `"reportportal-minio"`                                              |  |
| reportportal.minio.endpoint                                    | string | `"http://minio.reportportal.svc.cluster.local:9000"`                |  |
| reportportal.minio.endpointshort                               | string | `"minio.reportportal.svc.cluster.local:9000"`                       |  |
| reportportal.minio.accesskeyName                               | string | `"root-user"`                                                       |  |
| reportportal.minio.secretkeyName                               | string | `"root-password"`                                                   |  |

## Values Elasticsearch

| Key                                                            | Type | Default | Description |
|----------------------------------------------------------------|------|---------|-------------|
| elasticsearch.replicas                                         | int  | `1`     |  |

## Values Minio

| Key                                      | Type   | Default                                                             | Description |
|------------------------------------------|--------|---------------------------------------------------------------------|-------------|
| minio.auth.existingSecret                | string | `"reportportal-minio"`                                              |  |
| secrets.auth.existingSecret.rootPassword | string | `""`                                              |  |
| secrets.auth.existingSecret.rootUser     | string | `""`                                              |  |

## Values Postgresql

| Key                                          | Type   | Default                                                                                                                          | Description |
|----------------------------------------------|--------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| postgresql.serviceAcount.enabled             | bool   | `true`                                                                                                                           |            |
| postgresql.auth.username                     | string | `"rpuser"`                                                                                                                       |            |
| postgresql.auth.database                     | string | `"reportportal"`                                                                                                                 |            |
| postgresql.auth.existingSecret               | string | `"reportportal-postgresql"`                                                                                                      |            |
| postgresql.initdbScripts.init_postgres.sh    | string | `"\| #!/bin/sh /opt/bitnami/postgresql/bin/psql -U postgres -d ${POSTGRES_DB}"`                                                  |            |
|                                              |        | `"-c 'CREATE EXTENSION IF NOT EXISTS ltree; CREATE EXTENSION IF NOT EXISTS pgcrypto; CREATE EXTENSION IF NOT EXISTS pg_trgm;'"`  |            |
| secrets.auth.existingSecret.postgresPassword | string | `""`                                                                                                                       |            |
| secrets.auth.existingSecret.password         | string | `""`                                                                                                                       |            |

## Values Rabbitmq

| Key                                              | Type   | Default                   | Description |
|--------------------------------------------------|--------|---------------------------|-------------|
| rabbitmq.auth.existingPasswordSecret             | string | `"reportportal-rabbitmq"` |  |
| rabbitmq.auth.existingErlangSecret               | string | `"reportportal-rabbitmq"` |  |
| secrets.auth.existingSecret.rabbitmqPassword     | string | `""`                      |  |
| secrets.auth.existingSecret.rabbitmqErlangCookie | string | `""`                      |  |