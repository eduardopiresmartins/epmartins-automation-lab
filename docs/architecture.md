# Arquitetura

## Padrão adotado

Os três workflows seguem uma arquitetura simples e reaproveitável:

`Webhook de entrada -> Normalização dos dados -> Prompt estruturado -> Modelo de IA -> Parser estruturado -> Resposta JSON`

## Por que este desenho

Esse padrão foi escolhido porque ele:

- reduz complexidade para portfólio;
- facilita testes com payloads previsíveis;
- deixa o papel da IA explícito dentro do fluxo;
- torna simples a troca de provedor de modelo;
- facilita expansão futura com CRM, help desk, planilhas, e-mail ou banco de dados.

## Componentes principais

### 1. Webhook

Recebe o payload inicial da automação. Isso permite testar o fluxo com `curl`, Postman, frontends internos ou integrações de terceiros.

### 2. Normalização

O nó `Set` organiza os campos esperados pelo prompt. Isso reduz variações na entrada e melhora a consistência da resposta.

### 3. Prompt estruturado

O nó `Basic LLM Chain` concentra as instruções de negócio. Em vez de pedir apenas um texto livre, os prompts exigem saídas objetivas e orientadas a operação.

### 4. Modelo de IA

O modelo sugerido é `gpt-4o-mini`, mas o padrão pode ser substituído por outro modelo compatível com o n8n e com o custo esperado do projeto.

### 5. Parser estruturado

O `Structured Output Parser` obriga o modelo a devolver dados em formato previsível. Isso é importante para integrar a saída com sistemas posteriores.

### 6. Resposta final

O nó `Code` padroniza a resposta final com metadados úteis para debug, demonstração e integração.

## Possíveis extensões

- Persistir resultados em banco de dados.
- Enviar respostas para Slack, e-mail ou CRM.
- Adicionar validação de payload e tratamento de erro.
- Incluir logs de auditoria.
- Criar trilha de aprovação humana antes da ação final.
