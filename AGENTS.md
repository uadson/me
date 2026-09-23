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
- **Frontend / Marcação:** HTML5 semântico, estruturado e acessível com suporte internacional nativo (PT-BR e EN).
- **Estilização:** [Tailwind CSS](https://tailwindcss.com) com suporte nativo e reativo a Modo Escuro (`dark:`) e Modo Claro, tipografia `Inter` e regras de impressão customizadas (`@page { size: A4 }` e `.no-print`) para exportação limpa em PDF.
- **Mecanismo de Internacionalização (i18n):**
  - Controle declarativo baseado no atributo `lang` da tag `html` via seletores CSS puros (`html[lang="pt-BR"] .lang-en { display: none !important; }` e `html[lang="en"] .lang-pt { display: none !important; }`).
  - Seletor de idioma interativo no topo da página (`🇧🇷 PT` / `🇺🇸 EN`) com persistência em `localStorage` e detecção via URL (`?lang=en` ou `?lang=pt`).
  - Dropdown inteligente de download de PDF permitindo exportar diretamente o currículo na versão em Português ou na versão em Inglês via `window.print()`.
  - Ponto de entrada `/en/` (`en/index.html`) para redirecionamento transparente a recrutadores internacionais.
- **CI/CD:** Pipeline automatizado no GitHub Actions disparado a cada push na branch `main`.

---

## 3. Histórico de Versões e Entregas

### [v1.1.0] - 23/09/2026 - Suporte Bilíngue (PT/EN) e Download Customizado em PDF
- **Internacionalização Completa (PT e EN):**
  - Tradução técnica integral de todas as seções (Resumo Profissional, Habilidades, Experiência, Projetos, Metodologia, Educação e Contato).
  - Adição de seletor de idiomas interativo `[ 🇧🇷 PT | 🇺🇸 EN ]` na barra superior.
  - Dropdown no botão de download permitindo baixar o PDF em Português ou em Inglês.
  - Criação da rota `/en/` para acesso direto à versão em inglês.
- **Governança Git:**
  - Criação da branch `feature/i18n-pdf-download-pt-en`, merge na `main`, tag `v1.1.0` e push remoto.

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
