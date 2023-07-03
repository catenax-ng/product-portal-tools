# reportportal-minio

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

ReportPortal: Minio for Catena-X Portal

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://raw.githubusercontent.com/bitnami/charts/archive-full-index/bitnami | minio | 7.1.9 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| minio.global.minio.existingSecret | string | `"reportportal-minio"` |  |
| minio.fullnameOverride | string | `"reportportal-minio"` |  |
| secrets.auth.existingSecret.rootUser | string | `"<path:portal/data/reportportal/minio#rootUser>"` |  |
| secrets.auth.existingSecret.rootPassword | string | `"<path:portal/data/reportportal/minio#rootPassword>"` |  |

