Análise de Padrões em Roubos e Furtos de Veículos no Estado de São Paulo
Visão Geral do Projeto
Este projeto implementa técnicas avançadas de análise de dados e machine learning para identificar padrões em ocorrências de roubos e furtos de veículos no Estado de São Paulo. A análise integra dados de segurança pública com variáveis socioeconômicas e demográficas, oferecendo insights valiosos para o direcionamento estratégico de políticas públicas e alocação de recursos de segurança.
📑 Índice

Objetivos
Metodologia e Técnicas Aplicadas

EDA
Testes de Hipóteses
ANACOR
PCA
K-Means


Principais Descobertas

Padrões Temporais
Segmentação
Insights


Tecnologias Utilizadas
Estrutura do Projeto
Como Executar
Fontes
Variáveis Principais
Aplicações Práticas
Referências
Contribuições

🎯 Objetivos

✅ Identificar padrões temporais e geográficos em roubos e furtos de veículos
✅ Segmentar municípios com base em características socioeconômicas e criminais
✅ Fornecer evidências estatísticas para apoiar decisões estratégicas em segurança pública
✅ Demonstrar a eficácia de algoritmos de clustering na análise criminal

🔬 Metodologia e Técnicas Aplicadas
Análise Exploratória de Dados (EDA)

Visualização temporal: Distribuições por hora, dia da semana e período do dia
Análise geográfica: Estudo por sub-regiões do estado
Identificação de padrões: Formulação de hipóteses baseadas em dados
Visualizações avançadas: Heatmaps e gráficos de cascata para variações percentuais

Testes de Hipóteses e Correlação

Correlação de Spearman: Análise da associação entre horário e quantidade de ocorrências
Resultado: ρ = 0,7965 (p-valor = 0,0032) – Forte correlação positiva confirmada estatisticamente

Análise de Correspondência Simples (ANACOR)

Objetivo: Investigação da relação entre dias da semana e períodos do dia
Teste qui-quadrado: χ² = 398,48 (p < 0,001)
Padrão identificado: Maior incidência nas madrugadas de fim de semana

Análise de Componentes Principais (PCA)

Redução dimensional: Preservação de 91,09% da variância
Benefícios: Otimização para visualização e melhoria do desempenho do clustering
Resultado: Facilitação da interpretação dos agrupamentos

Clustering com K-Means

Número ótimo de clusters: K=4 (determinado pelo método do cotovelo)
Amostra: 645 municípios paulistas
Coeficiente de silhueta: 0,80
Análise: Estatísticas descritivas detalhadas para cada cluster

📊 Principais Descobertas
Padrões Temporais
AspectoDescriçãoHorário de pico19h às 21h (50% das ocorrências no período noturno)Dias críticosSextas-feiras (noite) e fins de semana (madrugada)Correlação horáriaAumento progressivo de ocorrências ao longo do dia
Segmentação Municipal (4 Clusters)
ClusterCaracterísticasCluster 0Municípios menores com baixa criminalidade e alta variabilidadeCluster 1Centros urbanos densos com alta atividade econômicaCluster 2Cidades de médio porte com altas taxas de roubo/furtoCluster 3Regiões extensas com densidade populacional moderada
Insights Socioeconômicos

📈 Correlação econômica: PIB per capita elevado associado a maiores taxas de criminalidade
💰 Disparidade de investimentos: Diferenças significativas nos investimentos em segurança entre municípios
🏙️ Densidade populacional: Relação direta entre densidade demográfica e incidência de crimes

🛠️ Tecnologias Utilizadas
Python 3.11.4

pandas - Manipulação e análise de dados
scikit-learn - K-Means, PCA, métricas de avaliação
scipy - Testes estatísticos e correlações
prince - Análise de correspondência (ANACOR)
seaborn e matplotlib - Visualizações
yellowbrick - Método do cotovelo
numpy - Operações numéricas

📁 Estrutura do Projeto
projeto/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── eda.ipynb
│   ├── clustering.ipynb
│   └── analysis.ipynb
├── src/
│   ├── data_processing.py
│   ├── visualization.py
│   └── models.py
├── outputs/
│   ├── figures/
│   └── reports/
└── README.md
🚀 Como Executar

Clone o repositório

bashgit clone https://github.com/seu-usuario/analise-roubos-furtos-sp.git
cd analise-roubos-furtos-sp

Instale as dependências

bashpip install -r requirements.txt

Execute os notebooks

bashjupyter notebook notebooks/
📊 Fontes

Secretaria de Segurança Pública do Estado de São Paulo
IBGE - Dados demográficos e socioeconômicos
SEADE - Fundação Sistema Estadual de Análise de Dados

📋 Variáveis Principais

Temporais: Hora, dia da semana, mês, período do dia
Geográficas: Município, região, coordenadas
Criminais: Tipo de ocorrência, local, circunstâncias
Socioeconômicas: PIB per capita, densidade populacional, IDH

🎯 Aplicações Práticas

Planejamento policial: Alocação otimizada de recursos
Políticas públicas: Direcionamento de investimentos em segurança
Prevenção: Identificação de áreas e horários de risco
Monitoramento: Acompanhamento da eficácia de intervenções

📚 Referências

Hair Jr., J. F., et al. (2019). Multivariate Data Analysis
James, G., et al. (2021). An Introduction to Statistical Learning
Python Software Foundation. (2023). Python Documentation

🤝 Contribuições
Contribuições são bem-vindas! Por favor:

Fork o projeto
Crie uma branch para sua feature (git checkout -b feature/AmazingFeature)
Commit suas mudanças (git commit -m 'Add some AmazingFeature')
Push para a branch (git push origin feature/AmazingFeature)
Abra um Pull Request


Desenvolvido com ❤️ para análise de segurança pública
