# Challenge-2---Telecom-X
Desafio para análise de dados na Telecom X -  projeto "Churn de Clientes"

# Análise de Clientes (Churn)


## 📌 Introdução

Este projeto apresenta uma análise detalhada sobre a evasão de clientes (Churn) em uma empresa de telecomunicações. A partir de dados limpos e estruturados, foram identificados os principais padrões que contribuem para o cancelamento de serviços, com o objetivo de propor ações para retenção de clientes.

## 🧹 Limpeza e Tratamento de Dados

- **Normalização:** As colunas aninhadas ('customer', 'phone', 'internet' e 'account') foram transformadas em uma estrutura tabular única.
- **Inconsistências:** Valores como `""` e `"No internet service"` foram tratados para evitar distorções na análise.
- **Nulos em 'Churn':** Linhas com valores ausentes na coluna alvo foram removidas, resultando em um DataFrame final com **7043 registros**.
- **Conversão de Tipos:** A coluna `Charges.Total`, inicialmente do tipo string, foi convertida para formato numérico.
- **Nova Feature:** Criada a variável `Charges.Daily`, com base no custo mensal dividido por tempo de permanência.
- **Codificação:** Variáveis categóricas foram convertidas com One-Hot Encoding para análises e modelos futuros.

## 📈 Análise Exploratória de Dados (AED)

- **Análise Descritiva:** Métricas como média, mediana e desvio padrão foram calculadas para variáveis numéricas.
- **Churn por Classe:** Gráficos de contagem confirmam o desequilíbrio entre clientes que evadiram e os que permaneceram.
- **Boxplots de Variáveis Numéricas:** Clientes que evadem tendem a ter menores valores de `Charges.Monthly` e `Charges.Daily`.
- **Categóricas por Churn:** Clientes com contratos "Month-to-month" e pagamento via "Electronic check" apresentam maior taxa de evasão.


