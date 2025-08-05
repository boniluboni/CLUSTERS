Análise de Padrões em Roubos e Furtos de Veículos no Estado de São Paulo
Visão Geral do Projeto
Este projeto implementa técnicas avançadas de análise de dados e machine learning para identificar padrões em ocorrências de roubos e furtos de veículos no Estado de São Paulo. A análise integra dados de segurança pública com variáveis socioeconômicas e demográficas, oferecendo insights valiosos para o direcionamento estratégico de políticas públicas e alocação de recursos de segurança.
Objetivos

Identificar padrões temporais e geográficos em roubos e furtos de veículos
Segmentar municípios com base em características socioeconômicas e criminais
Fornecer evidências estatísticas para apoiar decisões estratégicas em segurança pública
Demonstrar a eficácia de algoritmos de clustering na análise criminal

Metodologia e Técnicas Aplicadas
1. Análise Exploratória de Dados (EDA)

Visualização de distribuições temporais (hora, dia da semana, período do dia)
Análise geográfica por sub-regiões do estado
Identificação de padrões e formulação de hipóteses
Criação de heatmaps e gráficos de cascata para variações percentuais

2. Testes de Hipóteses e Correlação
Correlação de Spearman: Análise da associação entre horário e quantidade de ocorrências

Resultado: ρ = 0,7965 (p-valor = 0,0032)
Forte correlação positiva confirmada estatisticamente

3. Análise de Correspondência Simples (ANACOR)

Investigação da relação entre dias da semana e períodos do dia
Teste qui-quadrado: χ² = 398,48 (p < 0,001)
Identificação de padrões: maior incidência nas madrugadas de fim de semana

4. Análise de Componentes Principais (PCA)

Redução de dimensionalidade preservando 91,09% da variância
Otimização para visualização e melhoria do desempenho do clustering
Facilitação da interpretação dos agrupamentos

5. Clustering com K-Means

Determinação do número ótimo de clusters: método do cotovelo (K=4)
Segmentação de 645 municípios paulistas
Avaliação com coeficiente de silhueta: 0,80
Análise detalhada de cada cluster com estatísticas descritivas

Principais Descobertas
Padrões Temporais

Horário de pico: 19h às 21h (concentração de 50% das ocorrências no período noturno)
Dias críticos: Sextas-feiras (noite) e fins de semana (madrugada)
Correlação horária: Aumento progressivo de ocorrências ao longo do dia

Segmentação Municipal (4 Clusters)

Cluster 0: Municípios menores com baixa criminalidade e alta variabilidade
Cluster 1: Centros urbanos densos com alta atividade econômica
Cluster 2: Cidades de médio porte com altas taxas de roubo/furto
Cluster 3: Regiões extensas com densidade populacional moderada

Insights Socioeconômicos

Correlação entre PIB per capita elevado e maiores taxas de criminalidade
Disparidade nos investimentos em segurança entre municípios
Relação entre densidade demográfica e incidência de crimes

Tecnologias Utilizadas
Python 3.11.4
Bibliotecas principais:

pandas: Manipulação e análise de dados
scikit-learn: K-Means, PCA, métricas de avaliação
scipy: Testes estatísticos e correlações
prince: Análise de correspondência (ANACOR)
seaborn e matplotlib: Visualizações
yellowbrick: Método do cotovelo
numpy: Operações numéricas


├── data/
│   ├── raw/                    # Dados originais (SSP, IBGE, SEFAZ)
│   │   ├── ocorrencias_2021.csv
│   │   ├── dados_ibge.csv
│   │   └── investimentos_sefaz.csv
│   └── processed/              # Dados processados e integrados
│       └── dataset_final.csv
│
├── notebooks/
│   ├── 01_preprocessing.ipynb  # Limpeza e integração dos dados
│   ├── 02_eda.ipynb           # Análise exploratória completa
│   ├── 03_statistical_tests.ipynb  # Spearman e ANACOR
│   ├── 04_pca_analysis.ipynb  # Redução de dimensionalidade
│   └── 05_clustering.ipynb    # K-Means e análise dos clusters
│
├── src/
│   ├── data_processing.py     # Funções de pré-processamento
│   ├── statistical_analysis.py # Implementação dos testes
│   ├── clustering.py          # Pipeline do K-Means
│   └── visualization.py       # Funções de visualização
│
├── results/
│   ├── figures/               # Gráficos e visualizações
│   └── reports/               # Relatórios detalhados
│
├── requirements.txt           # Dependências do projeto
├── README.md                  # Este arquivo
└── LICENSE                    # MIT License
