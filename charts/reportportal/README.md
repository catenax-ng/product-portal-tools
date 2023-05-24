# ReportPortal for Catena-X Portal

![Version: 1.1.0](https://img.shields.io/badge/Version-1.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://helm.runix.net | reportportal | 1.11.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| reportportal.secret.password | string | `""` |  |
| reportportal.env.email | string | `"portal@catena-x.net"` |  |
| reportportal.existingSecret | string | `"secret-reportportal"` |  |
| reportportal.ingress.enabled | bool | `false` |  |
| reportportal.ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| reportportal.ingress.hosts[0].host | string | `"portal-reportportal.dummy"` |  |
| reportportal.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| reportportal.ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| reportportal.ingress.tls[0].hosts[0] | string | `"portal-reportportal.dummy"` |  |
| reportportal.ingress.tls[0].secretName | string | `"tls-secret"` |  |

