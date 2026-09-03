# 📈 Previsão de Séries Temporais: Ações Petrobras (PETR4)

Este projeto de Data Science aplica modelos preditivos para analisar e prever o comportamento histórico e futuro das ações da Petrobras (PETR4). Utilizando dados históricos diários, o estudo compara abordagens estatísticas clássicas e modelos de forecasting para identificar qual técnica se adapta melhor à volatilidade do mercado financeiro.

## 🎯 Objetivo

O principal objetivo é realizar uma análise comparativa de diferentes abordagens de modelagem preditiva. A busca é encontrar o modelo que melhor compreende a volatilidade e as quebras estruturais do mercado, fornecendo as projeções mais precisas para ativos voláteis do setor de energia.

## 🧠 Metodologia e Modelos

O pipeline de análise consiste em extração de dados, Análise Exploratória de Dados (EDA), teste de estacionariedade (ADF), e finalmente o treino e avaliação dos modelos.

Os modelos documentados no notebook são Holt-Winters e Prophet; eles são avaliados em uma janela de teste de 90 dias:

| Modelo | Tipo | Características Principais |
| :--- | :--- | :--- |
| **Holt-Winters** | Estatístico Clássico | Suavização Exponencial Tripla. Focado em capturar tendências e sazonalidade anual explícita (período de 365 dias). |
| **Prophet** | Machine Learning (Facebook/Meta) | Modelo moderno altamente adaptável. Lida excepcionalmente bem com mudanças bruscas de tendência (changepoints), crises e sazonalidade semanal. |

## 🏆 Resultados e Avaliação

A avaliação utilizou as métricas **MAE (Erro Absoluto Médio)**, **RMSE (Raiz do Erro Quadrático Médio)** e **MAPE (Erro Percentual Absoluto Médio)**.

O modelo **Prophet** apresentou o melhor desempenho geral, acompanhando de forma muito mais precisa a curva da ação em relação aos valores reais durante a janela de teste.

- **Erro Médio (MAPE) do Prophet**: ~4,2%
- **Superioridade**: A tecnologia se provou mais robusta e adaptável às oscilações bruscas de ações voláteis (como o setor de petróleo), superando as limitações lineares do Holt-Winters.

## 📁 Estrutura do Repositório

O projeto é apresentado em um único Jupyter Notebook completo, contendo todas as etapas da análise:

- `series_temporais_PETR4.ipynb`: Notebook principal que inclui a extração de dados via `yfinance`, análise exploratória, testes de estacionariedade (ADF), implementação dos modelos (Holt-Winters e Prophet) e visualização comparativa das métricas.

## 🚀 Próximos Passos

Para refinar ainda mais a capacidade preditiva do modelo Prophet, as próximas iterações do projeto focarão em:

1. Integração de **variáveis exógenas**, como a Cotação do Dólar (USD/BRL) e o Preço do Barril de Petróleo (Brent).
2. Ajuste fino dos hiperparâmetros do Prophet para otimizar o tratamento de outliers.

---
*Projeto desenvolvido por Kaique como portfólio de Data Science e Análise de Séries Temporais.*


## Reprodutibilidade e uso responsável

Instale as dependências com `python -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt` e execute o notebook. Os resultados dependem da fonte externa e da data de coleta. Este é um estudo educacional; desempenho histórico não garante retorno futuro e não constitui recomendação financeira.
