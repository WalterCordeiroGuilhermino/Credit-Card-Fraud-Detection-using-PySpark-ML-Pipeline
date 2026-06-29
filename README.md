# Credit-Card-Fraud-Detection-using-PySpark-ML-Pipeline

# 💳 Credit Card Fraud Detection using PySpark ML Pipeline

## 📌 Sobre o Projeto
Este projeto foi desenvolvido como trrabalho acadêmico para minha pós graduação em ciencia de dados pela Extecamp de Unicam onde baseado em uma database de teste para detecção de transações fraudulentas em cartões de crédito foi utilizando a biblioteca **Spark ML** no ambiente do Google Colab. Esse trabalho tem como objetivo principal é demonstrar a capacidade de engenharia de dados e estruturação de arquiteturas preditivas em cenários de Big Data.

## 🛠️ Arquitetura do Pipeline (Spark ML)
Os dados brutos passam por uma esteira automatizada de transformação antes de alimentar o modelo preditivo:
1. **Tratamento de Strings (`StringIndexer`):** Conversão de variáveis categóricas textuais (`gender`, `category`) em índices numéricos.
2. **Codificação Vetorial (`OneHotEncoder`):** Transformação dos índices em vetores binários esparsos para evitar distorções de pesos matemáticos.
3. **Consolidação de Features (`VectorAssembler`):** Agrupamento do valor da transação (`amt`) e dos vetores gerados em uma estrutura única de atributos.
4. **Modelo Classificador (`LogisticRegression`):** Algoritmo de classificação binária treinado com limite de iterações (`maxIter=10`).

## 📊 Avaliação e Métricas
Dada a natureza altamente desbalanceada do dataset de fraudes, o modelo foi avaliado utilizando duas métricas distintas:
* **Acurácia (Accuracy):** Avaliação global de acertos do modelo.
* **AUC-ROC (Area Under ROC):** Métrica principal utilizada para validar a capacidade real do modelo em discriminar uma transação legítima de uma fraude sem sofrer distorções pelo desbalanceamento do banco.



