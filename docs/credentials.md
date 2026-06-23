# Credenciais necessárias

## Visão geral

Os workflows deste laboratório evitam dependências desnecessárias e foram reduzidos ao conjunto mínimo para demonstração. Em todos os casos, a credencial principal é a do provedor de IA.

## Credenciais por tipo

- Chave de API do provedor de IA.
- URL pública do webhook do n8n, quando o workflow for consumido externamente.
- Credenciais opcionais de integrações adicionais, caso você queira expandir o fluxo para e-mail, CRM, help desk ou banco de dados.

## Credencial padrão do repositório

Nos arquivos `workflow.json`, o nó de modelo está configurado para usar uma credencial nomeada como `OpenAI account`. Você pode:

1. Criar essa credencial com o mesmo nome no n8n.
2. Ou abrir o nó e selecionar a credencial já existente no seu ambiente.

## Boas práticas

- Nunca versione tokens, segredos ou IDs sensíveis.
- Use variáveis de ambiente ou o cofre de credenciais do n8n.
- Registre no próprio workflow apenas placeholders, nunca valores reais.
- Se publicar capturas de tela do n8n, revise se não há identificadores expostos.
