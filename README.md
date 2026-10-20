# Mais Mendes — protótipo do e-commerce

Protótipo navegável do e-commerce da Mais Mendes Distribuidora, usado para validar arquitetura e fluxo antes da implementação no tema **Ipanema** da Nuvemshop.

**Ver online:** https://atende3ads-ux.github.io/mais-mendes-ecommerce-prototipo/
**Mapa da loja (sitemap interativo):** https://atende3ads-ux.github.io/mais-mendes-ecommerce-prototipo/sitemap.html

## O que dá para testar

- **Home** na estrutura do Ipanema: banner rotativo (4 opções), categorias com foto, como funciona, marcas parceiras em faixa contínua, listas de produtos, cadastro para CNPJ e newsletter.
- **Categoria e busca** (`categoria.html`): filtro por subcategoria e marca, ordenação, adicionar com quantidade direto no card.
- **Produto** (`produto.html`): variações com preço por opção, tag de desconto, quantidade, cálculo de frete e prazo por CEP.
- **Meu orçamento**: lista lateral com total, quanto falta para a entrega grátis, frete e prazo, e a barra fixa que acompanha a navegação.
- **Três preços**: em "Minha conta" dá para ver a loja como visitante (CPF), empresa (CNPJ) ou profissional CREA-GO, e passar pelo cadastro com aprovação simulada. `index.html#conta` abre direto.
- **Profissionais CREA-GO** (`crea.html`): benefício, cadastro e o preço antes e depois de entrar. O CREA-GO usa um segmento de clientes com uma promoção automática de 5%, sem uma segunda tabela de preço. `crea.html#painel` abre a simulação do que a equipe faz no painel: conferir o registro, incluir no segmento e a configuração da promoção.

## O que é ilustrativo

- **Preços:** são reais os 3 da planilha do cliente, a tabela dos cabos Lamesa e a argamassa Precon (tirados das artes do cliente). Os demais são de exemplo.
- **Descontos:** a tag e o preço "de" são de exemplo, só para mostrar o componente.
- **Preço no Pix e parcelas:** 5% no Pix e até 10x sem juros são valores de exemplo. A exibição segue o recurso nativo da Nuvemshop (um percentual único de desconto por meio de pagamento, mostrado na lista, no produto e no carrinho).
- **Preço CNPJ e CREA-GO:** a regra do CREA-GO é a que o cliente já publica (5% de desconto + 3% de cashback, fiação fora). Os 10% do CNPJ são exemplo. O cadastro não envia nem guarda nada. Falta confirmar no painel se o plano Impulso tem segmentos de clientes; se não tiver, o CREA-GO vira a segunda tabela de preço (plano Escala) e a vitrine fica igual.
- **Simulação do painel:** telas ilustrativas, com os nomes de menu da Central de Ajuda da Nuvemshop. Não reproduzem o painel.
- **Frete e prazo:** seguem a política de frete do cliente (13/10/2026), com valores simulados para transportadora. Grande Goiânia = CEPs 74xxx, Senador Canedo e Trindade, até o cliente confirmar as cidades atendidas.
- **Fotos de produto:** todas em fundo branco e sem marca d'água. 15 produtos usam a foto real, recortada das artes do próprio cliente; os outros usam imagens de licença livre que mostram o tipo de produto, não a marca exata. Fontes em [CREDITOS.md](CREDITOS.md).
- **Textos e fotos dos banners.**

## Estrutura

```
index.html · categoria.html · produto.html · crea.html
sitemap.html           mapa da loja para validação, no padrão visual da 3ADS (arquivo único)
assets/css/style.css   tokens do manual de marca + componentes
assets/js/data.js      catálogo gerado da planilha de produtos do cliente
assets/js/app.js       cabeçalho, rodapé, orçamento e páginas
assets/img/            logo, banners, fotos de produto e logos das marcas (créditos em CREDITOS.md)
```

HTML, CSS e JS puros, sem build. Para rodar local: `python3 -m http.server` na pasta e abrir `localhost:8000`.
