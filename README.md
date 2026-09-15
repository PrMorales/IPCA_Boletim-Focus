## Auditoria de Expectativas: IPCA vs. Boletim Focus

Este projeto de Análise Exploratória de Dados (EDA) investiga a precisão das projeções macroeconômicas do mercado financeiro brasileiro. Através do uso de APIs públicas do Banco Central, o pipeline confronta a inflação real (IPCA) com as expectativas do Boletim Focus, revelando padrões de comportamento, inércia preditiva e as falhas de previsão decorrentes de choques reais na economia.

---

### 🎯 O Desafio Analítico

O mercado financeiro precifica o futuro do país com base nas medianas do Boletim Focus. Mas qual é a real taxa de acerto? O objetivo deste projeto é construir um fluxo de dados para calcular o Erro Médio Absoluto (MAE) das previsões de 1 mês de antecedência e expor visualmente como o mercado reage a crises, distorções tributárias e anos eleitorais.

---

### 📊 Principais Descobertas (Insights)

* **Os Extremos:** O mercado financeiro falha sistematicamente em prever vales e picos. O maior erro direcional ocorreu em 2022, evidenciando a incapacidade dos modelos em precificar o "efeito rebote" de intervenções artificiais via canetadas de impostos.
* **A Maldição do 1º Trimestre:** A análise de dispersão térmica (Heatmap) comprova que o Brasil sofre de inércia inflacionária nos primeiros meses do ano. Ainda assim, projeções frequentemente subestimam a força dessa sazonalidade.
* **Comportamento Conservador:** O confronto direto entre as previsões de 2025 e 2026 revela uma estabilidade irrealista. Na ausência de pânico, o mercado adota um comportamento conservador, replicando médias históricas (cerca de 0.30% ao mês).
* **Eleições Precificadas:** Surpreendentemente, as projeções para outubro e novembro de 2026 não embutem anomalias ou prêmios de risco inflacionário severo, indicando uma aposta clara na manutenção da máquina institucional, independente do cenário político.

---

### 🛠️ Tecnologias e Arquitetura de Dados

* **Linguagem:** Python
* **Processamento:** Pandas (Merge, Pivot Tables, Rolling Windows, Tratamento de Datas)
* **Visualização:** Plotly Graph Objects (Dashboards Interativos) e Seaborn (Heatmap)
* **Consumo de Dados (APIs REST):** SGS (Séries Temporais) e API Olinda OData (BCB)

> **Nota Metodológica:** O código foi construído para ser 100% reprodutível. Basta executar o Notebook para que os dados sejam atualizados em tempo real diretamente dos servidores do Banco Central.
