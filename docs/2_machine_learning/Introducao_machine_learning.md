# 1. Introdução ao Machine Learning

## 1.1. O Que é Machine Learning?

**Machine Learning (Aprendizado de Máquina)** é um subcampo da Inteligência Artificial que utiliza algoritmos estatísticos para permitir que sistemas "aprendam" com dados, identificando padrões e tomando decisões com intervenção humana mínima.

---

## 1.2. Relação com a Estatística

O Machine Learning é essencialmente **Estatística computacional em ação**. Enquanto a Estatística tradicional foca em inferência e testes de hipóteses, o ML prioriza a predição e a automatização. Ambas compartilham:

- Modelos de regressão e classificação  
- Técnicas de validação cruzada  
- Métricas de desempenho (RMSE, AUC-ROC)  
- Tratamento de viés e variância

---

## 1.3. Principais Categorias

1. **Aprendizado Supervisionado**  
   (Dados rotulados - Regressão/Classificação)  
   Ex: Prever preços de imóveis (Regressão Linear) ou diagnosticar doenças (Árvores de Decisão)

2. **Aprendizado Não-Supervisionado**  
   (Dados não rotulados - Clusterização)  
   Ex: Segmentação de clientes (K-Means), Redução de dimensionalidade (PCA)

3. **Aprendizado por Reforço**  
   (Sistemas que aprendem por tentativa e erro)  
   Ex: Jogos autônomos, Robótica

---

## 1.4. Por Que Combinar Estatística e ML?

| Estatística Clássica          | Machine Learning             |
|-------------------------------|------------------------------|
| Foco em interpretabilidade    | Foco em performance preditiva|
| Amostras menores              | Grandes volumes de dados     |
| Testes de significância       | Otimização de hiperparâmetros|

---

## 1.5. Aplicações Práticas
🏥 **Saúde:** Diagnóstico de câncer com redes neurais

🏦 **Finanças:** Detecção de fraudes em transações

🛒 **Varejo:** Sistemas de recomendação (como os da Amazon/Netflix)

>"Machine Learning é estatística em esteróides, mas sem compreensão >estatística, você estará apenas pressionando botões aleatórios." — John Tukey

---

# 2. Tópicos de Machine Learning

## 2.1. classificação versus regressão

Existem duas categorias de problemas que podem ser bem resolvidos com a utilização de Machine Learning: os de classificação e os de regressão.

### 2.1.1. Classificação
Quando precisamos prever a qual categoria pertence uma determinada amostra, trata-se de um problema de classificação. Alguns exemplos que podemos citar são:

Prever se um(a) determinado(a) paciente está com Covid.
Se um(a) cliente está propenso(a) a desistir da compra.
Se algum(a) usuário(a) web está propenso(a) a clicar em um anúncio.
Nesses casos mencionados, a previsão se concentra em 0 ou 1 (Covid/não Covid, desistir/não desistir, clicar/não clicar) que é denominada de classificação binária, na qual existem somente duas classes. Há também casos em que a classificação se dá com mais duas classes, chamada de classificação multiclasse, como a filtragem dos e-mails em “principal”, “social”, “promoções”, “importantes” ou “fóruns”.

Entre os algoritmos de classificação podemos citar:

- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Decision Tree Classifier
- Random Forest Classifier

### 2.1.2. Regressão
Quando precisamos prever um valor numérico específico, isso indica que estamos lidando com um problema de regressão. Alguns exemplos desses problemas estão relacionados à previsão de:

- preços/custos futuros;
- estoque;
- receita futura.

Nessas situações, podemos utilizar algum modelo de regressão para realizar essas previsões e apresentar como resposta algum valor contínuo relacionado ao problema. Existem diferentes tipos de algoritmos de machine learning utilizados para resolver esse tipo de problema:

- Linear Regression;
- Random Forest Regressor;
- Support Vector Regression (SVR).

[Fonte](https://cursos.alura.com.br/course/machine-learning-classificacao-tras-panos/task/107923)

# 3. Conteúdos disponíveis

- [**2.1. Crisp-DM**](./2.1_CRISP-DM/2.1.1_CRISP-DM.md)
- [**2.2. Pré Treinamento**](./2.1_CRISP-DM/2.1.2_Pre_treinamento.md)
- [**2.3.Treinamento**](./2.1_CRISP-DM/2.1.3_Treinamento.md)
- [**2.4. Pós Treinamento**](./2.1_CRISP-DM/2.1.4_Pos_treinamento.md)

---