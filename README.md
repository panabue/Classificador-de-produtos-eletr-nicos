# Classificador-de-produtos-eletronicos
Bot para o Telegram que classifica produtos eletrônicos de acordo com seu departamento.
## Descrição
Foram definidas 3 classes de produtos eletrônicos (informática, eletrodomésticos, celulares). Para cada classe coletei pelos menos 200 produtos do Mercado Livre utilizando scrapy. 

Considerando os modelos pré-treinados Distilbert e Bert em https://huggingface.co/models?pipeline_tag=text-classification&sort=trending, fiz os splits de treino, teste e validação e realizei o treinamento de cada modelo. O resultado final de classificação foi reportado utilizando o https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html.

Com o melhor modelo, construimos o bot do telegram para que ele reconheça os produtos dados pelos usuários.
## Conteudo
