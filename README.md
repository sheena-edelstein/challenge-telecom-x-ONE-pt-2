# 📡 Projeto Telecom X: Predição de Churn com Machine Learning

![Status do Projeto](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![Python](https://img.shields.io/badge/Python-3.12-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)

## 🎯 Propósito da Análise
O objetivo principal deste projeto é desenvolver um modelo preditivo de alta precisão para identificar o **Churn** (evasão de clientes) na Telecom X. Através do processamento de dados históricos e comportamento de consumo, o modelo busca fornecer insights acionáveis para que a equipe de retenção possa intervir antes que o cliente finalize o contrato.

## 📂 Estrutura do Projeto
A organização dos arquivos segue as melhores práticas de Data Science:

* `TelecomX_BR.ipynb`: Notebook principal com todo o pipeline de extração, limpeza, modelagem e avaliação.
* `dados_tratados.csv`: Base de dados limpa e estruturada utilizada para o treinamento.
* `Visualizacoes/`: Pasta contendo os prints dos gráficos de Matriz de Confusão e Feature Importance.

## 🛠️ Processo de Preparação dos Dados

### 1. Classificação de Variáveis
As variáveis foram segmentadas para aplicação das técnicas corretas:
* **Numéricas:** `tenure`, `MonthlyCharges` e `TotalCharges`.
* **Categóricas:** `gender`, `Contract`, `InternetService`, `PaymentMethod`, entre outras.

### 2. Engenharia de Features e Codificação
Para tornar os dados compatíveis com os algoritmos matemáticos, aplicamos:
* **Achatamento de JSON:** Dados aninhados foram transformados em colunas tabulares.
* **One-Hot Encoding:** Transformação de variáveis categóricas em colunas binárias (0 e 1), utilizando `drop_first=True` para evitar a colinearidade.
* **Padronização (StandardScaler):** Essencial para a **Regressão Logística**, garantindo que todas as variáveis numéricas estivessem na mesma escala (média 0 e desvio 1).
* **Balanceamento (SMOTE):** Técnica de oversampling para equilibrar a classe minoritária (Churn), permitindo que o modelo aprenda melhor os padrões de evasão.

### 3. Divisão de Dados
Os dados foram divididos em **70% para treino** e **30% para teste**, utilizando **estratificação** para manter a proporção original de Churn em ambos os conjuntos.

## 🧠 Modelagem e Justificativas
Optamos pela implementação de dois modelos distintos:
1.  **Regressão Logística:** Escolhida por sua alta interpretabilidade, permitindo entender o peso estatístico de cada variável na evasão.
2.  **Random Forest:** Escolhido por sua robustez e capacidade de captar relações não-lineares complexas, além de não ser sensível à escala dos dados brutos.



## 📊 Insights e Visualizações (EDA)
Durante a Análise Exploratória de Dados, identificamos padrões críticos:
* **Risco Temporal:** O gráfico de *Boxplot* revelou que o Churn ocorre predominantemente nos primeiros 12 meses de contrato.
* **Impacto Financeiro:** A análise de densidade mostrou que clientes com contratos "Month-to-month" e pagamentos via "Electronic check" possuem a maior taxa de evasão.
* **Matriz de Correlação:** Variáveis como `tenure` (negativa) e `TotalCharges` (positiva) mostraram-se preditores fundamentais.



## 🚀 Como Executar o Projeto

1. **Pré-requisitos:**
   Certifique-se de ter o Python instalado. Recomenda-se o uso do Google Colab ou um ambiente virtual (venv).

2. **Instalação de Bibliotecas:**
   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn imbalanced-learn

## Execução
1. Clone este repositório.
2. Certifique-se de que o arquivo dados_tratados.csv está na mesma pasta que o notebook.
3. Abra o TelecomX_BR.ipynb no Google Colab ou no Jupyter Notebook.
4. Execute as células em ordem para visualizar o processamento e o treinamento dos modelos.

## Gráficos
<img width="1114" height="490" alt="image" src="https://github.com/user-attachments/assets/5c8d87d2-06e6-4f8f-81aa-ea938dd270fa" />
<img width="1489" height="1190" alt="image" src="https://github.com/user-attachments/assets/7cb64883-225a-4bfd-81e8-089fcb048f1f" />
<img width="1790" height="490" alt="image" src="https://github.com/user-attachments/assets/47c27219-9530-4ca1-a49e-7b3119ad5589" />
<img width="873" height="779" alt="image" src="https://github.com/user-attachments/assets/6c23efdb-7b91-4509-8bb4-44e33764d4d3" />
<img width="846" height="547" alt="image" src="https://github.com/user-attachments/assets/fd4698b2-de93-4c3e-add3-36ab74535432" />
<img width="1144" height="1056" alt="image" src="https://github.com/user-attachments/assets/6f70e7e7-65b5-45f6-af0c-46cc3355baef" />
<img width="841" height="547" alt="image" src="https://github.com/user-attachments/assets/83b1e6d4-6d61-4469-8529-e19099fc1783" />
<img width="872" height="547" alt="image" src="https://github.com/user-attachments/assets/0eddf1f3-d55e-44fa-9745-8b497d9b1566" />
<img width="1014" height="624" alt="image" src="https://github.com/user-attachments/assets/45f0471d-0aa9-41b5-87b4-d95dd90109b1" />
<img width="532" height="477" alt="image" src="https://github.com/user-attachments/assets/6ac14273-2468-45e3-a046-1358795ca725" />
<img width="532" height="476" alt="image" src="https://github.com/user-attachments/assets/87e4987e-86fd-45d2-b7aa-2336c88ec089" />
<img width="1083" height="548" alt="image" src="https://github.com/user-attachments/assets/9472c172-1197-4014-a305-9e860e045cfa" />
<img width="1057" height="548" alt="image" src="https://github.com/user-attachments/assets/2f940fbe-ada3-4c46-8e11-6fd3f55b16d8" />
