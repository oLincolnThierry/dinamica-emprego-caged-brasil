# Análise e Predição de Rotatividade no Mercado de Trabalho Brasileiro (CAGED)

### 📄 Visão Geral

Este projeto é um estudo de caso aprofundado sobre a dinâmica do mercado de trabalho no Brasil. Utilizando dados públicos do Cadastro Geral de Empregados e Desempregados (CAGED) de 2023, o projeto tem como objetivos:

* Explorar as tendências de empregabilidade e a distribuição demográfica e setorial.
* Propor um modelo de Machine Learning para a previsão de rotatividade (turnover) de empregos.

---

### 🛠️ Metodologia e Pipeline de Análise

#### 1. Aquisição e Pré-processamento de Dados (ETL)
* **Enriquecimento de Dados via Web Scraping:** Utilizei `pandas.read_html` para coletar e integrar tabelas de classificações de UF (IBGE), CNAE (classificação de atividade econômica) e CBO (Classificação Brasileira de Ocupações), enriquecendo o dataset principal.
* Tratamento de dados inconsistentes e valores nulos para garantir a integridade do conjunto de dados.

#### 2. Análise Exploratória de Dados (EDA)

O decréscimo do PIB em contraste com a eclosão da pandemia da COVID-19 evidenciou problemas estruturais na economia brasileira. A reconfiguração da oferta e demanda de mão de obra tem sido motivo de análise.

A análise exploratória nos permitiu identificar as principais dinâmicas do mercado de trabalho:

* **Distribuição de Empregos por Região:** A análise visual mostra a concentração da movimentação de empregos no país, com a região Sudeste liderando em volume.
  
    
    ![Distribuição por Região](assets/Gráfico%20de%20Pizza%20da%20Distribuição%20por%20Região.PNG)


    
* **Movimentação por Setor Econômico:** O setor de Comércio; Reparação de Veículos Automotores e Motocicletas (Seção G) foi o que apresentou o maior volume de movimentação no período.
    
![Atividade Econômica](assets/Gráfico%20de%20Barras%20por%20Atividade%20Econômica.PNG)

#### Análise de Correlação das Variáveis Quantitativas
A matriz de correlação nos ajudou a identificar o grau de relacionamento linear entre as variáveis. Observamos correlações elevadas entre pares como `regiao` e `uf`, o que é esperado. Outras correlações significativas, como entre `saldomovimentacao` e `tipomovimentacao`, sugerem que o tipo de movimentação é um fator determinante para o saldo de empregos. A análise dessas correlações foi crucial para guiar a seleção de features para os modelos preditivos.

_Coloque a imagem do heatmap aqui:_

![Movimentação por Setor Econômico](assets/Matriz%20de%20Correlação.PNG)

---

### 🤖 Proposta de Machine Learning

Com base na análise exploratória, um modelo de **classificação** foi proposto para prever a probabilidade de um trabalhador ser desligado (turnover).

* **Variável Alvo:** Desligamento (sim/não).
* **Modelo Utilizado:** `RandomForestClassifier`.
* **Métricas de Avaliação:** Acurácia, Precisão, Recall e F1-Score.

#### Resultados do Modelo

A análise de importância de features demonstrou que o modelo está aprendendo padrões lógicos, com os seguintes resultados:

* **Ocupação e Salário:** A Ocupação e o Valor de Salário Fixo foram as features mais importantes para a previsão de desligamento.
* **Ocupações Específicas:** O modelo destacou que cargos com alta rotatividade, como "Auxiliar de escritório" e "Vendedor de comércio varejista", são os mais relevantes para a previsão.

_Coloque a imagem do gráfico de importância de features aqui:_

![Importância das Features do Modelo de ML](assets/Gráfico%20de%20Importância%20das%20Features%20do%20Modelo%20de%20ML.PNG)

---

### 📝 Conclusão

A pandemia de COVID-19 trouxe desafios sem precedentes para a economia brasileira, evidenciando fragilidades e acelerando transformações. O impacto foi significativo, e a reconfiguração da oferta e demanda de mão de obra destacou a importância da adaptabilidade e da inovação. Este projeto serve como um ponto de partida para análises mais aprofundadas, mostrando como dados do mercado de trabalho podem ser utilizados para entender tendências e fazer previsões.

---

### ⚙️ Tecnologias Utilizadas

* `Python`
* `Pandas`
* `Scikit-learn`
* `Matplotlib`
* `Seaborn`
