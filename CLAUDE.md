# Football Agent Manager

Jogo em um arquivo só: `index.html` (português). Publicado no GitHub Pages a partir da `main`.

## Fonte da verdade

- `index.html` da `main` no GitHub é o arquivo-mestre. Edite sempre ele.
- A antiga cópia `janela-aberta.html` do PC não é mais a fonte. Não publicar a partir dela sem antes trazer o `index.html` do GitHub.
- Netlify: nunca publicar.

## Publicar

O usuário autoriza com "pode fazer e publicar". Publicar = enviar para a `main`.

1. Grave a versão (hora de Brasília), senão o botão "Buscar atualização" não acha a versão nova:
   `V=$(TZ=America/Sao_Paulo date +%Y%m%d%H%M); sed -i "s/const APP_V='[0-9]*'/const APP_V='$V'/" index.html`
2. Commit com mensagem curta em português dizendo o que mudou no jogo.
3. `git push origin HEAD:main` (e também o branch da sessão).
4. Na resposta: "Para pegar a versão nova, use Menu → Buscar atualização."

## Como alterar

- Código dentro de um IIFE (`(()=>{'use strict'; ... })();`). Funções não ficam no `window`.
- Edições por substituição exata (script Python que confere se o trecho existe uma vez).
- Depois de editar: extrair o `<script>` e rodar `node --check`.
- Testar no Playwright: copiar `index.html` para o scratchpad, injetar antes do `})();` final um `window.__t=()=>{...}` com o teste (ex.: `initWorld('Teste',0)`, montar o cenário, chamar as funções, `monthly()`), e conferir erros de página.
- Telas: conferir no tamanho de celular. Sempre alinhado, nada cortado.

## Regras do jogo e do usuário

- Antecipar ajustes ligados à mudança (textos, rótulos, listas parecidas, aviso, calendário) sem esperar pedido.
- Nunca inventar jogador pronto. Jogador só nasce na base.
- Card com muito texto começa recolhido e abre com seta, igual ao calendário (ação `fold`, `ui.fold[chave]`).
- Planilhas em `planilha/`: regras no `planilha/README.md`.

## Estilo das respostas

- Português, direto, frases curtas, em tópicos.
- Dizer o que mudou, como funciona no jogo e onde ver.
- Dizer o que foi testado e o que não foi.
- Terminar com "Menu → Buscar atualização" quando publicar.
