# 💄 Aura Beauty Co. - Dashboard de Performance de Vendas
> **Objetivo:** Implementação de Cultura Data Driven para o setor de cosméticos.

![Marca.png](https://github.com/CleitonTelesDev/Power-BI/blob/main/Aura%20Beauty%20Co/Dados/imagens_power_bi_visualizando_analisando_dados/Marca%20Aura.png?raw=true)

---

## 📝 Sobre o Projeto
A **Aura Beauty Co.** é uma empresa do ramo da beleza que atua desde 2022. Apesar da presença no mercado, a tomada de decisão era baseada em processos manuais e intuição. 

Este projeto marca a transição da empresa para uma **Cultura Data Driven**, transformando dados históricos em inteligência de mercado para otimizar faturamento, logística (Ship-to-Door) e precificação.

---

## 🛠️ Estrutura e Desenvolvimento

### 1. Tratamento de Dados (ETL)
Utilizei o Power Query para a limpeza e transformação dos dados brutos, garantindo que colunas como `Preço`, `Quantidade` e as coordenadas geográficas (`Latitude`/`Longitude`) estivessem prontas para análise, sem inconsistências.

### 2. Modelagem de Dados
O modelo foi estruturado seguindo o padrão **Star Schema (Esquema Estrela)** para máxima performance:
* **Fato:** `fPedidos` (Transações, Quantidades, Descontos e Localização).
* **Dimensões:** `dProdutosFinais`, `dMarcas`, `dMetaMensal` e `dCalendario`.

### 3. Inteligência de Dados (DAX)
Abaixo estão as principais métricas desenvolvidas para sustentar os indicadores de negócio:

| Medida | Lógica Aplicada | Objetivo |
| :--- | :--- | :--- |
| **Faturamento** | `SUMX(fPedidos, [quantidade] * RELATED(dProdutosFinais[Preço]))` | Cálculo preciso de receita total cruzando tabelas. |
| **Faturamento Médio** | `AVERAGEX(fPedidos, [quantidade] * RELATED(dProdutosFinais[Preço]))` | Identificar o ticket médio por pedido. |
| **Meta Máxima** | `IF([Faturamento] < [SomaMetas], [SomaMetas] * 1.2, [Faturamento])` | Ajuste dinâmico do eixo do gráfico de medidor. |
| **Meta S2Door** | `8` | Target fixo de 8 dias para entrega (Ship-to-Door). |
| **Soma Metas** | `AVERAGE(dMetaMensal[Meta])` | Base de comparação para performance mensal. |

---

## 📊 Visualizações e Insights

O dashboard foi construído para responder perguntas fundamentais do negócio:

* **Faturamento por Produto:** Gráfico de barras clusterizado com **linhas de referência** para identificar produtos de alta performance.
* **Análise de Marcas:** Uso de **parâmetros de campo** para comparar categorias por Origem, Marca e Categoria no mesmo gráfico.
* **Séries Temporais:** Análise de faturamento com linhas de tendência, **Forecasting (Previsão)** e detecção de **Anomalias**.
* **Logística Geográfica:** Gráfico de mapa utilizando as colunas de cidade e bolhas de faturamento para visualização regional.
* **KPI Ship-to-Door:** Monitoramento do tempo "do envio à porta", focado na eficiência logística (onde "baixo é bom").
* **Gráfico de Medidor:** Visualização clara do faturamento vs. meta, com ajuste dinâmico de eixo.
* **Análise de Dispersão:** Estudo da correlação entre **Faturamento e Preço**, validando se a redução de preços aumenta o volume total de vendas.

---

## 🚀 Tecnologias Utilizadas
* **Power BI** (Visualização e DAX)
* **Power Query** (M Language)
* **GitHub** (Documentação e Portfólio)

---

## 📬 Contato
Desenvolvido por **Cleiton Teles**<br>
LinkedIn: www.linkedin.com/in/cleitonteles<br>
E-mail: juantrick@gmail.com
* [Portfólio de Projetos](https://github.com/CleitonTelesDev?tab=repositories)
