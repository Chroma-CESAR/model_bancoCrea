## Descrição
A utilização do modelo de classificação de despesas em Machine Learning começa com o processamento e análise dos dados disponíveis na planilha. Essa planilha contém registros de despesas categorizadas em 13 classes diferentes, como 
"Aluguel", "Contas de Consumo", "Educação", entre outras, numeradas de 0 a 12.

O objetivo do modelo é prever a categoria de uma nova despesa com base em características como valor, data, descrição ou outros atributos relevantes. 

<br>

## Técnicas Usadas
### Random Forest
O Random Forest é um modelo de Machine Learning baseado em um conjunto de árvores de decisão. Ele funciona assim:

Cria várias árvores de decisão independentes, cada uma treinada com diferentes subconjuntos dos dados.
Cada árvore faz uma previsão e, no final, o modelo combina os resultados de todas elas. Para classificação, ele usa a maioria dos votos; para regressão, faz uma média dos resultados.
Esse modelo é robusto, lida bem com dados complexos e reduz o risco de erros que poderiam ocorrer em uma única árvore, tornando as previsões mais precisas e confiáveis.

### StratifiedKFold
O StratifiedKFold é uma técnica de validação cruzada usada para avaliar modelos de Machine Learning. Ele divide os dados em várias partes (ou "folds"), mas com uma diferença importante: garante que a proporção das classes seja mantida em cada divisão.

Por exemplo, se sua base tem 70% da categoria "A" e 30% da categoria "B", cada parte criada pelo StratifiedKFold também terá essas mesmas proporções. Isso ajuda a evitar distorções nos resultados, especialmente em bases de dados desbalanceadas, 
garantindo que o modelo seja testado de forma justa em diferentes cenários.

<br>

## Processo do Modelo

1. **Pré-processamento dos dados:** Os dados da planilha são organizados e tratados. Isso inclui limpeza de valores inconsistentes, transformação de descrições de texto em vetores
numéricos (usando técnicas como TF-IDF ou embeddings), e codificação de colunas categóricas.

2. **Divisão dos dados:** Os dados são divididos em conjuntos de treinamento e teste, para que o modelo possa aprender e ser avaliado.
   
3. **Treinamento do modelo:** O algoritmo de classificação Random Forests foi escolhido para esse caso por se encaixar melhor no contexto do objetivo. O modelo é treinado para associar as descrições das despesas às categorias corretas com 
base nos exemplos do conjunto de treinamento.

4. **Avaliação:** O modelo é testado com dados que ele ainda não viu, no conjunto de teste, para verificar sua precisão e confiabilidade.

5. **Predição:** Após o treinamento, o modelo pode ser usado para classificar novas despesas automaticamente. Basta fornecer os dados da despesa, e o modelo retorna a categoria correspondente.

Por exemplo, se uma nova entrada contém a descrição "Pagamento de aluguel de escritório", o modelo analisará os padrões aprendidos e poderá classificá-la como pertencente à categoria "Aluguel".

Esse tipo de aplicação é útil para automação financeira, controle de orçamento e análise de despesas de forma eficiente e escalável.

<br>

## Ferramentas Utilizadas
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
