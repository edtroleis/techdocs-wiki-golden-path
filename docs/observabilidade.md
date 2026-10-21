# Observabilidade

## Os três sinais

| Sinal | Padrão | Ferramenta |
|-------|--------|------------|
| Logs | JSON em stdout, com `trace_id` | Loki / ELK |
| Métricas | RED (Rate, Errors, Duration) | Prometheus + Grafana |
| Traces | OpenTelemetry | Tempo / Jaeger |

## Log estruturado

```json
{"ts":"2026-10-21T12:00:00Z","level":"info","msg":"item created","item_id":1,"trace_id":"abc123"}
```

## Alertas mínimos

- Serviço fora do ar (health check).
- Taxa de erro 5xx acima do SLO.
- Latência p95 acima do SLO.

Todo alerta tem link para o **runbook** do serviço no TechDocs.
