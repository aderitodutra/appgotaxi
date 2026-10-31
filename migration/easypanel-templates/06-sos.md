# Template: SOS GoTaxi — sos.gotaxi.com.br (React + Vite)

Portal público de doações + área dos centros de recuperação/ONGs/institutos.
Usa a mesma API (`/api/sos`) e o mesmo banco. As tabelas `sos_*` são criadas sozinhas pela API.

## Tipo de serviço
**App → Github**

## Configuração (igual ao Admin, mudando só o WORKSPACE)

| Campo | Valor |
|---|---|
| Service Name | `gotaxi-sos` |
| Repository | o mesmo do Admin/PDV |
| Branch | `main` |
| Dockerfile Path | `migration/dockerfiles/Dockerfile.web` |
| Port | `80` |

### Build Args

```
WORKSPACE=sos
BASE_PATH=/
PORT=3000
```

## Domains

| Host | HTTPS | Path | Port |
|---|---|---|---|
| `sos.gotaxi.com.br` | ✅ Let's Encrypt | `/` | `80` |

## DNS

| Tipo | Nome | Valor |
|---|---|---|
| A | `sos` | `SEU_IP_VPS` |

## Depois do deploy
1. Faça também o deploy da **api** e do **admin** (eles têm as rotas e a tela SOS).
2. Super Admin → **SOS GoTaxi** → aba **Chave PIX**: cadastre a chave, o nome e a cidade da GoTaxi.
3. Teste: `https://sos.gotaxi.com.br` (público) e `https://sos.gotaxi.com.br/entrar` (centros).

## Resources
- CPU: 0.25 vCPU
- Memory: 128 MB
