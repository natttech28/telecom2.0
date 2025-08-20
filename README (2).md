

## Propósito da Análise
O objetivo desta segunda parte do projeto é **desenvolver modelos preditivos capazes de identificar clientes com maior probabilidade de cancelar os serviços da Telecom X**.  
A previsão do **churn** (evasão de clientes) permite que a empresa antecipe ações estratégicas de retenção, reduzindo perdas financeiras e melhorando a satisfação do cliente.

---

## Estrutura do Projeto
- `telecomx_churn_modelagem.ipynb` → Notebook principal com o pipeline de modelagem preditiva.  
- `dados_tratados.csv` → Conjunto de dados tratado na Parte 1 (ETL e EDA), utilizado como entrada para a modelagem.  
- `visualizacoes/` → Pasta opcional para armazenar gráficos gerados durante a análise.  
- `README.md` → Documento explicativo do projeto.  

---

## Preparação dos Dados
### Classificação das variáveis
- **Numéricas**: colunas como `tenure`, `MonthlyCharges`, `TotalCharges`.  
- **Categóricas**: colunas como `Contract`, `PaymentMethod`, `InternetService`.  

### Etapas de pré-processamento
1. **Encoding**: variáveis categóricas transformadas via *One-Hot Encoding*.  
2. **Normalização**: variáveis numéricas padronizadas com *StandardScaler*.  
3. **Divisão dos dados**: separação em treino (80%) e teste (20%), garantindo avaliação justa dos modelos.  

---

## Modelagem Preditiva
Foram testados dois algoritmos principais:  
- **Regressão Logística** → modelo baseline, simples e interpretável.  
- **Random Forest** → modelo de árvore de decisão mais robusto, capaz de capturar relações não-lineares.  

### Avaliação
- **Métricas**: Accuracy, Precision, Recall, F1-score e AUC-ROC.  
- **Matriz de confusão**: análise dos erros de classificação.  
- **Importância das variáveis**: identificação dos principais fatores de churn.  

---

## Exemplos de Insights (EDA + Modelagem)
- Clientes com **contratos mensais** têm maior propensão ao churn.  
- **Tempo de permanência baixo (tenure)** aumenta as chances de cancelamento.  
- **Mensalidades mais altas** estão associadas a maior evasão.  
- Métodos de pagamento como **cartão de crédito automático** tendem a reduzir o churn.  

Gráficos incluídos no notebook:
- Distribuição de churn por tipo de contrato.  
- Importância das variáveis no modelo Random Forest.  
- Curva ROC comparando os modelos.  

---

##  Instruções de Execução
1. Certifique-se de ter o Python 3 instalado.  
2. Instale as dependências necessárias:  
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Coloque o arquivo `dados_tratados.csv` na mesma pasta do notebook.  
4. Execute o notebook `telecomx_churn_modelagem.ipynb` do início ao fim.  

---

## Conclusão Estratégica
Os principais fatores que influenciam a evasão foram:  
- Tipo de contrato (mensal).  
- Tempo de permanência baixo.  
- Valor da mensalidade.  

Esses resultados sugerem que a **Telecom X deve investir em planos anuais ou bienais mais atrativos, reduzir barreiras iniciais para novos clientes e oferecer benefícios financeiros para clientes de alto risco**.  
