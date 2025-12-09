🎧 #Consumo Musical na Pandemia: Uma Análise A Partir do Ranking Billboard
Repositório relativo ao projeto desenvolvido no 2º semestre do curso Inteligência e Análise de Dados da Instituição Senai Santo Amaro. Este trabalho foi inscrito e aprovado no Congresso Internacional de Inovação de Pesquisa.


🏹 # Objetivo Geral
O presente projeto buscou analisar os impactos da Pandemia de Covid-19 na forma de consumo musical por meio das plataformas de streaming entre os anos de 2018 e 2023, nos Estados Unidos.


🔆 # Introdução
A indústria musical foi diretamente impactada pelos efeitos da Pandemia de Covid-19 principalmente por conta da proibição das apresentações ao vivo. Paralelamente, o consumo musial por meio das plataformas de streaming cresceu. Diante desse cenário, surgiu a indação a cerca da influência da pandemia no consumo musical.


🖋️ # Metodologia 
O desenvolvimento do projeto foi extenso, sendo contemplado em diversas etapas, descritas a seguir. Todos os códigos foram implementados no Colab, em linguagem de programação Python e utilizando diferentes bibliotecas. O trabalho foi norteado a partir dos dados disponíveis no ranking Billboard Hot 100. De lá foi retirado o histórico das faixas que mais tocaram nas rádios digitais e plataformas de streaming dos Estados Unidos entre os anos de 2018 e 2023.


✳️ # Etapa 1: Obtenção da Base Inicial

A etapa 1 envolveu a obtenção da base de dados inicial. 

_Durante a construção desse repositório observou-se que os dados, antes liberados a todos, agora estão disponíveis apenas para assinantes da revista. Mas a título de registro, o link de acesso no site da Billboard é o: https://www.billboard.com/charts/hot-100/2018-01-06/._

O código obtém todos as datas que caem aos sábados do ano indicado (dia da semana em que o ranking atualiza) e salva numa lista. A partir dessas datas, extrai do site o nome do artista, o título da faixa e posição no ranking de cada uma das 100 faixas. Faz esse processo para todas as semanas de todos os anos, de 2018 a 2023. Por fim, salva em um arquivo CSV.


✳️ # Etapa 2: Informações Complementares com LastFM 

Para esta etapa é necessário criar uma conta no LastFM (https://www.last.fm/pt/) e solicitar acesso à API do site, por meio da solicitação de uma chave da API.
O código basicamente analisa a base anterior linha a linha, e, por meio do nome do artista, atribui um gênero musical.

_A partir desse etapa é importante incluir no código um time.sleep para dar um 'tempo' entre as solicitação à API, evitando assim, que seja atingido o limite da API._


✳️ # Etapa 3: Informações Complementares com Spotify

Para esta etapa é necessário criar uma conta no Spotify Developers (https://developer.spotify.com/) e solicitar acesso à API do site, por meio da solicitação de client id e client secret.
Nesta etapa, através da leitura do nome do artista e nome da faixa, o código obtem o Spotify ID (identificador único da faixa dentro da plataforma), duração da faixa em minutos e data de lançamento.


✳️ # Etapa 4: Merge e Cruzamento de Dados

Esta etapa faz o merge entre todas as bases, antes separadas por ano ano, verifica o percentual de preenchimento entre elas e faz o cruzamento de dados com outras bases de dados disponíveis no site Kaggle, a fim de complementar as informações já mencionados acima e o BPM.

