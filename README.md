# 📊 Simulação de Carteiras

Projeto desenvolvido em Python para realizar uma simulação de carteira de investimentos e comparar sua evolução com o índice Ibovespa (IBOV).

O projeto utiliza dados históricos do mercado financeiro para acompanhar a evolução de uma carteira fictícia de R$ 20.000 ao longo do período analisado.

## 🎯 Objetivo

O objetivo do projeto é simular o comportamento de uma carteira de investimentos composta por diferentes ativos e comparar sua evolução com o Ibovespa.

Para simplificar a análise:

- Foi considerado apenas um aporte em cada ativo;
- Todos os aportes foram realizados no mesmo dia;
- O valor total utilizado na simulação foi de R$ 20.000;
- Foram utilizados dados históricos dos ativos para acompanhar a evolução do patrimônio.

## 🛠️ Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- yFinance
- Jupyter Notebook

## 💰 Carteira utilizada

A carteira simulada possui os seguintes ativos:

| Ativo | Valor investido |
|---|---:|
| PETR4 | R$ 2.000 |
| ITUB3 | R$ 2.300 |
| ABEV3 | R$ 5.200 |
| EGIE3 | R$ 4.800 |
| SMAL11 | R$ 1.300 |
| VALE3 | R$ 1.400 |
| COCA34 | R$ 1.000 |
| AAPL34 | R$ 2.000 |
| **Total** | **R$ 20.000** |

## 📅 Período analisado

Os dados utilizados na simulação compreendem o período de:

**01/01/2016 a 01/01/2026**

Os dados históricos dos ativos foram obtidos utilizando a biblioteca `yfinance`.

## 📈 Metodologia

### 1. Importação das bibliotecas

Foram utilizadas bibliotecas Python para manipulação, análise e visualização dos dados.

### 2. Configuração da carteira

Foi criada uma estrutura contendo os ativos e os respectivos valores destinados a cada investimento.

### 3. Importação dos dados

Os preços históricos dos ativos foram obtidos através da biblioteca `yfinance`.

Para a análise, foi utilizado o preço de fechamento diário.

### 4. Simulação da carteira

A partir do primeiro preço disponível no período, foi calculada a quantidade de papéis que poderia ser adquirida com o valor destinado a cada ativo.

Em seguida, foi calculado o valor de cada posição ao longo do tempo.

A soma das posições permitiu acompanhar a evolução do patrimônio total da carteira.

### 5. Comparação com o Ibovespa

Além da carteira, foram obtidos dados históricos do índice Ibovespa (`^BVSP`).

Os dados da carteira e do IBOV foram então reunidos em um único DataFrame para permitir a comparação.

### 6. Normalização dos dados

Como os ativos e o Ibovespa possuem escalas diferentes, uma comparação direta poderia gerar uma interpretação distorcida.

Para solucionar esse problema, os dados foram normalizados a partir do primeiro valor da série.

Dessa forma, todas as séries começam em **1**, permitindo comparar a evolução e a rentabilidade acumulada ao longo do período.

## 📊 Resultado

Ao final da análise, são gerados gráficos para visualizar:

- A evolução do patrimônio da carteira;
- A evolução do Ibovespa;
- A comparação entre a carteira e o IBOV após a normalização dos dados.

## ▶️ Como executar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/danielmenezes98/Simula-o-de-Carteiras.git
