# Air Quality in São Paulo 🌎🌿

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/) 
[![Project Status](https://img.shields.io/badge/status-completed-brightgreen.svg)]()

Projeto de análise da qualidade do ar em São Paulo, focando na variação dos níveis de dióxido de nitrogênio (NO₂) ao longo do dia em diferentes regiões.

## 📊 Dataset
- **Fonte:** [Kaggle - SP Air Quality](https://www.kaggle.com/datasets/amandalk/sp-air-quality)
- **Período:** 5 de agosto de 2013 a 9 de setembro de 2020
- **Coleta:** Medições horárias de poluentes.

---

## 🎯 Objetivos
- Analisar padrões diários na concentração de NO₂.
- Identificar causas e horários de pico de poluição.
- Comparar diferenças regionais de concentração de poluentes.

---

## 🛠️ Tecnologias e Bibliotecas
- **Python 3.8+**
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Datetime](https://docs.python.org/3/library/datetime.html)

---

## 🔍 Análise Exploratória
![print(air_quality head(3))](https://github.com/user-attachments/assets/2dbab26f-f3b5-4bae-9667-96342e623b99)
- Dataset com 11 colunas: Datetime, Station e poluentes (Benzene, CO, PM10, PM2.5, NO₂, O3, SO2, Toluene, TRS).
- Tratamento de valores ausentes de NO₂ pela imputação por subgrupos da mediana de cada estação de coleta.
- Remoção de outliers usando intervalo interquartil (IQR) de cada estação de coleta.

---

## 🧹 Manipulação dos Dados
- Extração da **hora** (`Hour`) da coluna `Datetime`.
- Criação da coluna **Region** agrupando estações em:
  - Capital
  - Região Metropolitana
  - Interior
  - Vale do Paraíba
  - Litoral
- Visualização usando gráficos de linha segmentados por região.

---

## 📈 Resultados
![NO2_(µgm³)_per_hour_in_São_Paulo](https://github.com/user-attachments/assets/4005b7be-285f-4c19-abd5-db70926bcb7c)
- **Picos de NO₂:**
  - 6h–10h (manhã)
  - 17h–20h (tarde/noite)
- **Menor concentração:**
  - 1h–5h (madrugada)
  - 11h–15h (início da tarde)
- **Regiões mais críticas:** Capital, Região Metropolitana e Litoral.

---

## 📝 Conclusão
  
A análise sugere que o tráfego de veículos é um dos principais responsáveis pelos picos de concentração de NO₂ em São Paulo, principalmente nos horários de pico.
  
Para melhorar a qualidade do ar, seria essencial:
- Incentivar o transporte público e sustentável,
- Estimular o uso de veículos elétricos e GNV,
- Implementar políticas de controle rigoroso sobre emissões industriais.
