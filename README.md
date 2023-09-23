# Bagging e Random forest

# 1° - O Bagging (Bootstrap Aggregating)

O Bagging é uma técnica de aprendizado de máquina que funciona da seguinte forma:

1. Dividimos nossos dados de treinamento em várias partes (subconjuntos).

2. Em cada parte, treinamos um modelo de aprendizado de máquina, como uma árvore de decisão.
 
3. Depois que todos os modelos são treinados, eles trabalham juntos para fazer previsões em novos dados.

4. A resposta final é obtida combinando as previsões de todos os modelos. Geralmente, usamos a "votação" ou "média" para escolher a resposta final.

Essa técnica ajuda a tornar nossas previsões mais precisas e confiáveis porque estamos considerando várias opiniões de diferentes modelos. É como perguntar a várias pessoas e tirar uma conclusão com base em todas as respostas.


# 2° - O Random Forest

O Random Forest é uma técnica de aprendizado de máquina que usa várias árvores de decisão para fazer previsões mais precisas. Aqui está como funciona:

1. Dividimos nossos dados de treinamento em várias partes chamadas "conjuntos de treinamento".

2. Em cada conjunto de treinamento, treinamos uma árvore de decisão, que é um modelo de aprendizado de máquina.

3. Depois que todas as árvores são treinadas, elas trabalham juntas para fazer previsões em novos dados.

4. A resposta final é determinada pela maioria das previsões das árvores (votação). Para problemas de classificação, a classe com mais votos é escolhida como a previsão final. Para problemas de regressão, a média das previsões é usada.

5. O Random Forest é eficaz porque as árvores são treinadas em subconjuntos diferentes dos dados e características, tornando as previsões mais estáveis e precisas.

Em resumo, o Random Forest é uma técnica que usa muitas árvores de decisão trabalhando juntas para fazer previsões melhores e mais confiáveis em problemas de aprendizado de máquina.

# *Explicação dos hiperparâmetros de Random Forest*

* **n_estimators:** Quanto maior o número de árvores, melhor a generalização do modelo, mas também maior o tempo de treinamento.
* **criterion:** A métrica de avaliação para dividir os nós. As opções mais comuns são **gini** e **entropy**.
* **max_depth:** Quanto maior a profundidade, mais complexo o modelo, mas também mais propenso a overfitting.
* **min_samples_split:** Quanto maior o número, mais conservador o modelo, mas também menos propenso a overfitting.
* **min_samples_leaf:** Quanto maior o número, mais conservador o modelo, mas também menos propenso a overfitting.
* **min_weight_fraction_leaf:** Quanto menor o número, mais o modelo pode se concentrar em classes minoritárias.
* **max_features:** Quanto maior o número, mais flexível o modelo, mas também mais propenso a overfitting.
* **max_leaf_nodes:** Limita o número de folhas em cada árvore.
* **min_impurity_decrease:** Um nó só será dividido se a divisão melhorar a impureza em pelo menos um valor especificado.
* **bootstrap:** Se amostras bootstrap são usadas ao construir árvores.
* **oob_score:** Usa amostras out-of-bag para estimar a pontuação de generalização.
* **n_jobs:** Usa vários núcleos para acelerar o treinamento.
* **random_state:** Gera resultados reproduzíveis.
* **verbose:** Controla a verbosidade do treinamento.
* **warm_start:** Usa a solução da chamada anterior para ajustar o modelo.
* **class_weight:** Dá pesos diferentes às classes para compensar um desbalanceamento.
* **ccp_alpha:** Usa poda de complexidade mínima para reduzir a complexidade do modelo.
* **max_samples:** Limita o número de amostras usadas para treinar cada árvore.

**Observações:**

* Os valores padrão dos hiperparâmetros podem não ser ótimos para todos os datasets. Portanto, é frequentemente necessário ajustar os hiperparâmetros para melhorar o desempenho do modelo.
* A explicação dos hiperparâmetros é apenas um resumo. Para mais informações, consulte a documentação do Random ForestClassifier.

# A diferença entre os dois:

Bagging é uma técnica que combina várias cópias do mesmo modelo (por exemplo, árvores de decisão) em conjuntos de dados diferentes, enquanto o Random Forest é uma extensão do Bagging que introduz aleatoriedade nas árvores de decisão por meio de seleção aleatória de características, resultando em um conjunto mais diversificado de árvores. O Random Forest tende a ser mais robusto e preciso em comparação com o Bagging padrão.
