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

## Categorias de base (`base.csv`)

São os garotos das categorias de base dos clubes. Eles jogam o sub-20, a Copinha, a Youth League e o Mundial Sub-20. Os nomes vieram dos elencos da UEFA Youth League 2026/27, das seleções de base de 2025 (Mundial Sub-20, Mundial Sub-17, Sul-Americanos e Euros de base) e dos elencos sub-20 de 2026 dos clubes brasileiros (ogol.com.br). A divisão entre zagueiro e lateral, e entre volante e meia, foi estimada, então confira a posicao. O overall e o potencial são estimativas do jogo, então ajuste à vontade.

Nesta planilha também dá para mudar a **posicao**: GOL, ZAG, LAT, VOL, MEI ou ATA.

### Adicionar um garoto novo

Crie uma linha nova com todas as colunas preenchidas:

- **clube**: o nome do clube exatamente como aparece no jogo (por exemplo `Flamengo`, `Atlético-MG`, `Bayern de Munique`)
- **nome_original** e **nome**: o nome do garoto, igual nas duas colunas
- **overall** e **potencial**
- **posicao**: GOL, ZAG, LAT, VOL, MEI ou ATA
- **idade**: de 14 a 20
- **pais**: em português, como no jogo (`Brasil`, `Argentina`, `Inglaterra`...)

Ele entra na base do clube nas carreiras novas e, uma vez, nas carreiras em andamento.

## Patrocinadores (`patrocinadores.csv`)

São as marcas que patrocinam seus atletas (chuteira, relógio, banco...) e as empresas que podem ser patrocinador master do clube que você comprar.

Pode mudar:

- **nome**: o nome que aparece no jogo
- **nivel**: 1 = marca global, 2 = marca grande, 3 = marca nacional. Marcas globais só procuram atletas de imagem muito alta e pagam mais. Só as marcas de nível 1 e 2 viram patrocinador master de clube.

Não mexa em **id**, **categoria** e **nome_original**: é por elas que o jogo acha a marca.

### Adicionar uma marca nova

Crie uma linha nova. Deixe o **id** vazio e preencha:

- **categoria**: uma destas, escrita igual: Material esportivo, Relógios, Bebidas, Bancos, Telefonia e tecnologia, Games e apps, Moda e beleza, Automóveis, Suplementos, Empresas (só clubes)
- **nivel**: 1, 2 ou 3
- **nome_original** e **nome**: o nome da marca, igual nas duas colunas

### Como o jogo usa

- O nome novo aparece na hora, em todas as carreiras, inclusive nos contratos que já estão assinados.
- O nível vale para as próximas propostas. Contratos já assinados continuam com o valor combinado.
- Se você trocou o nome de uma marca pela tela **Marcas do jogo**, dentro do jogo, o nome dessa tela vale mais que o da planilha naquele aparelho.
