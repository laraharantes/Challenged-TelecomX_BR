# Telecom X - Análise de Evasão de Clientes (Churn)

## 🚀 Propósito da Análise

Este projeto tem como objetivo identificar os principais fatores que contribuem para a evasão de clientes (churn) na empresa fictícia Telecom X. A análise visa orientar a tomada de decisão com base em dados reais, fornecendo insights que ajudem a reduzir o cancelamento de contratos e aumentar a retenção de clientes.

Este projeto foi desenvolvido como parte de um **desafio do curso de Data Science da Alura**.

## 📁 Estrutura do Projeto

```
TelecomX_BR.ipynb       # Notebook principal com todo o processo de análise
TelecomX_Data.json       # Base de dados original em formato JSON
README.md                # Documento de apresentação do projeto
```

## 🧹 Limpeza e Tratamento de Dados

Foram realizadas as seguintes etapas de pré-processamento:

* **Importação e normalização de dados aninhados** do JSON, dividindo informações em colunas como `cliente`, `telefone`, `internet` e `conta`.
* **Padronização dos nomes de colunas** para letras minúsculas e uso de underscores.
* **Conversão de valores categóricos binários** (como "Yes"/"No") para 1 e 0.
* **Tratamento de valores nulos**, como preenchimento da coluna de cobrança total com a média dos valores disponíveis.
* **Conversão de variáveis numéricas e categóricas**, como `seniorcitizen`, `charges_monthly`, `charges_total`.
* **Criação de colunas derivadas**, como `qtd_servicos` (quantidade de serviços contratados).

Essas etapas garantiram a consistência e integridade dos dados antes da análise exploratória.

## 📊 Exemplos de Gráficos e Insights

### ✅ Distribuição Geral do Cancelamento

* **26,5%** dos clientes cancelaram o contrato.

### 📅 Churn por Tipo de Contrato

* Contratos mensais têm a maior taxa de cancelamento (**42,6%**).

### 🧱 Forma de Pagamento

* Clientes que utilizam **electronic check** têm o maior churn (**45,3%**).

### 📃 Correlação com Churn

| Variável        | Correlação com churn |
| --------------- | -------------------- |
| meses\_contrato | **-0.35**            |
| fatura\_total   | **-0.20**            |
| qtd\_servicos   | **-0.07**            |

> "Clientes que permanecem mais tempo, possuem contratos anuais e pagam com cartão automático tendem a cancelar menos."

## ⚖️ Instruções para Execução

### 1. Clone o repositório ou envie os arquivos para o Google Colab

```bash
# via Git (opcional)
git clone https://github.com/seu_usuario/telecom-x-churn.git
```

### 2. Execute o notebook

* Abra o arquivo `TelecomX_BR.ipynb` no Google Colab ou Jupyter Notebook.
* Siga as células sequencialmente:

  * Importação de bibliotecas
  * Leitura e tratamento dos dados
  * Análise descritiva e visualizações
  * Correlações e recomendações

### 3. Requisitos

* Python 3.10+
* pandas, matplotlib, seaborn, numpy

---

Este projeto faz parte de um desafio de análise de dados com foco em **Data Science para Negócios**, utilizando **Python e visualização estratégica** como ferramentas principais.
