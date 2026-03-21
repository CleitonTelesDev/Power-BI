# 💄 Aura Beauty Co. - Business Intelligence Dashboard

![Capa do Projeto](https://via.placeholder.com/1000x300?text=Aura+Beauty+Co.+Data+Driven+Project)

## 📝 Sobre o Projeto
A **Aura Beauty Co.** é uma empresa do setor de cosméticos que atua no mercado desde 2022. Historicamente, a empresa operava sem um acompanhamento analítico rigoroso de seus dados. 

Este projeto marca a transição da companhia para uma **Cultura Data Driven**, utilizando o Power BI para transformar dados brutos de vendas, produtos e logística em decisões estratégicas fundamentadas.

---

## 🛠️ Etapas de Desenvolvimento

### 1. ETL e Tratamento de Dados (Power Query)
Os dados brutos foram processados para garantir a integridade das análises:
* **Limpeza:** Remoção de duplicatas e tratamento de valores nulos em colunas críticas como `Preço` e `id_produto`.
* **Padronização:** Uniformização de categorias e subcategorias de produtos.
* **Cálculos Customizados:** Criação da métrica *Ship-to-Door* (tempo entre o envio e a entrega final) e tratamento de datas para séries temporais.

### 2. Modelagem de Dados
Utilizei a arquitetura **Star Schema (Esquema Estrela)** para garantir performance e escalabilidade:
* **Tabela Fato:** `Pedidos` (contendo transações, quantidades e descontos).
* **Tabelas Dimensão:** `Produtos`, `Marcas`, `Calendário` e `Geolocalização`.
* **Relacionamentos:** Estabelecidos através de chaves primárias e estrangeiras (ex: `id_produto`, `Cod_marca`).

---

## 📊 Visualizações e Análises (Dashboards)

O relatório foi dividido em pilares estratégicos para atender diferentes áreas da empresa:

### 💰 Performance Comercial
* **Faturamento por Produto:** Gráfico de barras clusterizado com linhas de referência para identificar os produtos "Best Sellers".
* **Análise de Marcas:** Gráfico dinâmico que permite alternar a visão entre **Origem (Nacional/Internacional)**, **Marca** e **Categoria** via parâmetros.
* **Acompanhamento de Metas:** Gráfico de medidor (Gauge) comparando o faturamento realizado contra a meta mensal estabelecida.

### 📈 Tendências e Previsões
* **Série Temporal:** Gráfico de linhas com análise de tendência e **Forecasting (Previsão)** para os próximos meses, além de detecção automática de anomalias no faturamento.
* **Elasticidade de Preço:** Gráfico de dispersão analisando a correlação entre variação de preço e volume de faturamento.

### 🚚 Logística e Expansão
* **Mapa de Calor:** Visualização geográfica do faturamento por cidade para identificar regiões com potencial de expansão.
* **Eficiência Logística:** KPI de *Ship-to-Doors* monitorando o tempo médio de entrega anual (Métrica: "Baixo é bom").

---

## 🚀 Tecnologias Utilizadas
* **Power BI:** Visualização e dashboard.
* **DAX (Data Analysis Expressions):** Criação de medidas complexas e KPIs.
* **Power Query (M):** Extração e transformação de dados.
* **Excel/CSV:** Fontes de dados iniciais.

---

## 💡 Insights Gerados
* Identificação de quais marcas internacionais possuem maior margem de contribuição.
* Detecção de gargalos logísticos em cidades específicas através do KPI de entrega.
* Validação de que reduções pontuais de preço impactam positivamente o faturamento total (elasticidade detectada no gráfico de dispersão).

---

## 📬 Contato
Desenvolvido por **Cleiton Teles**<br>
[LinkedIn] www.linkedin.com/in/cleitonteles
* [Portfólio de Projetos](https://github.com/CleitonTelesDev?tab=repositories)
