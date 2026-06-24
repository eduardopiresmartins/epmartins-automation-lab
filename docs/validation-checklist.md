# Checklist de validação

Este checklist reúne validações técnicas e cuidados de segurança para manter o projeto consistente como documentação pública e artefato profissional de portfólio.

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
