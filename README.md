# Vi Crochê

Site de uma página para divulgar os tapetes de crochê da Vi. Cada modelo tem um botão "Compre agora" que abre o WhatsApp dela com o nome do modelo já escrito.

## Como ver

Abra o `index.html` no navegador. Não precisa instalar nada.

No VS Code, a extensão **Live Server** atualiza a página sozinha enquanto você edita.

## Onde mexer

Tudo fica no `index.html`:

- **Número do WhatsApp:** a constante `WHATS` no começo do `<script>`, no formato `55` + DDD + número.
- **Modelos da vitrine:** a lista `MODELOS`. Para adicionar um tapete, coloque a foto em `img/` e copie um bloco da lista. Os campos são:
  - `nome`, `foto`, `tag` (o selinho em cima da foto), `tec` (a técnica) e `desc`
  - `amb`: os filtros onde ele aparece, entre `"banheiro"`, `"cozinha"` e `"sala"`
  - `contain: true` para fotos que não podem ser cortadas
  - `pet: true` para mostrar o selo "Aguenta patinha de cachorro"
- **Cores e fontes:** as variáveis no `:root`, no início do `<style>`.
- **Textos:** direto no HTML (topo, "Como encomendar", "Sobre a Vi" e rodapé).

## Fotos

As fotos ficam em `img/`. O ideal é usar JPG com até 1000 px no lado maior para o site carregar rápido no celular.

## No ar

O site está publicado em https://vi-croche.github.io/ pelo GitHub Pages. Cada `git push` na branch `main` atualiza o site em 1 ou 2 minutos.

A prévia do link no WhatsApp (foto, título e descrição) fica nas tags `og:` do `<head>`. Se o endereço do site mudar, troque também o `og:url` e o `og:image`. O WhatsApp guarda a prévia antiga por um tempo, então a mudança pode demorar a aparecer.

## Colocar no ar em outro lugar (grátis)

- **GitHub Pages:** suba o repositório no GitHub e ative em *Settings → Pages* (branch `main`, pasta raiz).
- **Netlify:** arraste esta pasta para app.netlify.com/drop.
