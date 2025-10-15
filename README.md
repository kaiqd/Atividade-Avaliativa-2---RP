# Clusterização de Vinhos com PCA e K-Means

Este projeto aplica **PCA** para reduzir a dimensionalidade do *Wine dataset* (scikit-learn) de 13 para **2 componentes principais** e, em seguida, executa **K-Means (k = 3)** sobre os dados reduzidos para identificar grupos de vinhos com perfis químicos semelhantes. Os resultados são apresentados em dois gráficos comparativos.

## O que o script faz

1. **Carregamento e preparação dos dados**
   - Carrega o *Wine dataset* (`load_wine`), com 178 amostras e 13 características químicas.
   - Aplica **padronização** com `StandardScaler` (etapa necessária para PCA).

2. **Redução de dimensionalidade (PCA)**
   - Ajusta `PCA(n_components=2)` sobre os dados padronizados.
   - Gera a matriz projetada em 2D e informa a **variância explicada total** pelos dois componentes.

3. **Clusterização (K-Means)**
   - Executa `KMeans(n_clusters=3, random_state=42, n_init=10)` sobre as componentes principais.
   - Atribui o rótulo de cluster para cada amostra e guarda os **centróides**.

4. **Visualização**
   - **Gráfico 1**: dispersão em PC1 × PC2 com as **atribuições do K-Means** (e centróides marcados com “X”).
   - **Gráfico 2**: a mesma projeção, colorida pelas **classes reais** do dataset (apenas para comparação visual).



