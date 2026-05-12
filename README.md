# Workshop: Pipeline CI/CD com GitHub Actions

Este repositório contém a estrutura evolutiva de um pipeline de automação, focado em boas práticas de DevOps e DataOps. O objetivo é demonstrar como garantir a integridade de arquivos e automatizar a entrega em produção com segurança.

## Estrutura dos Workflows

Os arquivos estão organizados na pasta `.github/workflows/` para facilitar o aprendizado em três etapas:

### 01. Integração Contínua (CI) - `01-ci.yaml`

- **O que faz:** Valida automaticamente se o arquivo `index.html` existe e está no local correto sempre que ocorre um push.
- **Gatilho:** Automático em arquivos `.html`.
- **Conceito:** Garantia de qualidade imediata (Fail Fast).

### 02. Entrega Contínua (CD) - `02-cd.yaml`

- **O que faz:** Realiza o deploy manual para o GitHub Pages.
- **Gatilho:** Manual via botão `Run workflow`.
- **Conceito:** Governança e controle humano sobre o ambiente de produção.

### 03. Pipeline Full CI/CD - `03-pipeline-full.yaml`

- **O que faz:** Une os dois processos em um fluxo orquestrado.
- **Fluxo Visual:** Utiliza o modelo de matriz para testar em múltiplos sistemas operacionais (Ubuntu e Windows).
- **Segurança:** O Deploy só é liberado se todos os testes da matriz passarem (`needs: build_and_test`) e requer aprovação manual no ambiente `production`.

## Tecnologias Utilizadas

- **GitHub Actions:** Orquestração do pipeline.
- **GitHub Pages:** Hospedagem do ambiente de produção.
- **YAML:** Linguagem de configuração dos fluxos.


---

**Instrutora:** Prof.ª Debora Batista S. Paulo  
**Instituição:** MBA Mackenzie / Centro Paula Souza