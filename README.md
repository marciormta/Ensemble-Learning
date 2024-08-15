# Modelagem de Tópicos do Noticiário Financeiro

## Descrição do Projeto

Este repositório contém implementações de diferentes técnicas de **ensemble learning** aplicadas à modelagem de tópicos de notícias financeiras. Três abordagens principais foram exploradas:

1. **Voting (Votação)**: Combinação simples de modelos usando votação majoritária ou média das probabilidades.
2. **Otimização de Hiperparâmetros para Voting**: Exploração de diferentes configurações de `random_state` para encontrar a melhor performance.
3. **Stacking**: Combinação avançada de modelos onde um modelo final aprende a melhor maneira de integrar as previsões dos modelos base.

## Estrutura do Projeto

1. **voting.py**:
   - Implementa o método de Voting com Regressão Logística, Random Forest, e Naive Bayes.
   - Avalia a performance do modelo em um conjunto de dados de notícias financeiras.
   
2. **Hiperparâmetros_Voting.py**:
   - Estende o primeiro código explorando diferentes `random_state` para melhorar a divisão dos dados de treino e teste.
   - Compara as estratégias de votação `soft` e `hard` para identificar a configuração ideal.

3. **stacking.py**:
   - Implementa o método de Stacking, combinando Random Forest e Naive Bayes, com uma Regressão Logística como modelo final.
   - Avalia a performance dessa combinação mais sofisticada.

## Ferramentas e Bibliotecas

Este projeto foi desenvolvido utilizando as seguintes ferramentas e bibliotecas:

- **Python 3.9+**
- **NumPy**: Para manipulação de arrays e cálculos numéricos.
- **NLTK**: Para processamento de linguagem natural, incluindo a remoção de stop words.
- **Scikit-learn**: Para construção, treinamento e avaliação de modelos de machine learning, incluindo técnicas de ensemble como Voting e Stacking.
