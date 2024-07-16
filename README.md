# Classificador-de-produtos-eletrônicos
Bot para o Telegram que classifica produtos eletrônicos de acordo com seu departamento.
## Descrição
Foram definidas 3 classes de produtos eletrônicos (informática, eletrodomésticos, celulares). Para cada classe coletei pelos menos 200 produtos do Mercado Livre utilizando scrapy. 

Considerando os modelos pré-treinados Distilbert e Bert em https://huggingface.co/models?pipeline_tag=text-classification&sort=trending, fiz os splits de treino, teste e validação e realizei o treinamento de cada modelo. O resultado final de classificação foi reportado utilizando o https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html.

Com o melhor modelo, fiz o Bot do telegram para que ele reconheça os produtos dados pelos usuários.
## Conteúdo
(1) o conjunto de dados

(2) o código para o colab para treinamento dos modelos 

(3) código para conectar o modelo no bot do telegram 
## Como usar
1-Caso queira treinar os modelos novamente, baixe o arquivo Dataset-Produtos-Eletrônicos.zip e coloque no seu Drive. Execute o arquivo Treinamento-dos-Modelos.ipynb no colab. 

Pule a parte de configuração do scrapy caso esteja utilizando o Dataset-Produtos-Eletrônicos.zip no seu Drive. 

Ao fim da execução, dois arquivos contendo os modelos treinados serão criados no seu Drive. Agora execute o Bot-Telegram.ipynb no colab. 

O bloco da função Main deve permanecer em execução para que o Bot possa funcionar.  Dentro do arquivo podemos encontrar o link do Bot no Telegram, basta clicar nele e iniciar a conversa. 

Lembre-se que o bot classifica produtos em 3 classes apenas: (informática, eletrodomésticos, celulares).

2-Caso nao queira treinar os modelos novamente, segue os links para os modelos treinados:
Link para o modelo (Bert): https://drive.google.com/drive/folders/1-oT2s24dS3voPQT-Kz_YPQgr7Wdch9n8?usp=sharing

Link para o modelo (Distilbert): https://drive.google.com/drive/folders/100E0Mch2Iv9JYC6hHyBAplpQ6MNsz9CX?usp=drive_link
