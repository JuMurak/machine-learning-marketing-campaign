# Modelagem e Avaliação do Dataset “Marketing Campaign”
Trabalho Final – Parte 2  
Disciplina: Introdução ao Aprendizado de Máquina  
Instituto Federal de São Paulo – Câmpus Campinas  
Docente: Everton Meyer da Silva  

## Integrante
- **Juliana Murakami**

---

# 1. Descrição do Tema
Este projeto apresenta a modelagem e avaliação de algoritmos de Machine Learning aplicados ao dataset **Marketing Campaign**, que contém informações de clientes e dados históricos de campanhas de marketing.

O objetivo preditivo deste trabalho é classificar a variável **Response**, que indica se um cliente aceitou (1) ou não aceitou (0) uma oferta de campanha.  
A tarefa é relevante porque permite que empresas direcionem esforços de marketing para consumidores com maior probabilidade de conversão, otimizando recursos e aumentando o impacto das campanhas.

---

# 2. Base de Dados Utilizada
A base de dados foi obtida oficialmente no Kaggle, no link:

🔗 **https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign?resource=download**

Cada linha representa um cliente e contém atributos como:
- Perfil demográfico (idade, escolaridade, estado civil)
- Renda anual
- Gastos em diferentes categorias de produtos
- Recência da última compra
- Histórico de aceitação de campanhas anteriores

A variável alvo utilizada na modelagem foi **Response**.

---

# 3. Notebook do Projeto
O notebook completo contém:

- Carregamento da base diretamente com `kagglehub`
- Pré-processamento (remoção de nulos, criação de atributos, encoding e normalização)
- Construção do pipeline com `ColumnTransformer`
- Treinamento dos modelos:
  - Regressão Logística  
  - Random Forest  
  - K-Nearest Neighbors (KNN)
- Avaliação utilizando:
  - accuracy  
  - precision  
  - recall  
  - f1-score  
  - ROC-AUC  
- Execução de validação cruzada **Stratified K-Fold (5 folds)**

 Arquivo: `parte2_marketing_campaign-final.ipynb`

---

# 4. Principais Resultados

### ✔ Regressão Logística
- Melhor equilíbrio entre recall da classe positiva e ROC-AUC  
- Maior capacidade de identificação dos clientes que aceitam a campanha  

### ✔ Random Forest
- Maior acurácia global  
- Recall menor para a classe positiva  

### ✔ KNN
- Resultado intermediário  
- Maior variação entre folds na validação cruzada  

**Modelo escolhido:** *Regressão Logística*, por apresentar o melhor equilíbrio entre desempenho e estabilidade.

---

# 5. Como Executar o Projeto

### **Requisitos**
- Python 3.10+
- Jupyter Notebook
- Bibliotecas:
