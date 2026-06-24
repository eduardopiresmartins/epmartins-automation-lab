# Ticket Urgency Classifier

## Problema de negócio

Tickets de suporte chegam com níveis diferentes de impacto, mas muitas vezes entram na fila sem contexto suficiente para priorização. Isso gera atraso no tratamento de incidentes críticos e sobrecarga em times de suporte e produto.

## Solução

Esta automação analisa o ticket recebido, estima urgência, impacto, sentimento e prioridade operacional, além de sugerir o encaminhamento mais adequado. O objetivo é apoiar a triagem inicial com mais consistência.

## Visão geral do fluxo

Entrada -> Processamento com IA -> Saída estruturada -> Próxima ação

O workflow recebe os dados do ticket via webhook, normaliza os campos essenciais, usa IA para classificar o caso e devolve um JSON que pode alimentar ferramentas de suporte, operação ou produto.

## Preview do workflow

![Preview do Ticket Urgency Classifier](../../assets/ticket-urgency-classifier-workflow-success.png)

Visão do fluxo de classificação operacional de tickets, com análise de urgência, impacto e prioridade para apoiar a triagem inicial de suporte.

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
curl -X POST https://SEU_N8N/webhook/ticket-urgency-classifier \
  -H "Content-Type: application/json" \
  -d @sample-input.json
```

Substitua `https://SEU_N8N` pela URL da sua instância do n8n. Em ambiente local, use a URL gerada pelo próprio n8n para o webhook de teste ou produção.

## Credenciais necessárias

- Chave de API do provedor de IA.
- URL de Webhook.
- Credenciais opcionais de integrações.

## Ideias de customização

- Integrar com Jira, Linear, Zendesk ou Freshdesk.
- Adicionar score de SLA em risco.
- Roteamento automático por squad ou especialidade.
- Enriquecer o ticket com histórico do cliente.
- Criar alçada automática para incidentes P1.

## Nota de portfólio

Este workflow demonstra a capacidade de transformar tickets de suporte em informação priorizada para operação, produto e tecnologia. O case reforça competências em classificação de urgência, análise de impacto, roteamento operacional e uso de IA como apoio à tomada de decisão.

## Créditos

Inspirado e tecnicamente adaptado a partir do template aberto `ticket_urgency_classification.json` do repositório `wassupjay/n8n-free-templates`, com simplificação da arquitetura e foco em classificação operacional.
