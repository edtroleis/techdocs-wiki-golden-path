# Golden Path de Arquitetura

O **golden path** é o caminho pavimentado para criar e operar um serviço: as escolhas
padrão que a plataforma suporta, documenta e automatiza.

!!! tip "Não é obrigatório, é o caminho mais fácil"
    Você pode sair do golden path quando houver um bom motivo. Registre a decisão num ADR
    (veja a [Wiki de Engenharia](http://localhost:3000/docs/default/component/wiki-engineering/adrs/))
    e saiba que o suporte da plataforma será limitado.

## Quando seguir

- Novo serviço HTTP ou worker.
- Migração de um serviço legado para a plataforma.
- Revisão de prontidão antes de ir para produção.

## Como ler este guia

1. [Princípios](principios.md): o porquê das escolhas.
2. [Estrutura do serviço](estrutura-servico.md) e [CI/CD](ci-cd.md): como construir.
3. [Observabilidade](observabilidade.md) e [Segurança](seguranca.md): como operar.
4. [Checklist de produção](checklist.md): antes do primeiro deploy.

Exemplo de serviço que segue este golden path:
[demo-service](http://localhost:3000/catalog/default/component/demo-service).
