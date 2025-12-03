# Modelagem e Avaliação do Dataset “Marketing Campaign”
Trabalho Final – Parte 2  
Disciplina: Introdução ao Aprendizado de Máquina  
Instituto Federal de São Paulo – Câmpus Campinas  
Docente: Everton Meyer da Silva  

## 1. Integrante
- Juliana Murakami

---

# 2. Descrição do Tema
Este projeto apresenta a modelagem e avaliação de algoritmos de Machine Learning aplicados ao dataset Marketing Campaign, que reúne informações de clientes e registros de campanhas de marketing anteriores.

O objetivo preditivo consiste em classificar a variável Response, indicando se um cliente aceita (1) ou não aceita (0) uma oferta de campanha. Essa tarefa é relevante para estratégias de marketing porque permite identificar clientes com maior probabilidade de conversão, reduzindo custos e aumentando a eficácia das ações promocionais.

---

# 3. Base de Dados Utilizada
A base de dados foi obtida oficialmente no Kaggle, disponível em:

https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign?resource=download

Cada linha representa um cliente, contendo atributos como idade, escolaridade, estado civil, renda, gastos em categorias específicas de produtos, recência da última compra, histórico de campanhas anteriores e variáveis comportamentais.

A variável alvo utilizada no processo de modelagem foi Response.

---

# 4. Notebook do Projeto
O notebook principal contém:

- Carregamento da base utilizando a biblioteca kagglehub.  
- Pré-processamento: remoção de valores nulos, criação de variáveis derivadas, normalização e codificação.  
- Construção de um Pipeline com ColumnTransformer para organizar o fluxo de transformações.  
- Treinamento de três modelos de classificação:
  - Regressão Logística
  - Random Forest
  - K-Nearest Neighbors (KNN)
- Avaliação dos modelos com accuracy, precision, recall, f1-score e ROC-AUC.
- Execução de validação cruzada do tipo Stratified K-Fold com 5 divisões.  
- Comparação dos resultados para escolha do modelo mais adequado.

Arquivo principal: `parte2_marketing_campaign-final.ipynb`

---

# 5. Como Executar o Projeto (Google Colab)

A forma mais prática de executar o notebook é utilizando o Google Colab, sem necessidade de instalação local.

### Passo a passo para executar:

1. Acesse o Google Colab:  
   https://colab.research.google.com/

2. Clique em "Arquivo" > "Fazer upload de notebook".

3. Envie o arquivo:  
   `parte2_marketing_campaign-final.ipynb`

4. Aguarde o notebook abrir no Colab.

5. Clique em "Ambiente de execução" > "Executar tudo".

6. Caso solicitado, autorize as permissões do ambiente.

Observações importantes:
- Não é necessário fazer download do CSV manualmente, pois o notebook carrega o dataset diretamente do Kaggle via kagglehub.
- Basta executar as células na ordem em que aparecem para reproduzir todo o pipeline de Machine Learning.

---

# 6. Principais Resultados

Resumo dos modelos avaliados:

- Regressão Logística: apresentou o melhor equilíbrio geral entre recall da classe positiva e ROC-AUC, sendo o modelo recomendado para o problema.
- Random Forest: obteve a maior acurácia global, porém com recall reduzido para a classe positiva.
- KNN: desempenho intermediário e maior variação entre os folds na validação cruzada.

O modelo final selecionado foi a Regressão Logística, por apresentar estabilidade, separação superior entre as classes e melhor alinhamento com o objetivo de marketing.

---

# 7. Slides da Apresentação
Os slides utilizados na apresentação fazem parte deste repositório e descrevem de forma visual as etapas do pipeline, os modelos e os resultados obtidos.

Arquivo disponível: `MachineLearning_JuMurak.pptx`

---

# 8. Considerações Finais
O projeto demonstra a aplicação de um pipeline completo de Machine Learning, contemplando pré-processamento, engenharia de atributos, modelagem, avaliação com múltiplas métricas e validação cruzada.  
A análise conduz à escolha de um modelo adequado para priorização de clientes em campanhas de marketing, contribuindo para decisões mais eficientes e baseadas em dados.

---

# 9. Licença
Este repositório tem finalidade acadêmica e segue as diretrizes do trabalho final da disciplina de Introdução ao Aprendizado de Máquina, do IFSP – Câmpus Campinas.
