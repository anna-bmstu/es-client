# es-client
Elasticsearch client, news are taken from RabbitMQ queue (crawler)

Работа с базой данных Elasticsearch. 
Несколько потоков достают данные в формате json из очереди CONTENTS. Эти данные были помещены туда потоками из программы crawler.
Затем создается индекс для хранения данных с полями заголовок, время публикации и текст. 
Документы сохраняются с идентификаторами, вычисленными как хэш от текста документа. В классе ElasticConnector есть методы, осуществляющие поиск по документам. 

В файле Kmean.py представлен алгоритм кластеризации k-means.
