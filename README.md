# 🚀 AIO Empresarial

**Plataforma SaaS de Inteligência Operacional e Automação Empresarial.**

O **AIO Empresarial** é uma plataforma *Software as a Service (SaaS)* desenvolvida para centralizar informações corporativas, integrar sistemas, automatizar processos e apoiar decisões estratégicas por meio de dados e inteligência artificial.

O projeto adota uma arquitetura modular, escalável e multiempresa (*Multi-Tenant*), com foco em segurança, desempenho e facilidade de integração.

## 🛠️ Tecnologias

| Tecnologia | Finalidade |
|---|---|
| ☕ Java 21 | Linguagem principal do backend |
| 🍃 Spring Boot 4.2 | Framework da API REST |
| 🐘 PostgreSQL 17 | Banco de dados relacional |
| 🔄 Flyway | Versionamento do banco de dados |
| 🐳 Docker | Infraestrutura e containers |
| 📦 Maven | Gerenciamento de dependências |
| 🅰️ Angular | Interface web (planejada) |
| 🧠 Grok / xAI | Inteligência artificial (planejada) |
| 💬 WhatsApp API | Comunicação empresarial (planejada) |

## 🏗️ Arquitetura

O projeto utiliza uma arquitetura de **monólito modular**, organizada por domínios de negócio.

- **Backend:** APIs REST, regras de negócio e integrações.
- **Frontend:** painel administrativo e dashboards.
- **Database:** persistência relacional e migrations versionadas.
- **Multi-Tenancy:** isolamento de informações por empresa.
- **Intelligence:** análise de dados e automações inteligentes.
- **Integrations:** comunicação com ERPs, CRMs e serviços externos.

## 📂 Estrutura do projeto

| Diretório | Descrição |
|---|---|
| `backend/` | Aplicação Java com Spring Boot |
| `frontend/` | Aplicação web Angular (futura) |
| `infra/` | Infraestrutura Docker |
| `docs/` | Documentação técnica |

## ⚙️ Ambiente de desenvolvimento

**Pré-requisitos:** Java 21, Docker Desktop e Git.

**1. Configurar as variáveis locais**

Copie `.env.example` para `.env` e ajuste as credenciais.

**2. Iniciar o PostgreSQL**

`docker compose --env-file .env -f infra/compose.yaml up -d`

**3. Executar o backend**

A partir da pasta `backend/`:

`.\mvnw.cmd spring-boot:run`

**4. Executar os testes**

`.\mvnw.cmd clean verify`

**5. Verificar a API**

`GET http://localhost:8080/api/v1/ping`

O banco de dados é versionado automaticamente pelo Flyway durante a inicialização da aplicação.

## 🗺️ Roadmap

- [x] Estrutura inicial do projeto
- [x] Configuração Java e Spring Boot
- [x] PostgreSQL integrado ao Docker
- [x] Configuração do Flyway
- [x] Primeira migration do banco de dados
- [x] Endpoint de verificação da API
- [x] Build e testes iniciais
- [ ] Gerenciamento de empresas (Tenants)
- [ ] Autenticação e controle de acesso
- [ ] Arquitetura Multi-Tenant
- [ ] Interface administrativa Angular
- [ ] Integrações com sistemas empresariais
- [ ] Integração com inteligência artificial
- [ ] Assistente empresarial via WhatsApp
- [ ] Motor de automações e relatórios
- [ ] Implantação em produção

## 🔐 Segurança

As configurações sensíveis são gerenciadas por variáveis de ambiente. Credenciais, tokens e informações privadas não devem ser versionados no repositório.

Os mecanismos de autenticação, autorização e isolamento multiempresa serão implementados nas próximas etapas.

## 📌 Status

**🚧 Em desenvolvimento — Etapa 1 concluída.**

O projeto encontra-se em sua fase inicial de desenvolvimento e ainda não está preparado para utilização em produção.

---

**AIO Empresarial** — Transformando dados em inteligência operacional.