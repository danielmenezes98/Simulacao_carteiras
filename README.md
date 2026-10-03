# 📊 Simulação de Carteiras

Projeto desenvolvido em Python para simular a evolução de uma carteira de investimentos e comparar seu desempenho com o índice Ibovespa (IBOV).

A análise utiliza dados históricos de diferentes ativos, para acompanhar a evolução do patrimônio ao longo do período de 2016 a 2026.

---

## 🎯 Sobre o projeto

O projeto consiste na criação de uma carteira fictícia de investimentos, utilizando um aporte inicial distribuído entre diferentes ativos.

A partir dos preços históricos, é calculada a quantidade de papéis adquirida em cada ativo e, posteriormente, é acompanhada a evolução do patrimônio da carteira ao longo do tempo.

Ao final, o desempenho da carteira é comparado ao Ibovespa por meio da rentabilidade acumulada.

### Para simplificar a simulação:

- Foi realizado apenas um aporte em cada ativo;
- Todos os aportes foram considerados na mesma data;
- Foi utilizado um valor total de **R$ 20.000**;
- A quantidade de papéis foi calculada com base no primeiro preço disponível no período analisado.

---

## 💰 Carteira utilizada

A carteira simulada foi composta pelos seguintes ativos:

| Ativo | Valor destinado |
| :--- | ---: |
| PETR4 | R$ 2.000 |
| ITUB3 | R$ 2.300 |
| ABEV3 | R$ 5.200 |
| EGIE3 | R$ 4.800 |
| SMAL11 | R$ 1.300 |
| VALE3 | R$ 1.400 |
| COCA34 | R$ 1.000 |
| AAPL34 | R$ 2.000 |
| **Total** | **R$ 20.000** |

---

## 📅 Período analisado

**01/01/2016 a 01/01/2026**

Os dados históricos dos ativos foram obtidos utilizando a biblioteca **yFinance**.

---

## 🛠️ Tecnologias utilizadas

- **Python** — linguagem utilizada no desenvolvimento da análise;
- **Pandas** — manipulação e organização dos dados;
- **NumPy** — operações numéricas;
- **Matplotlib** — visualização dos resultados;
- **yFinance** — obtenção dos dados históricos do mercado financeiro;
- **Jupyter Notebook** — desenvolvimento e documentação da análise.

---

## 🔎 Etapas da análise

### 1. Configuração da carteira

Foi criada uma estrutura contendo os ativos selecionados e o valor destinado a cada um deles.

### 2. Obtenção dos dados históricos

Os preços históricos dos ativos foram obtidos por meio do `yFinance`, considerando o período definido para a análise.

Para acompanhar a evolução dos investimentos, foram utilizados os preços de fechamento.

### 3. Simulação da carteira

A partir do primeiro preço disponível de cada ativo, foi calculada a quantidade de papéis que poderia ser adquirida com o valor destinado ao investimento.

Em seguida, foi calculado o valor de cada posição ao longo do período.

A soma dessas posições permitiu acompanhar a evolução do patrimônio total da carteira.

### 4. Comparação com o Ibovespa

Também foram obtidos os dados históricos do índice Ibovespa (`^BVSP`).

Os dados do IBOV e da carteira foram reunidos em um único DataFrame para possibilitar a comparação entre as duas séries.

### 5. Normalização dos dados

Como o Ibovespa e os ativos possuem escalas de valores diferentes, uma comparação direta entre seus preços não seria adequada.

Para solucionar esse problema, os dados foram normalizados a partir do primeiro valor da série.

Dessa forma, todas as séries passam a ter o valor inicial igual a **1**, permitindo analisar a evolução da rentabilidade acumulada ao longo do período.

---

## 📈 Visualização dos resultados

Ao final da análise, são gerados gráficos para visualizar a evolução da carteira e comparar seu desempenho com o Ibovespa.

A normalização permite observar as duas séries em uma escala comum, facilitando a análise da rentabilidade acumulada.

---

## ▶️ Como executar

### 1. Clone o repositório

```bash
git clone URL_DO_REPOSITORIO
