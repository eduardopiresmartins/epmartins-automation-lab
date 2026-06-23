# Product Description Generator

## Problema de negócio

Pequenos e médios vendedores de marketplace costumam perder tempo escrevendo descrições manualmente ou publicando anúncios fracos, genéricos e pouco orientados à conversão. Isso impacta velocidade de cadastro, consistência da comunicação e potencial de venda.

## Solução

Esta automação recebe informações básicas do produto e devolve uma estrutura pronta para uso comercial: título otimizado, descrição comercial, bullets de benefícios, tags e sugestão de categoria. O objetivo é acelerar o cadastro de itens com um padrão mais profissional de copy.

## Visão geral do fluxo

Entrada -> Processamento com IA -> Saída estruturada -> Próxima ação

O workflow recebe os dados via webhook, normaliza os campos principais, envia um prompt com contexto de e-commerce para o modelo e devolve uma resposta JSON pronta para integração com catálogo, ERP ou planilha operacional.

## Exemplo de entrada

Veja [sample-input.json](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/workflows/product-description-generator/sample-input.json).

## Exemplo de saída

Veja [sample-output.md](/Users/eduardopiresmartins/Documents/epmartins-automation-lab/workflows/product-description-generator/sample-output.md).

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

- Gerar versões diferentes para Shopee, Mercado Livre e loja própria.
- Incluir regras por categoria de produto.
- Adicionar tradução automática para catálogos multilíngues.
- Validar limite de caracteres por canal de venda.
- Enviar a saída para Google Sheets, ERP ou CMS.

## Créditos

Inspirado e tecnicamente adaptado a partir do template aberto `product_description_generator.json` do repositório `wassupjay/n8n-free-templates`, com simplificação de arquitetura e reposicionamento para case de portfólio.
