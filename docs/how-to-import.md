# Como importar os workflows no n8n

## Pré-requisitos

- Ter uma instância do n8n disponível, local ou em nuvem.
- Ter uma credencial de provedor de IA configurada no n8n.
- Ter acesso para criar e ativar webhooks.

## Passo a passo

1. Abra o n8n e clique em `Import from File`.
2. Escolha o arquivo `workflow.json` da automação desejada dentro da pasta `workflows/`.
3. Revise os nós de webhook, modelo e parser estruturado.
4. Configure a credencial do provedor de IA no nó `OpenAI Chat Model` ou adapte para o provedor da sua preferência.
5. Ajuste os prompts, limites e exemplos de schema se quiser refinar o comportamento para seu contexto.
6. Salve o workflow e execute um teste manual com o `sample-input.json` correspondente.
7. Ative o workflow quando a saída estiver consistente.

## Observações importantes

- Os fluxos deste repositório foram desenhados para serem claros e fáceis de adaptar.
- Nenhuma credencial real foi incluída.
- Os caminhos de webhook sugeridos são seguros para demonstração, mas devem ser revisados em produção.
- Se sua versão do n8n usar nomes ou versões ligeiramente diferentes para nós de IA, atualize os nós após a importação.
