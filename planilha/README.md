# Planilha dos jogadores

Cada arquivo `.csv` desta pasta é uma liga do jogo. O GitHub mostra o arquivo como tabela.

## Como editar

1. Abra o arquivo da liga (por exemplo `brasileirao.csv`).
2. Clique no lápis (**Edit this file**).
3. Ache a linha do jogador. Dá para usar Ctrl+F para buscar.
4. Altere só estas colunas:
   - **nome**: o nome que aparece no jogo
   - **overall**: força atual (30 a 99)
   - **potencial**: até onde ele pode chegar (30 a 99, nunca menor que o overall)
5. Clique em **Commit changes**.

Em cerca de 1 minuto o site atualiza. Na próxima vez que o jogo for aberto, a mudança vale.

## Não mexa em

- **clube** e **nome_original**: é por elas que o jogo acha o jogador. Se mudar, a linha é ignorada.
- **posicao**, **idade** e **pais**: estão aí só para consulta. Mudar não altera nada no jogo.
- A primeira linha (o cabeçalho) e o arquivo `arquivos.json`.

## Como o jogo usa

- **Carreira nova**: já começa com os valores da planilha.
- **Carreira em andamento**: cada linha alterada é aplicada uma vez, quando você abre o jogo. Depois o jogador volta a evoluir normalmente. Se você mudar a mesma linha de novo, a nova mudança é aplicada.
- **Clientes da sua agência** também recebem a mudança.
- **Sem internet**: o jogo usa os dados de sempre.

Para desfazer uma mudança, volte o nome, o overall e o potencial aos valores de antes. Isso conta como uma nova alteração.
