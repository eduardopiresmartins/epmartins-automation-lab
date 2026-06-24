# Product Description Generator

## Problema de negócio

Pequenos e médios vendedores de marketplace costumam perder tempo escrevendo descrições manualmente ou publicando anúncios fracos, genéricos e pouco orientados à conversão. Isso impacta velocidade de cadastro, consistência da comunicação e potencial de venda.

## Solução

Esta automação recebe informações básicas do produto e devolve uma estrutura pronta para uso comercial: título otimizado, descrição comercial, bullets de benefícios, tags e sugestão de categoria. O objetivo é acelerar o cadastro de itens com um padrão mais profissional de copy.

## Visão geral do fluxo

Entrada -> Processamento com IA -> Saída estruturada -> Próxima ação

O workflow recebe os dados via webhook, normaliza os campos principais, envia um prompt com contexto de e-commerce para o modelo e devolve uma resposta JSON pronta para integração com catálogo, ERP ou planilha operacional.

## Preview do workflow

![Preview do Product Description Generator](../../assets/product-description-generator-workflow-success.png)

Visão do fluxo completo de geração estruturada para cadastro de produtos em marketplaces, com entrada normalizada, processamento com IA e saída pronta para uso.

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
curl -X POST https://SEU_N8N/webhook/product-description-generator \
  -H "Content-Type: application/json" \
  -d @sample-input.json
```

Substitua `https://SEU_N8N` pela URL da sua instância do n8n. Em ambiente local, use a URL gerada pelo próprio n8n para o webhook de teste ou produção.

## Credenciais necessárias

- Chave de API do provedor de IA.
- URL de Webhook.
- Credenciais opcionais de integrações.

## Ideias de customização

- Gerar versões diferentes para Shopee, Mercado Livre e loja própria.
- Incluir regras por categoria de produto.
- Adicionar tradução automática para catálogos multilíngues.
- Validar limite de caracteres por canal de venda.
- Enviar a saída para Google Sheets, ERP ou CMS.

## Nota de portfólio

Este workflow demonstra a capacidade de transformar uma dor de e-commerce em uma automação prática usando n8n, IA e saída estruturada. O case reforça competências em modelagem de entrada, engenharia de prompt, padronização de resposta e pensamento de produto aplicado a marketplaces.

## Créditos

Inspirado e tecnicamente adaptado a partir do template aberto `product_description_generator.json` do repositório `wassupjay/n8n-free-templates`, com simplificação de arquitetura e reposicionamento para case de portfólio.
