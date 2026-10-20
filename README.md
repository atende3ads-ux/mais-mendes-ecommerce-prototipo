# Mais Mendes — protótipo do e-commerce

Protótipo navegável do e-commerce da Mais Mendes Distribuidora, usado para validar arquitetura e fluxo antes da implementação no tema **Ipanema** da Nuvemshop.

**Ver online:** https://atende3ads-ux.github.io/mais-mendes-ecommerce-prototipo/
**Mapa da loja (sitemap interativo):** https://atende3ads-ux.github.io/mais-mendes-ecommerce-prototipo/sitemap.html

## O que dá para testar

- **Home** na estrutura do Ipanema: banner rotativo (4 opções), categorias com foto, como funciona, marcas parceiras em faixa contínua, listas de produtos, faixa para CNPJ, depoimentos (seção nativa do Ipanema) e newsletter.
- **Categoria e busca** (`categoria.html`): filtro por subcategoria e marca, ordenação, adicionar com quantidade direto no card.
- **Produto** (`produto.html`): variações com preço por opção, tag de desconto, quantidade, cálculo de frete e prazo por CEP.
- **Meu orçamento**: lista lateral com total, quanto falta para a entrega grátis, frete e prazo, e a barra fixa que acompanha a navegação.

## O que é ilustrativo

- **Preços:** são reais os 3 da planilha do cliente, a tabela dos cabos Lamesa e a argamassa Precon (tirados das artes do cliente). Os demais são de exemplo.
- **Descontos:** a tag e o preço "de" são de exemplo, só para mostrar o componente.
- **Preço no Pix ou no CNPJ e parcelas:** 5% e até 10x sem juros são valores de exemplo. A linha única "com Pix ou no CNPJ" junta dois recursos nativos da Nuvemshop: o desconto por meio de pagamento (um percentual para a loja toda) e a tabela de preço de atacado (o plano Impulso tem uma). Só vale se os dois tiverem o mesmo percentual.
- **Frete e prazo:** seguem a política de frete do cliente (13/10/2026), com valores simulados para transportadora. A regra de CNPJ (grátis a partir de R$ 1.000) aparece só como aviso. Grande Goiânia = CEPs 74xxx, Senador Canedo e Trindade, até o cliente confirmar as cidades atendidas.
- **Fotos de produto:** todas em fundo branco e sem marca d'água. 15 produtos usam a foto real, recortada das artes do próprio cliente; os outros usam imagens de licença livre que mostram o tipo de produto, não a marca exata. Fontes em [CREDITOS.md](CREDITOS.md).
- **Textos e fotos dos banners.**
- **Depoimentos:** textos e nomes de exemplo, só para mostrar a seção. Na loja, entram avaliações reais de clientes, com autorização.

## Estrutura

```
index.html · categoria.html · produto.html
sitemap.html           mapa da loja para validação, no padrão visual da 3ADS (arquivo único)
assets/css/style.css   tokens do manual de marca + componentes
assets/js/data.js      catálogo gerado da planilha de produtos do cliente
assets/js/app.js       cabeçalho, rodapé, orçamento e páginas
assets/img/            logo, banners, fotos de produto e logos das marcas (créditos em CREDITOS.md)
```

HTML, CSS e JS puros, sem build. Para rodar local: `python3 -m http.server` na pasta e abrir `localhost:8000`.
