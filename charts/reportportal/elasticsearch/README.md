# reportportal-elasticsearch

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

ReportPortal: Elasticsearch for Catena-X Portal

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://helm.elastic.co | elasticsearch | 8.5.1 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| elasticsearch.replicas | int | `1` |  |
| elasticsearch.secret.enabled | bool | `true` |  |
| elasticsearch.secret.password | string | `"<path:portal/data/reportportal/elasticsearch#password>"` |  |
| elasticsearch.fullnameOverride | string | `"reportportal-elasticsearch"` |  |

