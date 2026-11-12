# My developer: portfólio

Página de portfólio do Theo Teixeira (My developer) com os 10 sites desenvolvidos para profissionais de Salto e região. Cada projeto mostra a página no computador e no celular, com uma descrição e o botão "Acessar o site". Os botões de contato abrem o WhatsApp (11) 96439-2079.

HTML, CSS e JavaScript puros, sem build.

## Estrutura

```
index.html                      página completa (estilos, scripts e lista de projetos dentro do arquivo)
img/<cliente>-d.jpg             print de cada site no computador (as 3 primeiras telas)
img/<cliente>-m.jpg             print de cada site no celular
img/og.jpg                      imagem que aparece ao compartilhar o link (WhatsApp, Instagram)
img/favicon.png                 ícone da aba
img/apple-touch-icon.png        ícone ao salvar na tela do celular
sites/isadora-magnaboschi/      cópia do site da Isadora (ainda não publicado à parte)
sites/talita-oka/               cópia do site da Talita (o endereço antigo saiu do ar)
vercel.json                     configuração da Vercel (URLs limpas)
```

## Publicar

1. Crie um repositório no GitHub (ex.: `My_Developer`) e envie os arquivos desta pasta para a raiz dele.
   Importante: **arraste as pastas `img` e `sites` inteiras** para a área de upload. O botão "choose your files" não envia pastas.
2. Na Vercel, clique em **Add New → Project**, importe o repositório e mantenha:
   - Project Name: `my-developer`
   - Framework Preset: **Other**
   - Build Command: vazio
   - Output Directory: vazio (raiz)
3. Clique em **Deploy**. O portfólio fica em https://my-developer.vercel.app/ e cada novo commit publica a atualização sozinho.

Se o nome `my-developer` não estiver disponível, escolha outro (ex.: `my-developer-portfolio`) e troque o endereço em `canonical`, `og:url` e `og:image` no `<head>` do `index.html`.

## Editar conteúdo

- Projetos: lista `CASOS` no script do `index.html` (nome, especialidade, tipo, link e descrição). Um projeto com `destaque:true` ocupa a largura inteira.
- Link de cada site: campo `url`. Quando a Isadora ou a Talita forem publicadas à parte, troque `sites/<cliente>/index.html` pelo endereço novo e apague a pasta correspondente em `sites/`.
- Novo projeto: adicione um item em `CASOS` e os prints `img/<cliente>-d.jpg` (900 px de largura, página do topo até umas 3 telas) e `img/<cliente>-m.jpg` (520 px de largura, abertura no celular).
- WhatsApp: variável `numero` no fim do `index.html` (hoje 5511964392079) e as mensagens nos atributos `data-wa`.
- Ao trocar uma imagem mantendo o mesmo nome, aumente o `?v=1` no link.
