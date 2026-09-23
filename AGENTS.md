# AGENTS.md - Documentação Viva e Histórico de Releases

Este documento serve como fonte única da verdade (*Single Source of Truth*) para a arquitetura, diretrizes e histórico de versões do projeto de currículo e portfólio web de Uadson Emile Castro Feitosa, publicado via GitHub Pages e divulgado no LinkedIn.

---

## 1. Visão Geral do Projeto
- **Nome:** `me` (Currículo & Portfólio Técnico)
- **Autor:** Uadson Emile Castro Feitosa
- **Hospedagem:** GitHub Pages via GitHub Actions (`.github/workflows/static.yml`)
- **Foco Profissional:** Senior Software Engineer • Python & AI-Assisted Development • Integrações de Dados & Automações Resilientes.

---

## 2. Arquitetura e Tecnologias
- **Frontend / Marcação:** HTML5 semântico, estruturado e acessível.
- **Estilização:** [Tailwind CSS](https://tailwindcss.com) com suporte nativo e reativo a Modo Escuro (`dark:`) e Modo Claro, tipografia `Inter` e regras de impressão customizadas (`@page { size: A4 }` e `.no-print`) para exportação limpa em PDF.
- **Scripts:** JavaScript Vanilla para alternância e persistência de tema (`localStorage`) e atualização dinâmica do ano no rodapé.
- **CI/CD:** Pipeline automatizado no GitHub Actions disparado a cada push na branch `main`.

---

## 3. Histórico de Versões e Entregas

### [v1.0.0] - 23/09/2026 - Reformulação com foco em Desenvolvimento Assistido por IA
- **Novo Posicionamento Estratégico:**
  - Redefinição do headline para *Senior Software Engineer • Python & AI-Assisted Development*.
  - Ênfase na experiência com integrações de dados em larga escala (dados imobiliários municipais com a Receita Federal / SINTER - 480k+ req/dia).
  - Inclusão da abordagem prática de *Engenharia de Software Assistida por IA* e *Spec-Driven Development (SDD)* como acelerador de produtividade e qualidade.
- **Vitrine de Projetos Reais no GitHub:**
  - **JusNotify:** Automação de monitoramento processual no TJGO com contorno transparente de Cloudflare Turnstile, FastAPI, SQLite WAL, React e CI/CD com GHCR/Docker Swarm.
  - **Doc-Tool:** Gerador de pacotes documentais e contratos societários em DOCX nativo e PDF com FastAPI, Pydantic v2 e React.
  - **RPA & Financial Analytics:** Automação com Playwright, normalização e classificação histórica de rubricas financeiras e dashboard Glassmorphic.
  - **ZeCash:** PWA de gestão financeira pessoal com parser de extratos (OFX, CSV, PDF), SQLite WAL e rotinas de backup snapshot.
- **Seção "Como Eu Trabalho":**
  - Explicação concisa sobre Spec-Driven Development (`AGENTS.md`) e TDD com IA (`pytest` e `Vitest`).
- **Governança Git:**
  - Criação da branch de feature, merge na branch principal `main`, push remoto e geração da tag `v1.0.0`.
