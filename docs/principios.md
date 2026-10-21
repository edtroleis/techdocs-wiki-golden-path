# Princípios

| # | Princípio | Na prática |
|---|-----------|------------|
| 1 | **Você constrói, você opera** | O time dono do serviço recebe os alertas |
| 2 | **Tudo como código** | Infra, pipeline, dashboards e alertas versionados |
| 3 | **Stateless por padrão** | Estado em bancos/filas gerenciados, nunca no disco do pod |
| 4 | **Contratos explícitos** | Toda API tem OpenAPI/AsyncAPI registrado no catálogo |
| 5 | **Seguro por padrão** | Sem segredos no repo; menor privilégio |
| 6 | **Observável desde o dia 1** | Logs estruturados, métricas RED e traces |
| 7 | **Docs junto do código** | `docs/` + TechDocs no mesmo repo do serviço |
