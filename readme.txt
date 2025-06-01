# Título do Projeto:
# Fundamentos de Machine Learning - Ensaio de Machine Learning (Classificação, Regressão e Clusterização)

## Objetivo:
Realizar ensaios comparativos com algoritmos de Machine Learning em cenários de classificação, regressão e clusterização, a fim de entender o comportamento e desempenho de diferentes modelos frente a diferentes tipos de dados. A análise tem como propósito apoiar a escolha mais eficaz de algoritmos em projetos reais de consultoria da empresa Data Money.

**observação:**
1) Os dados utilizados foram pré-tratados e as técnicas e justificativas para tal não foram apresentadas.
2) visando maior treinamento nas técnicas de codificação para a experimentação dos parâmetros foram usados loops for e resultados armazenados em bibliotecas que foram posteriormente convertidas em dataframe. Por isso RandomSeachCV e similares não foram usados.
3) Os resultados poderiam ter sido melhores com a aplicação das técnicas de cross-validation, mas a proposta da disciplina foi de utilizar apenas o HoldOut.

## Principais Bibliotecas Utilizadas:
- numpy, pandas: manipulação de dados
- sklearn: modelagem, métricas
  - Modelos de Classificação:
    - KNeighborsClassifier
    - DecisionTreeClassifier
    - RandomForestClassifier
    - LogisticRegression

  - Modelos de Regressão:
    - LinearRegression, Lasso, Ridge, ElasticNet
    - DecisionTreeRegressor
    - RandomForestRegressor

  - Modelos de Clusterização:
    - K-means
    - Affinity Propagation

## Métricas Utilizadas:
- Para Classificação:
  - accuracy_score
  - precision_score
  - recall_score
  - f1_score

- Para Regressão:
  - mean_squared_error
  - root_mean_squared_error
  - r2_score
  - mean_absolute_error
  - mean_absolute_percentage_error

- Para Clusterização:
  - silhouette score

## Resultados e Discussão
### Classificação:
- O modelo Decision Tree apresentou o melhor desempenho geral, com:

- Acurácia de 94,8% — classifica corretamente a maioria das amostras.

- F1-Score de 0.9403 — ótimo equilíbrio entre precisão e recall.

- Precisão (0.9482) e Recall (0.9325) — baixa taxa de falsos positivos e alta capacidade de detecção de casos positivos.

### Regressão:
- O modelo Random Forest Regressor se destacou com:

- Menor MAE (12.17) e RMSE (16.97) — previsões mais precisas.

- Melhor R²_teste (0.408) — maior capacidade explicativa entre os modelos.

### Clusterização:
- O K-means (n_clusters=3) teve o melhor Silhouette Score (0.2329), superando o Affinity Propagation (0.2238).

- K-means foi mais estável e prático, enquanto o Affinity Propagation se mostrou sensível ao parâmetro preference, gerando muitos clusters inconsistentes.

- Conclusão: K-means é a melhor escolha para esse caso.

Autor: Lucy Gomes de Souza
Projeto Oriundo da disciplina de Princípios de Machine Learning da Comunidade DS.
