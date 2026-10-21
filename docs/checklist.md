# Checklist de produção

Antes do primeiro deploy em produção:

- [ ] `catalog-info.yaml` com owner, system e lifecycle corretos
- [ ] TechDocs com visão geral, arquitetura e **runbook**
- [ ] API registrada no catálogo (OpenAPI)
- [ ] `/health`, `/ready` e `/metrics` implementados
- [ ] Logs estruturados com `trace_id`
- [ ] Alertas de disponibilidade, erro e latência configurados
- [ ] Segredos fora do repositório
- [ ] Imagem roda como não-root e passa no scan
- [ ] Pipeline com testes, scan e build de docs
- [ ] Procedimento de rollback testado
