# 💄 Aura Beauty Co. - Análise de Performance de Vendas  

### 📊 Transformando dados em decisões estratégicas no setor de cosméticos  
![Marca](https://github.com/CleitonTelesDev/Power-BI/blob/main/images/branding/Marca%20Aura.png?raw=true)

---

## 🧠 Sobre o Projeto  

A **Aura Beauty Co.** é uma empresa do segmento de beleza que, apesar de sua atuação desde 2022, baseava suas decisões em processos manuais e intuição.

Este projeto tem como objetivo implementar uma abordagem **Data Driven**, transformando dados históricos em **insights estratégicos** para apoiar decisões relacionadas a:

- 📈 Faturamento  
- 🚚 Logística (Ship-to-Door)  
- 💰 Precificação  

---

## 📊 Dashboard  

### 🔍 Visão Geral

![Dashboard Vendas](https://github.com/CleitonTelesDev/Power-BI/blob/main/images/dashboards/Vendas.png?raw=true)

![Dashboard Produtos](https://github.com/CleitonTelesDev/Power-BI/blob/main/images/dashboards/Produtos.png?raw=true)

---

## 📊 Principais Insights  

- 📈 O faturamento está concentrado em um grupo reduzido de produtos, indicando efeito Pareto  
- 💰 Reduções de preço aumentam volume de vendas, mas nem sempre resultam em maior receita total  
- 🌎 Determinadas regiões concentram maior volume de vendas, sugerindo oportunidades de expansão estratégica  
- 🚚 O tempo de entrega (Ship-to-Door) impacta diretamente a eficiência operacional  
- 📉 Produtos com baixo desempenho indicam oportunidades de revisão de portfólio  

---

## ⚙️ Pipeline de Dados  

### Tratamento de Dados (ETL)  

Utilização do **Power Query** para limpeza e transformação dos dados, garantindo consistência e qualidade para análise.

Principais etapas:
- Padronização de colunas (`Preço`, `Quantidade`)  
- Tratamento de valores inconsistentes  
- Preparação de dados geográficos (Latitude / Longitude)  

---

### 🖼️ Modelagem de Dados  

O modelo foi estruturado seguindo o padrão Star Schema, garantindo alta performance e organização para análises analíticas.

![Modelo](https://github.com/CleitonTelesDev/Power-BI/blob/main/images/modelo/modelo_dados.png?raw=true)

- 🧾 **Fato:** `fPedidos`  
- 📊 **Dimensões:** `dProdutosFinais`, `dMarcas`, `dMetaMensal`, `dCalendario`  

---

### Inteligência de Dados (DAX)  

Principais métricas desenvolvidas:

| Medida | Lógica Aplicada | Objetivo |
| :--- | :--- | :--- |
| **Faturamento** | `SUMX(fPedidos, [quantidade] * RELATED(dProdutosFinais[Preço]))` | Receita total |
| **Faturamento Médio** | `AVERAGEX(fPedidos, [quantidade] * RELATED(dProdutosFinais[Preço]))` | Ticket médio |
| **Meta Máxima** | `IF([Faturamento] < [SomaMetas], [SomaMetas] * 1.2, [Faturamento])` | Ajuste dinâmico |
| **Meta S2Door** | `8` | Tempo ideal de entrega |
| **Soma Metas** | `AVERAGE(dMetaMensal[Meta])` | Comparação mensal |

---

## 📁 Estrutura do Projeto  
📦 Power-BI  
┣ 📂 data  
┣ 📂 powerbi  
┣ 📂 images  
┃ ┣ 📂 branding  
┃ ┣ 📂 dashboards  
┃ ┗ 📂 modelo  
┣ README.md  

---

## 🚀 Tecnologias Utilizadas  

- Power BI  
- Power Query (M)  
- DAX  
- GitHub  

---

## ▶️ Como Reproduzir  

1. Baixe o arquivo `.pbix` disponível na pasta `powerbi/`  
2. Abra no Power BI Desktop  
3. Explore os dashboards e interações  

---

## 💼 Sobre Mim  

Sou um profissional de dados focado em transformar dados em **insights estratégicos que geram valor de negócio**.

📫 Contato:

- LinkedIn: https://www.linkedin.com/in/cleitonteles  
- Email: juantrick@gmail.com  

---

## ⭐ Competências Demonstradas  

Este projeto demonstra habilidades em:

- Modelagem de dados (Star Schema)  
- Construção de dashboards no Power BI  
- Criação de métricas com DAX  
- Análise orientada a negócio  
- Comunicação de insights  

---
