# 📈 Previsão de Cotações de Ações - Petrobras (PETR4.SA)

Este projeto realiza uma análise de séries temporais das ações da Petrobras (PETR4) com o objetivo de prever o comportamento futuro dos preços na bolsa de valores. A análise inclui exploração dos dados históricos (5 anos) e uma comparação direta entre modelos clássicos e modernos de predição.

## 🎯 Objetivo
Comparar diferentes abordagens de modelagem preditiva para descobrir qual entende melhor a volatilidade do mercado financeiro e fornece as projeções mais precisas.

## 🧠 Modelos Avaliados
Durante a análise, dois modelos principais foram testados e comparados:

1. **Holt-Winters**: Modelo estatístico clássico focado em sazonalidade e tendências passadas.
2. **Prophet (Facebook/Meta)**: Modelo moderno que lida excepcionalmente bem com mudanças bruscas de tendência, crises e feriados.

## 🏆 Resultados
O modelo **Prophet** apresentou o melhor desempenho geral em relação ao mercado real durante a janela de teste de 90 dias, acompanhando muito melhor a curva da ação.

* **Erro Médio do Prophet**: ~4,2%
* A tecnologia se provou superior e mais adaptável às oscilações bruscas de ações voláteis como as de petróleo.

## 📁 Estrutura do Repositório

- `series_temporais_PETR4.ipynb`: Notebook completo com todo o processo de extração de dados, análise exploratória, treino e avaliação dos modelos.

## 🚀 Próximos Passos
- Integração de variáveis exógenas como **Cotação do Dólar** e **Preço do Barril de Petróleo (Brent)** para refinar ainda mais a capacidade preditiva do modelo Prophet.

---
*Projeto desenvolvido por Kaique como portfólio de Data Science e Análise de Séries Temporais.*
