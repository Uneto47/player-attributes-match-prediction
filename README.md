# Player Attributes Match Prediction - FC Barcelona

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0%2B-yellow.svg)](https://scikit-learn.org/)

## 📋 Descrição

Projeto de Trabalho de Conclusão de Curso (TCC) que implementa **análise preditiva de resultados de partidas do FC Barcelona** utilizando técnicas de Machine Learning. O sistema analisa atributos individuais dos jogadores para prever vitórias do time, explorando diferentes representações de features e algoritmos de classificação.

## 🎯 Objetivos

- Prever resultados de partidas do FC Barcelona (Vitória vs Não Vitória)
- Comparar múltiplos algoritmos de Machine Learning
- Analisar a importância de atributos individuais dos jogadores
- Identificar os jogadores mais impactantes para o desempenho do time
- Avaliar diferentes estratégias de representação de features
- Realizar análise temporal incremental por temporada

## 🔬 Metodologia

### Dataset
- **Fonte**: Dataset customizado criado pelo autor utilizando dados públicos e reais de partidas
- **Composição**: CSV com dados históricos de partidas do Barcelona
- **Features**: Atributos individuais dos 11 jogadores titulares (finishing, dribbling, passing, stamina, etc.)
- **Target**: Classificação binária (1 = Vitória, 0 = Não Vitória)
- **Período**: Múltiplas temporadas históricas
- **Criação**: Dataset próprio construído a partir de fontes públicas oficiais

### Divisão dos Dados
- **Treino**: 60%
- **Validação**: 20%
- **Teste**: 20%

### Algoritmos Implementados

1. **Random Forest** - Ensemble de árvores de decisão
2. **Gradient Boosting** - Boosting com árvores
3. **XGBoost** - Extreme Gradient Boosting
4. **LightGBM** - Gradient Boosting eficiente
5. **CatBoost** - Boosting com suporte a categóricas
6. **SVM (Support Vector Machine)** - Classificação com kernels
7. **Regressão Logística** - Modelo linear probabilístico
8. **MLP (Multi-Layer Perceptron)** - Rede neural artificial

## 📊 Experimentos

### Experimento 1: Atributos Agregados
Usa atributos agregados dos jogadores (ex: médias de categorias).

### Experimento 2: Todos os Atributos Individuais
Utiliza todos os atributos individuais disponíveis de cada jogador.

### Experimento 3: Médias por Jogador
Calcula a média de atributos por cada jogador.

### Experimento 4: Atributos-Chave Selecionados
Foca em atributos específicos mais relevantes (finishing, dribbling, crossing, etc.).

## 📈 Análises Realizadas

### 1. Análise Exploratória
- Distribuição dos resultados (vitórias vs não vitórias)
- Estatísticas por mando de campo (casa vs fora)
- Análise temporal por temporada

### 2. Importância de Features
- Ranking das features mais importantes para predição
- Análise por categoria (ofensivo, defensivo, físico, técnico)
- Curva de importância acumulada

### 3. Identificação do Melhor Jogador
- Cálculo de importância total por jogador
- Taxa de vitória individual
- Ranking dos top 15 jogadores mais impactantes

### 4. Análise Temporal Incremental
- Treinamento progressivo por temporada
- Avaliação da consistência do modelo ao longo do tempo
- Comparação de desempenho casa vs fora

### Estrutura de Arquivos

```
player-attributes-match-prediction/
│
├── players-notebook.ipynb      # Notebook principal com todas as análises
├── barcelona_dataset.csv        # Dataset (não incluído no repositório)
├── README.md                    # Este arquivo

## 📊 Métricas de Avaliação

- **Acurácia**: Proporção de predições corretas
- **Precisão**: Proporção de vitórias preditas corretamente
- **Recall**: Proporção de vitórias reais identificadas
- **F1-Score**: Média harmônica entre precisão e recall
- **Matriz de Confusão**: Visualização de acertos e erros

## 🔍 Principais Descobertas

O notebook gera análises detalhadas incluindo:

- **Melhor modelo**: Identificação do algoritmo com melhor desempenho
- **Features críticas**: Atributos que mais influenciam nas vitórias
- **Jogador-chave**: Identificação do jogador mais impactante
- **Evolução temporal**: Como o modelo performa ao longo das temporadas
- **Fator casa**: Diferença de desempenho entre casa e fora

## 📦 Saídas Geradas

O notebook gera automaticamente:

- 📊 Gráficos de distribuição de resultados
- 📈 Matrizes de confusão para cada modelo
- 🎯 Análise de importância de features
- 👤 Ranking de jogadores mais importantes
- 📉 Comparação visual entre experimentos
- ⏱️ Evolução temporal da acurácia

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Pandas & NumPy**: Manipulação de dados
- **Scikit-learn**: Algoritmos de ML e métricas
- **XGBoost, LightGBM, CatBoost**: Algoritmos de boosting
- **Matplotlib & Seaborn**: Visualização de dados
- **Jupyter Notebook**: Ambiente de desenvolvimento

## 📝 Notas Importantes

- Os dados dos jogadores devem estar no formato CSV específico
- O notebook está otimizado para o FC Barcelona, mas pode ser adaptado para outros times
- Não utiliza balanceamento SMOTE - mantém a distribuição natural das classes
- Suporta execução tanto local quanto no Google Colab

## 👨‍💻 Autor

Desenvolvido como Trabalho de Conclusão de Curso (TCC)

## 📄 Licença

Este projeto é de código aberto para fins educacionais e de pesquisa.

---

**⚠️ Disclaimer**: Este projeto é para fins acadêmicos e de pesquisa. Os resultados das predições não devem ser utilizados para apostas ou fins comerciais.