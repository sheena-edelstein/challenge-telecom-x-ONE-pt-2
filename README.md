# 📡 Detecção de Churn - Telecom X 🚀

![Status](https://img.shields.io/badge/Status-Finalizado-brightgreen)
![Python](https://img.shields.io/badge/Python-3.12+-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)

## 📋 Sobre o Projeto
Este repositório contém o desenvolvimento de um pipeline completo de **Machine Learning** para prever a evasão de clientes (Churn) da empresa Telecom X. O objetivo é identificar perfis com alta probabilidade de cancelamento para permitir ações de retenção direcionadas.

## 🧠 Desafio Técnico
A base de dados original apresentava desafios reais de Ciência de Dados:
- **Dados Aninhados:** Informações em formato JSON/Dicionário que precisavam de "achatamento" (flattening).
- **Desbalanceamento:** Uma proporção maior de clientes ativos em relação aos que evadiram.
- **Tipagem:** Necessidade de conversão de dados financeiros salvos como texto.

## 🛠️ Tecnologias e Ferramentas
* **Linguagem:** Python
* **Bibliotecas:** Pandas, NumPy, Scikit-learn, Imbalanced-learn (SMOTE), Matplotlib e Seaborn.
* **Ambiente:** Google Colab.

## ⚙️ Pipeline de Desenvolvimento

### 1. Pré-processamento
* Limpeza de IDs irrelevantes para evitar *overfitting*.
* Tratamento de valores nulos e conversão de tipos numéricos.
* **One-Hot Encoding:** Transformação de variáveis categóricas para formato binário.

### 2. Balanceamento e Escalonamento
* **SMOTE:** Aplicação de oversampling sintético para equilibrar a classe de Churn.
* **StandardScaler:** Padronização das escalas para modelos lineares.

### 3. Modelagem
Foram treinados e comparados dois modelos:
* **Regressão Logística:** Utilizada como baseline e para interpretação de coeficientes.
* **Random Forest:** Utilizada pela sua robustez e capacidade de capturar relações não-lineares.

## 📊 Resultados e Performance
O modelo **Random Forest** foi o escolhido para o relatório final.

| Métrica | Performance |
| :--- | :--- |
| **Acurácia** | 81% |
| **Recall (Evasão)** | 85% |
| **F1-Score** | 83% |

> **Nota:** O foco foi maximizar o **Recall**, garantindo que a Telecom X identifique o máximo de clientes em risco possível.

## 💡 Insights de Negócio
As variáveis que mais influenciam o Churn identificadas pelo modelo foram:
1. **Tenure (Tempo de Contrato):** Clientes novos têm maior risco.
2. **Tipo de Contrato:** Contratos "Mês a Mês" são os principais gatilhos de saída.
3. **Monthly Charges:** O valor da fatura mensal impacta diretamente na retenção.

## 📁 Estrutura do Repositório
* `notebooks/`: Jupyter Notebook completo com as análises e códigos.
* `data/`: Dataset utilizado no projeto (dados_tratados.csv).
* `reports/`: Relatório final em PDF enviado à diretoria.
