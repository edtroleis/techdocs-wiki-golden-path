# Estrutura do serviço

## Layout do repositório

```text
meu-servico/
├── catalog-info.yaml     # registro no Backstage
├── mkdocs.yml            # TechDocs
├── docs/                 # documentação
├── openapi.yaml          # contrato da API
├── src/ ou app/          # código
├── tests/
├── Containerfile
└── .github/workflows/    # CI
```

## Configuração (12-factor)

- Configuração por **variáveis de ambiente**, nunca hardcoded.
- Um artefato (imagem) promovido entre ambientes; só a config muda.
- Logs em `stdout`, em JSON.

```yaml
# exemplo de config por ambiente
env:
  - name: LOG_LEVEL
    value: info
  - name: DATABASE_URL
    valueFrom:
      secretKeyRef: { name: meu-servico, key: database-url }
```

## Endpoints obrigatórios

| Endpoint | Uso |
|----------|-----|
| `/health` (ou `/healthz`) | Liveness |
| `/ready` | Readiness |
| `/metrics` | Métricas Prometheus |
