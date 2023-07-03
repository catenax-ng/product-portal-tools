# ReportPortal for Catena-X Portal

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://reportportal.github.io/kubernetes | reportportal | 5.8.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| reportportal.uat.superadminInitPasswd.auto | bool | `false` |  |
| reportportal.uat.superadminInitPasswd.password | string | `"<path:portal/data/reportportal/reportportal#password>"` |  |
| reportportal.ingress.enable | bool | `true` |  |
| reportportal.ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| reportportal.ingress.usedomainname | bool | `true` |  |
| reportportal.ingress.hosts[0] | string | `"portal-reportportal.dev.demo.catena-x.net"` |  |
| reportportal.ingress.tls[0].hosts[0] | string | `"portal-reportportal.dev.demo.catena-x.net"` |  |
| reportportal.ingress.tls[0].secretName | string | `"tls-secret"` |  |
| reportportal.rabbitmq.endpoint.address | string | `"reportportal-rabbitmq"` |  |
| reportportal.rabbitmq.endpoint.user | string | `"rabbitmq"` |  |
| reportportal.rabbitmq.endpoint.apiuser | string | `"rabbitmq"` |  |
| reportportal.rabbitmq.endpoint.password | string | `"<path:portal/data/reportportal/rabbitmq#rabbitmqPassword>"` |  |
| reportportal.postgresql.endpoint.address | string | `"reportportal-postgresql"` |  |
| reportportal.postgresql.endpoint.password | string | `"<path:portal/data/reportportal/postgresql#password>"` |  |
| reportportal.elasticsearch.endpoint | string | `"http://reportportal-elasticsearch:9200"` |  |
| reportportal.elasticsearch.password | string | `"<path:portal/data/reportportal/elasticsearch#password>"` |  |
| reportportal.minio.endpoint | string | `"http://reportportal-minio:9000"` |  |
| reportportal.minio.endpointshort | string | `"reportportal-minio:9000"` |  |
| reportportal.minio.accesskey | string | `"<path:portal/data/reportportal/minio#rootUser>"` |  |
| reportportal.minio.secretkey | string | `"<path:portal/data/reportportal/minio#rootPassword>"` |  |

