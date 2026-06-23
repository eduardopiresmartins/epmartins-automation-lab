# Ticket Urgency Classifier

## Problema de negócio

Tickets de suporte chegam com níveis diferentes de impacto, mas muitas vezes entram na fila sem contexto suficiente para priorização. Isso gera atraso no tratamento de incidentes críticos e sobrecarga em times de suporte e produto.

## Solução

Esta automação analisa o ticket recebido, estima urgência, impacto, sentimento e prioridade operacional, além de sugerir o encaminhamento mais adequado. O objetivo é apoiar a triagem inicial com mais consistência.

## Visão geral do fluxo

Entrada -> Processamento com IA -> Saída estruturada -> Próxima ação

O workflow recebe os dados do ticket via webhook, normaliza os campos essenciais, usa IA para classificar o caso e devolve um JSON que pode alimentar ferramentas de suporte, operação ou produto.

## Exemplo de entrada

Veja [sample-input.json](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/workflows/ticket-urgency-classifier/sample-input.json).

## Exemplo de saída

Veja [sample-output.md](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/workflows/ticket-urgency-classifier/sample-output.md).

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

- Integrar com Jira, Linear, Zendesk ou Freshdesk.
- Adicionar score de SLA em risco.
- Roteamento automático por squad ou especialidade.
- Enriquecer o ticket com histórico do cliente.
- Criar alçada automática para incidentes P1.

## Créditos

Inspirado e tecnicamente adaptado a partir do template aberto `ticket_urgency_classification.json` do repositório `wassupjay/n8n-free-templates`, com simplificação da arquitetura e foco em classificação operacional.
