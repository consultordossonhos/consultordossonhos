# Site — Consultor dos Sonhos

Site de uma página com os dois ebooks (gratuito e avançado).

## Estrutura

```
index.html              -> o site (HTML+CSS+JS, tudo num arquivo só)
assets/cover-free.jpg    -> capa do ebook gratuito
assets/cover-paid.jpg    -> capa do ebook avançado
ebooks/Ocultismo_para_Iniciantes.pdf
ebooks/Ocultismo_e_Tradicoes_Esotericas.pdf
```

Não apague nem renomeie esses arquivos sem ajustar os caminhos no `index.html`.

## Como publicar (gratuito, sem precisar saber programar)

### Opção mais fácil — Netlify Drop
1. Acesse https://app.netlify.com/drop
2. Arraste a pasta inteira `site` (esta pasta) para a página.
3. Pronto — você recebe um link tipo `nome-aleatorio.netlify.app`.
4. Para trocar o nome do link: crie uma conta grátis na Netlify, abra o site recém-criado e em **Site settings → Change site name**.
5. Se quiser usar um domínio próprio (ex: consultordossonho.com.br), em **Domain settings** dá pra apontar o domínio comprado em qualquer registrador (Registro.br, GoDaddy, etc.).

### Opção GitHub Pages
1. Crie um repositório novo no GitHub (pode ser público).
2. Suba todos os arquivos desta pasta (`index.html`, `assets/`, `ebooks/`) para o repositório.
3. Em **Settings → Pages**, escolha a branch `main` e pasta `/ (root)`.
4. O GitHub te dá um link tipo `seuusuario.github.io/nome-do-repo`.

## Como editar depois

Abra `index.html` em qualquer editor de texto (até o Bloco de Notas funciona).

- **Trocar o link do Instagram**: procure por `consultordossonho` no arquivo e troque pelo seu usuário em todos os lugares (são 2: o link do header/footer e o `https://ig.me/m/consultordossonho` do botão "Quero esse guia").
- **Trocar o botão "Comprar" para WhatsApp em vez de Instagram**: troque
  `href="https://ig.me/m/consultordossonho"` por
  `href="https://wa.me/55SEUNUMEROAQUI?text=Quero%20o%20guia%20avan%C3%A7ado"`
  (troque `55SEUNUMEROAQUI` pelo seu número com DDI+DDD, só números).
- **Trocar textos**: qualquer texto dentro de `<h1>`, `<p>`, `<h3>` etc. pode ser editado direto.
- **Trocar as capas**: substitua os arquivos em `assets/` mantendo o mesmo nome, ou troque o nome no `src=""` das tags `<img>`.

## Quando o ebook pago tiver um link de pagamento de verdade

Quando você tiver uma página de checkout (Hotmart, Kiwify, Stripe etc.), é só trocar:

```html
<a class="btn btn-gold" href="https://ig.me/m/consultordossonho" ...>Quero esse guia</a>
```

pelo link de pagamento, por exemplo:

```html
<a class="btn btn-gold" href="https://pay.kiwify.com.br/SEU-LINK" ...>Quero esse guia</a>
```
