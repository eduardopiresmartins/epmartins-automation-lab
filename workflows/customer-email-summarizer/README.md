# Customer Email Summarizer

## Problema de negócio

Times de atendimento e operações recebem mensagens longas, pouco objetivas e com diferentes níveis de urgência. Ler tudo manualmente atrasa triagem, resposta e priorização.

## Solução

Esta automação recebe o conteúdo de um e-mail ou mensagem de cliente, resume o caso, identifica o assunto principal, sentimento, urgência e sugere a próxima ação. Isso ajuda a organizar a fila e responder com mais contexto.

## Visão geral do fluxo

Entrada -> Processamento com IA -> Saída estruturada -> Próxima ação

O workflow recebe os dados via webhook, organiza remetente, assunto e corpo da mensagem, usa IA para produzir um resumo operacional e entrega a saída em JSON para uso em CRM, help desk ou fila interna.

## Exemplo de entrada

Veja [sample-input.json](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/workflows/customer-email-summarizer/sample-input.json).

## Exemplo de saída

Veja [sample-output.md](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/workflows/customer-email-summarizer/sample-output.md).

## Como usar

1. Importe o arquivo `workflow.json` no n8n.
2. Configure as credenciais.
3. Ajuste prompts ou variáveis, se necessário.
4. Execute um teste.
5. Ative o workflow.

## Credenciais necessárias

- Chave de API do provedor de IA.
- URL de Webhook.
- Credenciais opcionais de integrações.

## Ideias de customização

- Enviar a saída automaticamente para Zendesk, Freshdesk ou HubSpot.
- Adicionar score de risco de churn.
- Criar rotas específicas por assunto.
- Sugerir respostas com tom da marca.
- Incluir histórico do cliente como contexto adicional.

## Créditos

Inspirado e tecnicamente adaptado a partir do template aberto `summarize_customer_emails.json` do repositório `wassupjay/n8n-free-templates`, com foco em triagem operacional e documentação em PT-BR.
