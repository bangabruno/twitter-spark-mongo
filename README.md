# eng-twitter-spark-mongo
Consumindo dados da API do Twitter, processando com Spark e utilizando uma API no Python com Flask para gravar e consultar os dados no MongoDB.

## Instruções

**source/01_api_mongo.ipynb:**
Definição da API utilizando Flask, criada apenas para interação com o MongoDB.
 
**source/02_twitter_spark.ipynb:**
Definição e inicialização do socket para interação com o job spark.
Preencher as variáveis de chave (c_key,  c_secret  a_token e a_secret) para utilização do tweepy, que será responsável por filtrar os      dados tweets para processamento. As chaves são para autenticação em sua própria API, que deve ser criada na página do twitter para  desenvolvedores (Necessário ter uma conta no twitter). Mais informações em: https://developer.twitter.com/en/apps

**source/03_job_spark.ipynb:**
Definição, inicialização e transformações dos tweets obtidos.
Após a comunicação realizada entre o socket, o streaming é iniciado e faz os seguintes passos sobre cada tweet (Utilizando RDD).
   1. Quebra cada tweet em palavras.
   2. Busca por palavras com hashtags (#hashtag)
   3. Agrupa as hashtags encontradas obtendo a quantidade (count()) de cada uma.
   4. Processa a lista de hashtags e envia cada uma delas e suas respectivas quantidades para atualização no banco de dados MongoDB,           utilizando a API como interface.


Pressione para startar o projeto em um ambiente já todo configurado para utilização :]

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bangabruno/eng-twitter-spark-mongo/master?urlpath=lab)
