# 2. Banco de Dados PostgreSQL

Date: 2024-01-15

## Status

Accepted

## Context
O sistema de biblioteca online necessita armazenar dados estruturados com relacionamentos complexos:
- Usuários e seus perfis
- Livros com metadados e disponibilidade
- Empréstimos e histórico de devoluções
- Reservas e filas de espera

Requisitos não funcionais:
- Consistência transacional (ACID)
- Integridade referencial
- Backup e recuperação confiáveis
- Suporte a consultas complexas

## Decision
Adotar **PostgreSQL** como sistema de gerenciamento de banco de dados principal.

## Consequences
**Positivas:**
- **ACID compliance** garantindo consistência dos dados
- **Integridade referencial** nativa via chaves estrangeiras
- Suporte a **JSONB** para dados semi-estruturados
- **Comunidade ativa** e documentação extensa
- **Extensões** como Full-Text Search para buscas em texto
- Integração com ORMs populares (Django ORM, SQLAlchemy)

**Negativas:**
- **Complexidade de configuração** maior que SQLite
- Requer **servidor dedicado** ou container
- **Escalabilidade horizontal** mais complexa que NoSQL
- **Curva de aprendizado** para otimizações avançadas


