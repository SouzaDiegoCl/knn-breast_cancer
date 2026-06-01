# AM - KNN com Dataset do Scikit-learn

Faculdade de Tecnologia do Estado de Sao Paulo - FATEC Registro

Atividade Prática - Aprendizado de Máquina

Aluno: Diego Baltazar de Souza Claudio

## Descrição da Atividade

Este projeto implementa um classificador KNN (K-Nearest Neighbors) utilizando o dataset `breast_cancer` do próprio scikit-learn. A atividade tem como objetivo demonstrar o fluxo completo de um problema de classificação supervisionada, desde a exploração inicial dos dados até a avaliação final do modelo.

O notebook do projeto apresenta uma análise completa com:

- informações gerais sobre o dataset, como shape, classes e features;
- ao menos um gráfico explorando a distribuição dos dados;
- pré-processamento com `StandardScaler`, com justificativa para o uso no KNN;
- treinamento do modelo testando valores de K de 1 a 20;
- gráfico de acurácia por K e escolha justificada do melhor valor;
- `classification_report` do modelo final com o K escolhido.

## Dataset

O projeto utiliza o dataset `breast_cancer` disponibilizado pelo scikit-learn por meio da função `sklearn.datasets.load_breast_cancer()`. Esse conjunto de dados contém medidas extraídas de imagens de massas de mama e é amplamente utilizado em tarefas de classificação binária.

As classes do problema são:

- `malignant`;
- `benign`.

As features descrevem características numéricas relacionadas ao núcleo celular, como raio, textura, perímetro, área, suavidade, compactação, concavidade e simetria, entre outras estatísticas calculadas.

## Características do Modelo

O modelo implementado neste projeto possui as seguintes etapas:

- **Entrada (features):** 30 variáveis numéricas do dataset `breast_cancer`.
- **Saída (target):** classificação binária indicando se o caso é maligno ou benigno.
- **Algoritmo:** K-Nearest Neighbors.
- **Pré-processamento:** padronização com `StandardScaler`.
- **Busca de hiperparâmetro:** avaliação de K entre 1 e 20.

O uso do `StandardScaler` é necessário porque o KNN calcula distâncias entre amostras. Quando as variáveis estão em escalas diferentes, algumas features podem dominar o cálculo da distância e prejudicar a qualidade da previsão. A padronização reduz esse problema ao colocar todas as variáveis em uma faixa comparável.

## Estrutura do Projeto
```
.
├── README.md                                    # Este arquivo
├── main.py                                      # Script principal
├── pyproject.toml                               # Configuração do projeto
└── notebooks/
		└── knn-notebook.ipynb                   # Notebook com a análise completa
```

## Instruções e Exemplos

Todas as instruções detalhadas, análises do dataset, visualizações gráficas, testes com diferentes valores de K e avaliação final do modelo encontram-se no notebook localizado em [notebooks/knn-notebook.ipynb](notebooks/knn-notebook.ipynb).

O notebook contém:

- descrição e contexto da atividade;
- carregamento do dataset do scikit-learn;
- análise exploratória com estatísticas e gráficos;
- explicação do pré-processamento;
- treinamento e comparação de valores de K de 1 a 20;
- gráfico de acurácia por K;
- avaliação final com `classification_report`.

## Pré-requisitos

- Python 3.14+
- Bibliotecas principais:
	- pandas
	- matplotlib
	- seaborn
	- scikit-learn

## Como Usar

1. Clone o repositório.
2. Instale as dependências com `uv sync`.
3. Abra o notebook `notebooks/knn-notebook.ipynb` para executar a análise.
4. Execute todas as células do notebook para reproduzir os resultados.