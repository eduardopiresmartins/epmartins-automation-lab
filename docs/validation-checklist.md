# Checklist de validação

Este checklist reúne validações técnicas, cuidados de segurança e pontos de qualidade para manter o projeto consistente como peça de portfólio. A seção final concentra ações pessoais de divulgação, separadas da documentação pública principal do repositório.

## Validação dos workflows no n8n

- [ ] Importar `workflows/product-description-generator/workflow.json` no n8n.
- [ ] Configurar credencial do provedor de IA.
- [ ] Executar teste com `sample-input.json`.
- [ ] Conferir se a saída segue o formato esperado em `sample-output.md`.
- [ ] Repetir o processo para `customer-email-summarizer`.
- [ ] Repetir o processo para `ticket-urgency-classifier`.

## Segurança

- [ ] Confirmar que nenhum arquivo contém API keys, tokens ou secrets.
- [ ] Confirmar que prints não exibem credenciais ou identificadores sensíveis.
- [ ] Confirmar que os webhooks usam URLs genéricas na documentação.
- [ ] Confirmar que arquivos de ambiente local não foram versionados.

## Qualidade de portfólio

- [ ] Conferir se todos os links internos funcionam.
- [ ] Conferir se o README principal comunica valor em menos de 10 segundos.
- [ ] Conferir se cada workflow possui problema, solução, exemplo de entrada, exemplo de saída e nota de portfólio.
- [ ] Adicionar 1 a 3 prints reais dos workflows no n8n.

## Divulgação pessoal

- [ ] Fixar o repositório no perfil do GitHub.
- [ ] Preparar post de lançamento no LinkedIn.
- [ ] Incluir link do repositório no post.
- [ ] Explicar o projeto como laboratório de automações com IA e n8n.
- [ ] Destacar aprendizados técnicos e visão de produto.
