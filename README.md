# Projeto de Previsão de Churn para E-commerce

## Visão Geral

Este projeto implementa um modelo de previsão de churn para uma empresa de e-commerce fictícia. Utilizamos Python e bibliotecas como Pandas, Scikit-learn e Matplotlib para criar, analisar e visualizar dados, bem como para treinar e avaliar um modelo de machine learning.

## Requisitos

- Python 3.7+
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

## Estrutura do Projeto

O projeto consiste em um único script Python que realiza todas as etapas, desde a geração de dados até a avaliação do modelo e previsões para novos clientes.

## Detalhamento das Etapas

### 1. Geração de Dados

Criamos um conjunto de dados fictício com 1000 clientes. Cada cliente tem as seguintes características:

- `customer_id`: Identificador único do cliente
- `age`: Idade do cliente
- `tenure_months`: Tempo como cliente (em meses)
- `total_purchases`: Número total de compras
- `avg_order_value`: Valor médio dos pedidos
- `last_purchase_days_ago`: Dias desde a última compra
- `total_spend`: Gasto total do cliente
- `num_support_requests`: Número de solicitações de suporte

A variável alvo `churn` é criada com base em duas condições:
1. A última compra foi há mais de 90 dias
2. O gasto total está abaixo da média

### 2. Análise Exploratória de Dados (EDA)

Realizamos uma análise exploratória básica que inclui:

- Exibição das primeiras linhas do dataset
- Informações gerais sobre o dataset (tipos de dados, valores não nulos)
- Estatísticas descritivas
- Cálculo da taxa de churn
- Visualização da matriz de correlação entre as variáveis

### 3. Preparação dos Dados

- Separação das features (X) e da variável alvo (y)
- Divisão dos dados em conjuntos de treino e teste (80% treino, 20% teste)
- Normalização das features usando StandardScaler

### 4. Treinamento do Modelo

Utilizamos um modelo Random Forest Classifier com 100 árvores de decisão.

### 5. Avaliação do Modelo

A avaliação do modelo inclui:

- Relatório de classificação (precisão, recall, f1-score)
- Matriz de confusão
- Visualização da importância das características

### 6. Previsões para Novos Clientes

Demonstramos como usar o modelo treinado para fazer previsões para novos clientes.

## Como Usar

1. Certifique-se de ter todas as bibliotecas necessárias instaladas.
2. Execute o script Python.
3. Analise a saída no console e as visualizações geradas.
4. Para fazer previsões para novos clientes, adicione seus dados ao DataFrame `new_customers` no final do script.

## Possíveis Melhorias

1. Utilizar dados reais em vez de dados fictícios.
2. Implementar técnicas de balanceamento de classes se o churn for um evento raro.
3. Experimentar outros algoritmos de classificação (ex: Gradient Boosting, SVM).
4. Realizar otimização de hiperparâmetros (ex: usando GridSearchCV).
5. Implementar validação cruzada para uma avaliação mais robusta do modelo.
6. Criar uma interface de usuário simples para facilitar a entrada de dados de novos clientes.

## Conclusão

Este projeto demonstra uma abordagem básica para prever churn em um contexto de e-commerce. O modelo e as técnicas utilizadas podem ser adaptados e expandidos para casos de uso específicos em empresas reais.
