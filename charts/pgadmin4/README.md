# pgAdmin4 for Catena-X Portal

![Version: 1.1.0](https://img.shields.io/badge/Version-1.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://helm.runix.net | pgadmin4 | 1.15.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| pgadmin4.secret.password | string | `""` |  |
| pgadmin4.env.email | string | `"portal@catena-x.net"` |  |
| pgadmin4.existingSecret | string | `"secret-pgadmin4"` |  |
| pgadmin4.ingress.enabled | bool | `false` |  |
| pgadmin4.ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| pgadmin4.ingress.hosts[0].host | string | `"portal-pgadmin4.dummy"` |  |
| pgadmin4.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| pgadmin4.ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| pgadmin4.ingress.tls[0].hosts[0] | string | `"portal-pgadmin4.dummy"` |  |
| pgadmin4.ingress.tls[0].secretName | string | `"tls-secret"` |  |

