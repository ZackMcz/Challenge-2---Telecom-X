# Challenge-2---Telecom-X
Desafio para análise de dados na Telecom X -  projeto "Churn de Clientes"

# Análise de Clientes (Churn)


## 📌 Introdução

Este projeto apresenta uma análise detalhada sobre a evasão de clientes (Churn) em uma empresa de telecomunicações. A partir de dados limpos e estruturados, foram identificados os principais padrões que contribuem para o cancelamento de serviços, com o objetivo de propor ações para retenção de clientes.

# Relatório de Análise de Evasão de Clientes (Churn)

## Introdução

Este relatório apresenta uma análise exploratória dos dados de telecomunicações com o objetivo de entender os fatores que levam à evasão de clientes (Churn). A evasão de clientes é um desafio significativo para as empresas de telecomunicações, impactando diretamente a receita e o crescimento. Compreender por que os clientes saem é o primeiro passo para desenvolver estratégias eficazes de retenção.

## Limpeza e Tratamento de Dados

Os dados foram extraídos de um arquivo JSON (`TelecomX_Data.json`). O arquivo continha informações aninhadas que foram normalizadas para criar um DataFrame plano. Durante o processo de limpeza e tratamento, as seguintes etapas foram realizadas:

*   **Normalização de Dados Aninhados:** As colunas aninhadas ('customer', 'phone', 'internet', 'account') foram expandidas em colunas separadas.
*   **Tratamento da Coluna 'Charges.Total':** Identificamos que a coluna 'Charges.Total' foi inicialmente tratada incorretamente com One-Hot Encoding devido ao grande número de valores únicos. Corrigimos isso convertendo a coluna para o tipo numérico, tratando valores ausentes (coercedos para NaN).
*   **Conversão de Variáveis Binárias:** Colunas categóricas binárias como 'Partner', 'Dependents', 'PhoneService' e 'PaperlessBilling' foram convertidas para representação numérica (0 e 1).
*   **One-Hot Encoding:** As colunas categóricas com mais de dois valores únicos (excluindo 'customerID', 'Churn', 'Charges.Total' e 'gender') foram codificadas usando One-Hot Encoding para prepará-las para modelagem.
*   **Tratamento de Valores Ausentes em 'Churn':** Linhas com valores ausentes na coluna 'Churn' foram removidas para garantir a integridade dos dados para análise e modelagem.
*   **Criação da Coluna 'Charges.Daily':** Uma nova coluna 'Charges.Daily' foi criada dividindo o 'Charges.Monthly' por 30 para analisar o custo diário.

## Análise Exploratória de Dados

A análise exploratória de dados (EDA) foi realizada para identificar padrões e relações nos dados. As visualizações geradas incluem:

**Distribuição da Evasão (Churn):**

A distribuição geral da evasão mostra a proporção de clientes que permaneceram (0) e saíram (1).

**Distribuição de Encargos Mensais e Diários por Churn:**

Box plots foram utilizados para comparar a distribuição de encargos mensais e diários entre clientes que permaneceram e clientes que saíram.

**Distribuição de Churn por Variáveis Categóricas:**

Gráficos de contagem foram gerados para examinar a relação entre o churn e variáveis categóricas como gênero, tipo de contrato e método de pagamento.


