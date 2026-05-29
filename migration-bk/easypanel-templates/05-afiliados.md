# Template: Afiliados Hub (React + Vite)

## Tipo de serviço
**App → Github**

## Configuração

| Campo | Valor |
|---|---|
| Service Name | `gotaxi-afiliados` |
| Repository | `genesiscompany/goplus` |
| Branch | `main` |
| Dockerfile Path | `migration/dockerfiles/Dockerfile.web` |
| Port | `80` |

### Build Args

```
WORKSPACE=afiliados-hub
GOOGLE_MAPS_KEY=AIzaSy...
BASE_PATH=/
PORT=3000
```

## Domains

| Host | HTTPS | Path | Port |
|---|---|---|---|
| `afiliados.gotaxi.com.br` | ✅ Let's Encrypt | `/` | `80` |

## Resources
- CPU: 0.5 vCPU
- Memory: 256 MB
