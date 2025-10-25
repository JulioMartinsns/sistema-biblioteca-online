# 3. GitHub Actions para CI/CD

Date: 2024-01-15

## Status

Accepted

## Context
O projeto necessita de uma pipeline de integração e entrega contínua que:
- Execute testes automaticamente a cada commit
- Garanta qualidade do código através de linting e análise estática
- Facilite o deployment em diferentes ambientes
- Seja de fácil configuração e manutenção

A equipe já utiliza GitHub para versionamento e colaboração.

## Decision
Adotar **GitHub Actions** como ferramenta principal de CI/CD.

## Consequences
**Positivas:**
- **Integração nativa** com repositórios GitHub
- **Configuração como código** via arquivos YAML
- **Marketplace** com ações pré-construídas
- **Gratuito** para repositórios públicos
- **Suporte a containers** e matrizes de build
- **Triggers flexíveis** (push, PR, schedule, etc.)

**Negativas:**
- **Vendor lock-in** com ecossistema GitHub
- **Limites de uso** para repositórios privados
- **Menos personalizável** que Jenkins em casos complexos
- **Dependência** da disponibilidade do GitHub

## Implementation
Será criado workflow em `.github/workflows/ci.yml` com:
- Testes unitários automatizados
- Análise estática de código
- Build da aplicação
- Notificações de status
