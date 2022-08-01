# Desafio Técnico - Americanas SA
**Cientista de Dados Jr**

Leonardo Gabriel Ferreira Rodrigues

leonardogfrodrigues@gmail.com

__________________
## Desenvolvimento
O desafio foi desenvolvido em linguagen Python (versão 3.7.13) e foi executado em nuvem por meio do ambiente Google Colaboratory.

## Relatório
Está disponível em: [Relatório Gerencial](https://github.com/leonardogfrodrigues/desafio-tecnico/blob/main/Relat%C3%B3rio.pdf)

__________________
# Etapas

## :eyeglasses: Análise Exploratória dos Dados
Etapa responsável por compreender, realizar estatística descritiva e visual dos dados.

## :game_die: Preparação dos Dados
Nessa etapa, os dados do conjunto foram normalizados de maneira a se obter a integridade dos mesmos, bem como contribuir com o desempenho da modelagem. Além disso, ela evita que valores discrepantes sejam mal distribuídos, mudando esses valores para uma escala comum, que combine com o conjunto.

O conjunto de dados foi distribuído em 75% para treino e 25% para teste, totalizando 349 amostras de treino e 117 para teste. 

## :memo: Modelagem
Foi proposto um modelo MultiLayer-Perceptron (MLP) chamado **AmericanasModel**, que consiste em uma rede neural apropriada para conjuntos de dados que não são linearmente separáveis. O **AmericanasModel** (conforme visto na Figura 1) possui as seguintes características:

- 2 hidden layers (camadas ocultas);
- Batch Normalization e função ReLU entre cada camada;
- Função dropout para regularizar os dados enviados à camada de saída;
- 1 camada de saída Sigmóide para o cálculo das probabilidades entre zero e um (0 e 1).

<img src="https://github.com/leonardogfrodrigues/desafio-tecnico/blob/main/figuras/AmericanasModel.png" width="620">


## :chart_with_upwards_trend: Avaliação da Performance do Modelo
O modelo foi treinado e testado com o **MLP AmericanasModel**, por 100 épocas. Foi avaliado utilizando os índices obtidos da matriz de confusão:

- VP: verdadeiro positivo
- VN: verdadeiro negativo
- FP: falso positivo
- FN: falso negativo

Posteriormente, esses índices foram utilizados para verificar a performance do modelo em termos de **Acurácia, Precisão, Recall, e F1-Score**.

Por fim, foi realizada uma comparação entre o **AmericanasModel** e outros modelos tradicionais de aprendizado supervisionado a fim de verificar a robustez do modelo proposto.

| Modelo              | Acurácia (%) | Precisão (%) | Recall (%) | F1-Score (%)  |
|---------------------|--------------|--------------|------------|---------------|
| Decision Tree       | 53,85        | 53,76        | 53,73      | 53,68         |   
| Gradient Boosting   | 62,39        | 62,33        | 62,15      | 61,92         |   
| Naïve Bayes         | 57,26        | 60,94        | 56,45      | 51,92         |   
| Regressão Logística | 62,39        | 66,48        | 61,71      | 59,14         |   
| Random Forest       | 64,1         | 65,76        | 63,34      | 62,66         |   
| KNN                 | 55,56        | 55,52        | 55,31      | 55            |   
| SVM   | 63,25        | 69,15        | 62,5       | 59,4          |   
| **AmericanasModel**     | **68,38**        | **68,66**        | **68,51**      | **68,34**         |   
 

## :white_check_mark: Entrega do Modelo
O MLP **AmericanasModel** após o treinamento foi salvo em formato .pth e carregado para teste. 
O modelo salvo poderá ser utilizado para criação de APIs preditoras. 

## :computer:  Execução da Solução
A solução pode ser facilmente executada em nuvem por meio do ambiente [Google Colaboratory](https://github.com/leonardogfrodrigues/desafio-tecnico/blob/main/desafio.ipynb). 
