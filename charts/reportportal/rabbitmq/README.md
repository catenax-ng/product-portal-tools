# reportportal-rabbitmq

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

ReportPortal: RabbitMQ for Catena-X Portal

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | rabbitmq | 10.3.9 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| rabbitmq.fullnameOverride | string | `"reportportal-rabbitmq"` |  |
| rabbitmq.auth.existingPasswordSecret | string | `"reportportal-rabbitmq"` |  |
| rabbitmq.auth.existingErlangSecret | string | `"reportportal-rabbitmq"` |  |
| rabbitmq.auth.username | string | `"rabbitmq"` |  |
| secrets.auth.existingSecret.rabbitmqPassword | string | `"<path:portal/data/reportportal/rabbitmq#rabbitmqPassword>"` |  |
| secrets.auth.existingSecret.rabbitmqErlangCookie | string | `"<path:portal/data/reportportal/rabbitmq#rabbitmqErlangCookie>"` |  |

