# Roteiro 3 - Classificação de Imagens de Gatos e Cachorros com CNN e Transfer Learning
https://colab.research.google.com/drive/16gcAhSnbFAubT9q0lHbmdIDDh0RrHXlW?usp=sharing
https://drive.google.com/drive/folders/1dTZQBX3X1thLCA_BNFXrs--9fArzOt_v?usp=sharing

Este projeto utiliza uma Rede Neural Convolucional com **Transfer Learning** baseada no modelo MobileNetV2, pré-treinado no dataset ImageNet, para classificar imagens de gatos e cachorros. Usando a biblioteca TensorFlow e a API funcional do Keras, o modelo é ajustado e treinado com novas camadas para personalizar a tarefa.

## Estrutura do Projeto

- **Treinamento**: Script de treinamento do modelo. Realiza a preparação dos dados, define a arquitetura da rede neural com `MobileNetV2` como modelo base, e salva o modelo treinado e suas métricas.
- **Predição**: Script para carregar o modelo salvo, fazer previsões em novas imagens e plotar as métricas de treino e validação.

## Pré-requisitos

Certifique-se de ter as bibliotecas a seguir instaladas em seu ambiente Python:

- `TensorFlow`
- `Pandas`

### 1. Baixar o Dataset

O script `train_model.py` faz o download automático do dataset de gatos e cachorros, fornecido pelo `TensorFlow`. O dataset será extraído e dividido em `train` e `validation` de forma automática.

### 2. Treinamento do Modelo

- Baixar e carregar o dataset de gatos e cachorros.
- Usar o `MobileNetV2` como o modelo base e adiciona camadas superiores personalizadas para a tarefa de classificação binária.
- Treinar o modelo congelando o modelo base e ajustando apenas as camadas superiores.
- Salvar o modelo treinado em `trained_model.h5` e exporta as métricas de acurácia e perda para o arquivo `training_metrics.csv`.

### 3. Fazer Previsões e Plotar as Métricas

- Carrega o modelo treinado de `trained_model.h5`.
- Lê as métricas de treinamento de `training_metrics.csv`.
- Plota gráficos das métricas de `accuracy` e `loss` para avaliar o desempenho do modelo.
