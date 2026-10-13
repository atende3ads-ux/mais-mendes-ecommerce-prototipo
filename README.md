# Mais Mendes — protótipo do e-commerce

Protótipo navegável do e-commerce da Mais Mendes Distribuidora, usado para validar arquitetura e fluxo antes da implementação no tema **Ipanema** da Nuvemshop.

**Ver online:** https://atende3ads-ux.github.io/mais-mendes-ecommerce-prototipo/

## O que dá para testar

- **Home** na estrutura do Ipanema: banner rotativo (4 opções), categorias com foto, como funciona, listas de produtos, faixa para CNPJ, marcas e newsletter.
- **Categoria e busca** (`categoria.html`): filtro por subcategoria e marca, ordenação, adicionar com quantidade direto no card.
- **Produto** (`produto.html`): variações com preço por opção, tag de desconto, quantidade, cálculo de frete e prazo por CEP.
- **Meu orçamento**: lista lateral com total, frete e prazo, e a barra fixa que acompanha a navegação.

## O que é ilustrativo

- **Preços:** são reais os 3 da planilha do cliente, a tabela dos cabos Lamesa e a argamassa Precon (tirados das artes do cliente). Os demais são de exemplo.
- **Descontos:** a tag e o preço "de" são de exemplo, só para mostrar o componente.
- **Frete e prazo:** simulados — CEPs iniciados em 74/75 caem em Goiânia e região.
- **Fotos de produto:** 15 são recortes das artes do próprio cliente; as outras vêm de bancos livres e mostram o tipo de produto, não a marca exata. Fontes em [CREDITOS.md](CREDITOS.md).
- **Textos e fotos dos banners.**

## Estrutura

```
index.html · categoria.html · produto.html
assets/css/style.css   tokens do manual de marca + componentes
assets/js/data.js      catálogo gerado da planilha de produtos do cliente
assets/js/app.js       cabeçalho, rodapé, orçamento e páginas
assets/img/            logo, banners e fotos de produto (créditos em CREDITOS.md)
```

HTML, CSS e JS puros, sem build. Para rodar local: `python3 -m http.server` na pasta e abrir `localhost:8000`.
