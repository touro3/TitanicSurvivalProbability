# Projeto Titanic - Previsão de Sobrevivência

## Visão Geral

Este projeto tem como objetivo prever a sobrevivência dos passageiros do Titanic com base nas informações disponíveis no dataset da competição Titanic do Kaggle. Utilizamos modelos de aprendizado de máquina para realizar essa classificação binária (sobreviver ou não).

## Conjunto de Dados

Foram usados três arquivos CSV fornecidos pela competição Titanic no Kaggle:

- **train.csv**: Conjunto de dados de treino contendo variáveis explicativas e o rótulo `Survived`, que indica se o passageiro sobreviveu (1) ou não (0).
- **test.csv**: Conjunto de dados de teste contendo variáveis explicativas, mas sem o rótulo `Survived`.
- **gender_submission.csv**: Arquivo contendo as respostas esperadas para o conjunto de teste, usado para avaliar a precisão do modelo.

### Colunas utilizadas:
- **Pclass**: Classe do bilhete do passageiro (1, 2 ou 3).
- **Sex**: Sexo do passageiro (male/female).
- **Age**: Idade do passageiro.
- **Fare**: Tarifa paga pelo bilhete.
- **Survived**: Variável alvo (0 = Não Sobreviveu, 1 = Sobreviveu), presente apenas no arquivo `train.csv`.

## Modelos

Modelos Utilizados:
Dois modelos principais foram treinados para prever a sobrevivência dos passageiros:

Random Forest:
Modelo baseado em múltiplas árvores de decisão que combina os resultados de várias árvores para melhorar a precisão.
Logistic Regression:
Modelo de regressão logística, amplamente utilizado em problemas de classificação binária.
Treinamento dos Modelos
Os modelos foram treinados com os dados de treino (train.csv) e testados com os dados de teste (test.csv). As previsões foram comparadas com os rótulos reais presentes no arquivo gender_submission.csv.

Acurácia dos Modelos:
Random Forest: 91.63%
Logistic Regression: 96.41%

## Ensemble de Modelos 

Para melhorar a precisão, utilizamos o Voting Classifier, que combina os dois modelos principais (Random Forest e Logistic Regression) para fazer previsões. Isso pode resultar em uma melhora no desempenho global.

Acurácia do Ensemble: 96.41%

## Dependências

As bibliotecas Python necessárias para executar o código estão listadas abaixo. Salve essas dependências em um arquivo `requirements.txt` e instale-as usando o comando:

```bash
pip install -r requirements.txt

