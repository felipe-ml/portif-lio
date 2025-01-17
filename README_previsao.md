# Projeto de Previsão de Valores Imobiliários

## Descrição
Este projeto implementa uma solução completa para previsão de valores de imóveis com base em dados geográficos, socioeconômicos e estruturais. Ele segue o fluxo de desenvolvimento de um modelo de aprendizado supervisionado, desde a preparação dos dados até a validação de modelos de regressão.

---

## Estrutura do Projeto
1. **Leitura e Análise Inicial dos Dados**
   - O conjunto de dados `housing.csv` é carregado utilizando `pandas`.
   - Análises básicas incluem verificação do cabeçalho e informações gerais do DataFrame.

2. **Divisão dos Dados**
   - Implementação manual e com bibliotecas de métodos para dividir o conjunto em treino e teste:
     - Divisão aleatória.
     - Divisão utilizando o último byte do hash (método de hashlib).
     - Uso do `train_test_split` da biblioteca Scikit-Learn.
   - Estratificação dos dados com base na renda mediana.

3. **Visualização de Dados**
   - Diagramas de dispersão para analisar padrões geográficos e características populacionais.
   - Visualização de correlações com base no coeficiente de Pearson e gráficos de dispersão.

4. **Preparação dos Dados**
   - Transformações numéricas e categóricas:
     - Imputação de valores faltantes com a mediana.
     - Codificação one-hot para atributos categóricos.
   - Atributos derivados criados incluem:
     - Quartos por domicílio.
     - Habitantes por domicílio.
     - Quartos por número total de cômodos.

5. **Construção de Pipelines**
   - Criação de pipelines de transformação para lidar separadamente com dados numéricos e categóricos.
   - Combinação dos pipelines em uma única etapa com `FeatureUnion`.

6. **Modelos de Regressão**
   - Treinamento e avaliação de modelos de regressão:
     - Regressão linear.
     - Árvore de decisão.
     - Regressor de floresta aleatória.
   - Utilização de validação cruzada (k-fold) para medir desempenho.

7. **Ajuste de Hiperparâmetros**
   - Uso do `GridSearchCV` para encontrar a melhor combinação de hiperparâmetros para o modelo de regressão com floresta aleatória.
   - Análise das importâncias de atributos.

---

## Requisitos
- Python 3.x
- Bibliotecas:
  - pandas
  - numpy
  - matplotlib
  - scikit-learn

---

## Como Executar
1. **Pré-requisitos**
   - Instale as bibliotecas necessárias utilizando `pip install -r requirements.txt`.

2. **Execução**
   - Garanta que o arquivo `housing.csv` esteja no mesmo diretório do código.
   - Execute o script ou notebook em um ambiente Python compatível (como Jupyter Notebook ou Google Colab).

3. **Personalização**
   - Ajuste o parâmetro de estratificação (`income_cat`) para explorar diferentes distribuições de renda.
   - Experimente novos hiperparâmetros no `GridSearchCV` para aprimorar o desempenho do modelo.

---

## Resultados Esperados
- Predições dos valores medianos das casas com base em variáveis preditoras.
- Avaliação quantitativa dos modelos por meio do RMSE (Raiz do Erro Quadrático Médio).
- Análise das importâncias relativas dos atributos no modelo ajustado.

---

## Limitações
- O conjunto de dados é limitado a uma região específica.
- O modelo pode superestimar ou subestimar se houver variáveis não incluídas.

---

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para criar issues ou pull requests.

---

## Autor
- Este código foi desenvolvido como parte de um exercício baseado em aprendizado de máquina.
