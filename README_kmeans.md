# Projeto de Classificação e Clusterização de Clientes

## Descrição
Este projeto implementa uma solução para a análise de dados de clientes por meio de técnicas de pré-processamento, padronização, normalização e clusterização. Utiliza o algoritmo KMeans para agrupar clientes com base em suas características e realiza a análise de clusters gerados, incluindo a visualização em 2D e 3D, além de avaliar a qualidade da clusterização por meio de métricas como o índice de Davies-Bouldin e o escore de Calinski-Harabasz.

---

## Estrutura do Projeto

1. **Leitura e Limpeza dos Dados**
   - O conjunto de dados `CLUSTER.csv` é carregado utilizando `pandas`.
   - Linhas com valores ausentes (NaN) são removidas, além da exclusão de um cliente específico e de colunas desnecessárias.

2. **Pré-processamento dos Dados**
   - O conjunto de dados é padronizado utilizando o `StandardScaler` e normalizado com o `MinMaxScaler` para garantir que as variáveis estejam na mesma escala.
   - A análise das colunas `Genero` e `Produto Mais Vendido` é feita para verificar a distribuição dos dados.

3. **Aplicação do Algoritmo de Clusterização (KMeans)**
   - A técnica KMeans é utilizada para realizar a clusterização dos dados com base nas variáveis `Produto Mais Vendido`, `Idade` e `Genero`.
   - A quantidade de clusters é definida utilizando o Método do Cotovelo.
   - Visualizações dos clusters gerados são feitas em gráficos 2D e 3D.

4. **Avaliação dos Resultados**
   - São calculadas métricas de avaliação da clusterização, como o índice de Davies-Bouldin e o escore de Calinski-Harabasz, para medir a qualidade dos clusters formados.
   
5. **Visualizações**
   - Gráficos de dispersão e histogramas são gerados para mostrar a distribuição dos clientes em cada cluster.
   - Gráficos de barras também são usados para analisar a contagem de diferentes valores para o atributo `Genero` em cada cluster.
   
6. **Exportação dos Resultados**
   - O DataFrame final, com a coluna de cluster atribuída a cada cliente, é exportado para um arquivo CSV para análise posterior.

---

## Requisitos

- Python 3.x
- Bibliotecas:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn

---

## Como Executar

1. **Pré-requisitos**
   - Instale as bibliotecas necessárias utilizando o comando:
     ```bash
     pip install -r requirements.txt
     ```

2. **Execução**
   - Coloque o arquivo `CLUSTER.csv` no mesmo diretório do código.
   - Execute o script no ambiente Python de sua escolha.

3. **Personalização**
   - Ajuste o número de clusters no algoritmo KMeans de acordo com suas necessidades.
   - Explore diferentes visualizações e métricas para avaliar a qualidade da clusterização.

---

## Resultados Esperados

- Análise da clusterização de clientes com base em suas características.
- Visualizações que permitem identificar padrões de agrupamento.
- Métricas de qualidade dos clusters para ajudar a validar a solução de agrupamento.

---

## Limitações

- O desempenho do algoritmo pode variar dependendo da qualidade dos dados fornecidos.
- A análise está limitada aos atributos utilizados no dataset original.

---

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para criar issues ou pull requests.

---

## Autor

- Este código foi desenvolvido como parte de um exercício de análise de dados e clusterização de clientes.
