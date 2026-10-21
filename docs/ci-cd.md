# CI/CD

## Pipeline padrão

```text
PR ──▶ lint ─▶ testes ─▶ build imagem ─▶ scan ─▶ TechDocs build
main ─▶ (tudo acima) ─▶ push imagem ─▶ deploy dev ─▶ deploy staging ─▶ aprovação ─▶ prod
```

| Etapa | Ferramenta sugerida | Bloqueia o merge? |
|-------|---------------------|-------------------|
| Lint | ruff / eslint | Sim |
| Testes | pytest / jest | Sim |
| Scan de imagem | Trivy | Sim (CVEs críticas) |
| TechDocs | `techdocs-cli generate` | Sim |

## Ambientes

- **dev**: deploy automático a cada merge na `main`.
- **staging**: automático após dev verde.
- **prod**: aprovação manual, com janela e rollback documentados no runbook.

!!! note "Docs também passam pelo CI"
    O build do TechDocs roda no pipeline. Doc quebrada é build quebrado.
