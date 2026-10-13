# Mais Mendes — protótipo do e-commerce

Protótipo navegável do e-commerce da Mais Mendes Distribuidora, usado para validar arquitetura e fluxo antes da implementação no tema **Ipanema** da Nuvemshop.

**Ver online:** https://atende3ads-ux.github.io/mais-mendes-ecommerce-prototipo/

## O que dá para testar

- **Home** na estrutura do Ipanema: banner, categorias, como funciona, listas de produtos, faixa para CNPJ, marcas e newsletter.
- **Categoria e busca** (`categoria.html`): filtro por subcategoria e marca, ordenação, adicionar com quantidade direto no card.
- **Produto** (`produto.html`): variações, quantidade, cálculo de frete e prazo por CEP.
- **Meu orçamento**: lista lateral com total, frete e prazo, e a barra fixa que acompanha a navegação.

## O que é ilustrativo

- Preços (só 3 produtos têm preço real na planilha do cliente).
- Valores e prazos de frete — CEPs iniciados em 74/75 simulam Goiânia e região.
- Imagens de produto: ícones no lugar das fotos.
- Textos de banner.

## Estrutura

```
index.html · categoria.html · produto.html
assets/css/style.css   tokens do manual de marca + componentes
assets/js/data.js      catálogo gerado da planilha de produtos do cliente
assets/js/app.js       cabeçalho, rodapé, orçamento e páginas
```

HTML, CSS e JS puros, sem build. Para rodar local: `python3 -m http.server` na pasta e abrir `localhost:8000`.
