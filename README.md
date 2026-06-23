# EPMartins Automation Lab

Laboratório de automações com IA e n8n para resolver problemas reais de negócio.

## Visão geral

Este repositório reúne workflows práticos de automação com IA, n8n e integrações orientados a cenários reais de operação, atendimento e e-commerce. A proposta é mostrar como combinar entrada estruturada, modelos de linguagem, regras de negócio e saídas acionáveis em fluxos simples de entender, testar e evoluir.

## Por que este projeto existe

Este projeto existe para demonstrar automação aplicada com foco em produto, integração entre APIs, uso pragmático de IA e documentação clara. Mais do que publicar arquivos JSON de n8n, a ideia é apresentar casos de uso com contexto de negócio, exemplos de entrada e saída e material suficiente para que outra pessoa entenda o valor da automação.

## Workflows disponíveis

| Workflow | Problema de negócio | Saída principal | Tecnologias | Status |
| --- | --- | --- | --- | --- |
| Product Description Generator | Criar descrições melhores para produtos de marketplace com mais rapidez. | Título otimizado, descrição comercial, benefícios, tags e sugestão de categoria. | n8n, modelo de IA, Webhook, JSON | MVP |
| Customer Email Summarizer | Reduzir o tempo gasto lendo e triando mensagens de clientes. | Resumo, assunto principal, sentimento, urgência e ação sugerida. | n8n, modelo de IA, e-mail/webhook, JSON | MVP |
| Ticket Urgency Classifier | Priorizar tickets de suporte com base em urgência e impacto no negócio. | Prioridade, urgência, impacto, sentimento e sugestão de encaminhamento. | n8n, modelo de IA, Webhook, JSON | MVP |

## Estrutura do repositório

```text
epmartins-automation-lab/
  README.md
  LICENSE
  .gitignore
  workflows/
    product-description-generator/
      workflow.json
      README.md
      sample-input.json
      sample-output.md
    customer-email-summarizer/
      workflow.json
      README.md
      sample-input.json
      sample-output.md
    ticket-urgency-classifier/
      workflow.json
      README.md
      sample-input.json
      sample-output.md
  docs/
    how-to-import.md
    credentials.md
    architecture.md
    roadmap.md
  assets/
    .gitkeep
```

## Como importar os workflows

O passo a passo está em [docs/how-to-import.md](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/docs/how-to-import.md).

## Credenciais necessárias

As credenciais e placeholders esperados estão em [docs/credentials.md](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/docs/credentials.md).

## Arquitetura

A visão geral da arquitetura dos fluxos está em [docs/architecture.md](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/docs/architecture.md).

## Roadmap

Os próximos passos planejados estão em [docs/roadmap.md](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/docs/roadmap.md).

## Créditos

Este projeto foi inspirado em templates abertos de automação da comunidade n8n, incluindo o repositório `wassupjay/n8n-free-templates`. Os workflows foram adaptados, curados e documentados como cases de portfólio orientados a problemas reais de negócio.

## Sobre mim

Criado por Eduardo Pires Martins — Desenvolvedor de Software com foco em backend, APIs, integrações, produtos digitais e tecnologia orientada a negócios.

Portfólio: https://www.epmartins.com.br  
LinkedIn: https://www.linkedin.com/in/eduardo-pires-martins/  
GitHub: https://github.com/eduardopiresmartins
