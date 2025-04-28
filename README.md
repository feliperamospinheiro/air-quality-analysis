# Air Quality in São Paulo 🌎🌿

[![Versão Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/) 
[![Status do Projeto](https://img.shields.io/badge/status-concluído-brightgreen.svg)]()

Análise da qualidade do ar em São Paulo, focando na variação dos níveis de dióxido de nitrogênio (NO₂) ao longo do dia em diferentes regiões da cidade e do estado.

---

## 📖 Sobre

Este projeto nasceu da necessidade de compreender como a poluição atmosférica se comporta em São Paulo — uma das maiores metrópoles do mundo.  
Seu principal objetivo é identificar padrões de concentração de NO₂, entender suas causas e sugerir ações para melhorar a qualidade do ar.

### 🎯 Objetivos
- Identificar momentos críticos de poluição.
- Apoiar políticas públicas de mobilidade e meio ambiente.
- Incentivar práticas sustentáveis em transporte e indústria.

### 🎯 Uso Pretendido
- Base para estudos acadêmicos e ambientais.
- Apoio à tomada de decisão para projetos de melhoria da qualidade do ar.
- Exercício de desenvolvimento de habilidades em análise e visualização de dados.

---

## 💡 Motivação

São Paulo enfrenta grandes desafios relacionados à poluição do ar, que impactam diretamente a saúde da população e a qualidade de vida urbana.  
Compreender os padrões de emissão pode orientar medidas eficazes de mitigação.

---

## 🌟 Origem do Projeto

O projeto surgiu a partir da exploração de bases públicas de dados ambientais e do desejo de aplicar conceitos de ciência de dados para resolver problemas reais que afetam o cotidiano da população.

---

## 📊 Dataset

![print(air_quality head(3))](https://github.com/user-attachments/assets/1469c983-08b6-4f11-94ac-0a4e8049c172)

- **Fonte:** [Kaggle - SP Air Quality](https://www.kaggle.com/datasets/amandalk/sp-air-quality)
- **Período:** De 5 de agosto de 2013 a 9 de setembro de 2020
- **Características:**
  - Medições horárias de poluentes: Benzene, CO, PM10, PM2.5, NO₂, O₃, SO₂, Toluene e TRS.
  - 11 colunas, incluindo informações de data/hora (`Datetime`) e estação de coleta (`Station`).

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- [Pandas](https://pandas.pydata.org/) — manipulação de dados
- [Matplotlib](https://matplotlib.org/) — visualização básica
- [Seaborn](https://seaborn.pydata.org/) — visualização estatística
- [Datetime](https://docs.python.org/3/library/datetime.html) — manipulação de datas e horas

---

## ⚙️ Descrição do Processo

### 📌 Limpeza dos Dados
- Imputação de valores ausentes de NO₂ com a mediana por estação de coleta.
- Remoção de outliers utilizando o intervalo interquartil (IQR) de cada estação de coleta.

### 📌 Manipulação dos Dados
- Extração da **hora** (`Hour`) da coluna `Datetime`.
- Criação da coluna **Region**, agrupando estações em:
  - Capital
  - Região Metropolitana
  - Interior
  - Vale do Paraíba
  - Litoral

### 📌 Visualização dos Dados
- Gráficos de linha para observar tendências horárias segmentadas por região.

---

## 📈 Resultados

![NO2_(µgm³)_per_hour_in_São_Paulo](https://github.com/user-attachments/assets/4005b7be-285f-4c19-abd5-db70926bcb7c)

**Padrões Identificados:**
- **Picos de NO₂:** 6h–10h (manhã) e 17h–20h (final da tarde e noite).
- **Menores níveis:** 1h–5h (madrugada) e 11h–15h (início da tarde).
- **Regiões mais críticas:** Capital, Região Metropolitana e Litoral.

---

## 🚧 Limitações

- A base de dados abrange apenas algumas regiões específicas.
- A análise focou exclusivamente no poluente NO₂, sem considerar interações entre outros poluentes.
- Fatores meteorológicos (como vento e chuva) não foram incorporados à análise.

---

## 🧗 Desafios Encontrados

- Tratamento de grande volume de dados ausentes.
- Definição adequada de limites para remoção de outliers.
- Agrupamento lógico das estações para análises regionais consistentes.

---

## 📝 Conclusão

A análise revelou que a concentração de NO₂ em São Paulo tende a acompanhar o fluxo de veículos nos horários de pico, variando de acordo com a região analisada.  
Esses resultados reforçam a importância de iniciativas que promovam alternativas de mobilidade mais sustentáveis e práticas urbanas que reduzam a emissão de poluentes.

Embora este estudo tenha focado especificamente no dióxido de nitrogênio, ele oferece insights iniciais que podem servir de base para análises futuras mais abrangentes, incluindo outros poluentes e fatores climáticos.  
A expectativa é que, com o apoio de dados e políticas bem direcionadas, seja possível construir cidades cada vez mais saudáveis e sustentáveis.

---

## 🙌 Créditos

- **Desenvolvimento e Análise:** [Felipe Ramos Pinheiro](https://github.com/feliperamospinheiro)
- **Fonte de Dados:** [Amanda LK (Kaggle)](https://www.kaggle.com/datasets/amandalk/sp-air-quality)
- **Inspiração:** Estudos acadêmicos em meio ambiente e sustentabilidade urbana.
