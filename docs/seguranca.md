# Segurança

## Segredos

- Nunca no repositório, nem em `.env` commitado.
- Use o gerenciador de segredos da plataforma (Vault, AWS Secrets Manager, Azure Key Vault).

## Dependências

- Dependabot/Renovate habilitado.
- CVEs críticas bloqueiam o merge.

## Imagens de container

- Imagem base mínima (distroless/UBI minimal).
- Usuário **não-root**.
- Scan com Trivy no CI.

!!! danger "Token vazou?"
    Revogue imediatamente, depois remova do histórico. Remover só o commit não basta.
