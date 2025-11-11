# Qual o melhor elenco do Cortinhians dos últimos 10 anos
> Baseado nos números

## Objetivo 
O obejtivo desse projeto é:
- Obter dados através do Power Query
- Limpeza e tratamento dos dados
- Analisar os dados obtidos através do [FBref](https://fbref.com/pt/equipes/bf4acd28/Corinthians-Estatisticas);
- Identificar padrões dos elencos campeões (2015 e 2017 que foram campeão brasileiro, 2018, 2023 com péssima atuação)
- Matar a curiosidade de qual elenco foi melhor nos últimos 10 anos;

## Obtenção dos Dados
Primeiramente fizemos a extraçao dos dados usando power query, isso foi inspirado no artigo: [Power Query: web scrapping ](https://www.linkedin.com/pulse/power-query-web-scrapping-de-200-p%C3%A1ginas-com-gustavo-kitagawa/) do [Gustavo](https://www.linkedin.com/in/gustavokitagawa/) onde aprendi a fazer esse procedimento.

Que consiste em usar a linguagem power query para obter os dados de uma tabela de um site. Usando o script e uma tabela com os links. Deixando o trabalho automatizado sem precisar ir um por um para obter os dados.


## Limpeza e Tratamento
- Dados extraidos para uma consulta no Power Query (obs: os dados de 2014-2018 são incompletos em relação aos dados de 2019-2023, os dados recentes possuem mais informações mas para fins comparativo utilizaremos os dados das mesmas colunas em todas as tabelas.)
- Usaremos como comparação duas tabelas uma com o elenco/jogadores daquele ano e uma com os resultados das partidas nos campeonatos (Série A, Libertadores, Sul Americana)
- Para uma primeira limpeza utilizamos ainda o Power Query, arrumamos os nomes das colunas, apagamos as colunas que não serão utilizada para análise.
- Uma limpeza mais profunda feita em seguida:
    - Separação da coluna Opponent em duas colunas uma com o nome do time e outra com nome do país relativo
    - Resultados dos pênaltis retirados e colocados como empate (pois para essa análise o que foi contabilizado foram os 90 minutos do tempo regular)
    - 


>Dados dos jogadores são em relação ao Campeonato Brasileiro Série A 

> OBS engraçada, durante a análise observei que colocaram a nacionalidade do Emerson Sheik como QAT (Qatar) o que está errado pois ele é brasileiro (BRA). 

> Correlação de vitórias com público em jogos em casa

> Tentar entender porque a média do público em 2022, 2023 são maiores dos que os anos que foram campeões. Talvez a pandemia?

Pontos a serem observados e insights obtidos dos dados analisados
Perguntas a serem respondidas:
- Proporção de vitória, derrota e empate, gols pró e gols contra
- % de aproveitamento para ser campeão
- Saldo de gols de um time campeão
- Posição 


Primeiro painel:

- 454 jogos totais (Brasileiro Série A, Libertadores, Sula Americana)
- 194(42%) v / 123(27%) d / 137(30%) e
- 566 gols pró / 426 gols contra
- Anos que foram campeões brasileiro (2015 e 2017) tiveram 71% e 63% de aproveitamento e o saldo de gols foram (47 e 33)¹


-  Não houve saldo de gols negativo ao longo dos anos (mas houve -1 no brasileiro de 2018 e 2023)
- Em 2018 (logo após ser campeão brasileiro) houve mais derrotas que vitórias 
- Com 227 jogos em casa, houve 55% de vitória, com saldo de gols de 167 gols pró
  
obs1: o aproveitamento é calculado pela porcentagem de pontos conquistados pela quantitade de pontos possíveis e o saldo de gols (gols marcados menos gols sofridos)

*O que faz um time campeão? (Com dados)*

- Não ironicamente fazer mais pontos e ganhar mais;
- Ataques que façam gol;
- Defesas que não tomam gol;
- Não perder jogos em casa (2015 teve 1 jogo perdido e 2017 2 jogos perdidos). Ter maior aproveitamento dentro de casa;
- Empatar jogos fora de casa;


> OBS2: Os dados da público em 2020 e 2021 estão faltando devido a pandemia que não havia ninguém nos estádios.

<img src="https://github.com/jeanmatheuss/analise-corinthians/blob/main/img/dash_14-24-gif.gif?raw=true" alt="dash-gif">
