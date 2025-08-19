# 📊 Análise e Predição de Rotatividade no Mercado de Trabalho Brasileiro (CAGED)

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-green?logo=scikit-learn)
---

## 📄 Visão Geral
Analisei os dados do Cadastro Geral de Empregados e Desempregados (CAGED) de 2023 para:  
- Explorar tendências de empregabilidade no Brasil por **região** e **setor econômico**.  
- Desenvolver um modelo de **Machine Learning** para prever a rotatividade (turnover) de empregos.  

---

## 🛠️ Metodologia
1. **ETL e Pré-processamento**  
   - Enriqueci os dados com *web scraping* (`pandas.read_html`) para integrar UF (IBGE), CNAE e CBO.  
   - Tratei inconsistências e valores nulos para garantir integridade.  

2. **Análise Exploratória (EDA)**  
   - Identifiquei concentração de empregos no Sudeste.  
   - Comércio e Reparação de Veículos foi o setor com maior movimentação.  
   - Correlacionei variáveis para seleção de features relevantes.  

---

## 🔍 Visualizações

| Distribuição por Região | Atividade Econômica |
|-------------------------|----------------------|
| ![Distribuição por Região](assets/Gráfico%20de%20Pizza%20da%20Distribuição%20por%20Região.PNG) | ![Atividade Econômica](assets/Gráfico%20de%20Barras%20por%20Atividade%20Econômica.PNG) |

| Matriz de Correlação | Importância das Features |
|----------------------|--------------------------|
| ![Matriz de Correlação](assets/Matriz%20de%20Correlação.PNG) | ![Importância das Features do Modelo de ML](assets/Gráfico%20de%20Importância%20das%20Features%20do%20Modelo%20de%20ML.PNG) |

---

## 🤖 Modelo de Machine Learning
- **Variável alvo:** Desligamento (sim/não).  
- **Algoritmo:** `RandomForestClassifier`.  
- **Métricas:** Acurácia, Precisão, Recall e F1-Score.  

📌 **Principais resultados:**  
- Ocupação e Salário foram as variáveis mais relevantes.  
- Profissões como *Auxiliar de escritório* e *Vendedor de comércio varejista* tiveram maior peso na previsão de desligamentos.  

---

## 📝 Conclusão
O projeto mostrou como dados do CAGED podem apoiar a compreensão do mercado de trabalho e prever padrões de desligamento.  
Além dos insights, foi uma oportunidade de aplicar **ETL, EDA e modelagem preditiva com Machine Learning**.  

---

## ⚙️ Tecnologias
- `Python`  
- `Pandas`  
- `Scikit-learn`  
- `Matplotlib`  
- `Seaborn`  
