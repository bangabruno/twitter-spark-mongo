# eng-twitter-spark-mongo [EM CONSTRUÇÃO]
Consumindo dados da API do Twitter, processando com Spark e utilizando uma API no Python com Flask para gravar e consultar os dados no MongoDB.

os.environ['PYSPARK_SUBMIT_ARGS'] = "--master mymaster --total-executor 2 --conf "spark.driver.extraJavaOptions=-Dhttp.proxyHost=proxy.mycorp.com-Dhttp.proxyPort=1234 -Dhttp.nonProxyHosts=localhost|.mycorp.com|127.0.0.1 -Dhttps.proxyHost=proxy.mycorp.com -Dhttps.proxyPort=1234 -Dhttps.nonProxyHosts=localhost|.mycorp.com|127.0.0.1 pyspark-shell"

Pressione para startar o projeto :]

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bangabruno/eng-twitter-spark-mongo/master?urlpath=lab)
