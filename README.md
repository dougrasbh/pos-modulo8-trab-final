# 📘 Projeto: Detecção de Doenças Cardíacas com Machine Learning

Este projeto foi desenvolvido como Trabalho Prático da disciplina **Machine Learning Aplicado II**, com foco em treinar e avaliar modelos capazes de prever a presença de doenças cardíacas com base em indicadores clínicos.

---

## 👥 Membros da Equipe
- **Arthur Bezerra**  
- **Debora Barros**  
- **Ronald Boadana**

---

## 📊 Descrição do Problema

O objetivo do projeto é prever se um paciente possui risco de doença cardíaca utilizando atributos clínicos fornecidos no dataset *Heart Disease UCI*.

A variável alvo é **`target`**, onde:  
- `0` → Ausência de doença cardíaca  
- `1` → Presença de doença cardíaca  

O dataset inclui variáveis como:
  1. Idade: Númerica
  2. Sexo: Categórica
  3. Tipo de Dor no Peito: Categórica
  4. Pressão Arterial em Repouso: Numérica
  5. Colesterol: Numérica
  6. Glicemia em Jejum (≥ 120 mg/dl = 1, senão 0): Categórica
  7. ECG em Repouso: Catégorica
  8. Frequência Cardíaca Máxima Alcançada: Numérica
  9. Angina Induzida por Exercício: Categórica
  10. Depressão do Segmento ST: Numérica
  11. Inclinação do Segmento ST: Categórica
  12. Doença Cardíaca (1 = sim, 0 = não): Categórica (variável alvo) 

---

## 🧹 Pré-processamento dos Dados

Para garantir melhor qualidade e desempenho dos algoritmos, realizamos:

### ✔️ Tratamento de Outliers
Valores discrepantes em variáveis numéricas foram substituídos pela **mediana** da coluna correspondente.

### ✔️ Balanceamento de Classes (SMOTE)
Como o dataset apresenta desbalanceamento entre as classes, aplicamos **SMOTE** (Synthetic Minority Over-sampling Technique) para aumentar sinteticamente exemplos da classe minoritária, tornando o treinamento dos classificadores mais robusto.

### ✔️ Normalização / Padronização
Escalonamento aplicado para melhorar o desempenho de modelos sensíveis à escala (KNN e SVC).

### ✔️ Redução de Dimensionalidade (PCA) — Experimentos com e sem PCA
Realizamos experimentos comparativos **com e sem PCA**:
- *Sem PCA* — treinamento direto sobre as features pré-processadas (após SMOTE e escalonamento).  
- *Com PCA* — aplicamos PCA após o escalonamento para reduzir dimensionalidade e avaliamos o impacto na performance de cada modelo.

### ✔️ Divisão Treino/Teste
- **Treino:** 80%  
- **Teste:** 20%  

---

## 🤖 Modelos Utilizados

Foram treinados e avaliados os seguintes algoritmos:

- **RandomForestClassifier**  
- **KNeighborsClassifier**  
- **LogisticRegression**  
- **DecisionTreeClassifier**  
- **SVC (Support Vector Classifier)**

Para cada modelo, analisamos:
- Acurácia  
- Precisão  
- Recall  
- F1-Score

O F1-Score foi escolhido como métrica para comparação dos modelos

Os resultados incluem comparações:
- modelos **com SMOTE**
- treinamentos **com PCA** vs **sem PCA**  
O notebook destaca o melhor cenário/combinação obtida.

---

## 🚀 Como Executar o Projeto

### 1️⃣ Coloque o arquivo `heart.csv` na raiz do projeto  
Se estiver usando Google Colab ou Kaggle, apenas envie o arquivo para o ambiente.
