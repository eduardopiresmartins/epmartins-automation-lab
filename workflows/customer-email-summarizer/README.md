# Customer Email Summarizer

## Problema de negócio

Times de atendimento e operações recebem mensagens longas, pouco objetivas e com diferentes níveis de urgência. Ler tudo manualmente atrasa triagem, resposta e priorização.

## Solução

Esta automação recebe o conteúdo de um e-mail ou mensagem de cliente, resume o caso, identifica o assunto principal, sentimento, urgência e sugere a próxima ação. Isso ajuda a organizar a fila e responder com mais contexto.

## Visão geral do fluxo

Entrada -> Processamento com IA -> Saída estruturada -> Próxima ação

O workflow recebe os dados via webhook, organiza remetente, assunto e corpo da mensagem, usa IA para produzir um resumo operacional e entrega a saída em JSON para uso em CRM, help desk ou fila interna.

## Preview do workflow

![Preview do Customer Email Summarizer](../../assets/customer-email-summarizer-workflow-success.png)

Visão do fluxo de triagem e resumo de mensagens de clientes, com normalização dos dados de entrada, análise semântica e resposta estruturada para atendimento.

## Exemplo de entrada

Veja [sample-input.json](sample-input.json).

## Exemplo de saída

Veja [sample-output.md](sample-output.md).

## Como usar

1. Importe o arquivo `workflow.json` no n8n.
2. Configure as credenciais.
3. Ajuste prompts ou variáveis, se necessário.
4. Execute um teste.
5. Ative o workflow.

## Como testar rapidamente

```bash
curl -X POST https://SEU_N8N/webhook/customer-email-summarizer \
  -H "Content-Type: application/json" \
  -d @sample-input.json
```

Substitua `https://SEU_N8N` pela URL da sua instância do n8n. Em ambiente local, use a URL gerada pelo próprio n8n para o webhook de teste ou produção.

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

## Nota de portfólio

Este workflow demonstra a capacidade de aplicar IA em triagem operacional e atendimento ao cliente. O case reforça competências em integração via webhook, normalização de dados, classificação semântica, geração de resumo e desenho de soluções que reduzem tempo operacional.

## Créditos

Inspirado e tecnicamente adaptado a partir do template aberto `summarize_customer_emails.json` do repositório `wassupjay/n8n-free-templates`, com foco em triagem operacional e documentação em PT-BR.
