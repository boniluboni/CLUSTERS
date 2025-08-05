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
<table>
<tr>
<td><strong>Horário de pico</strong></td>
<td>19h às 21h (concentração de 50% das ocorrências no período noturno)</td>
</tr>
<tr>
<td><strong>Dias críticos</strong></td>
<td>Sextas-feiras (noite) e fins de semana (madrugada)</td>
</tr>
<tr>
<td><strong>Correlação horária</strong></td>
<td>Aumento progressivo de ocorrências ao longo do dia</td>
</tr>
</table>
Segmentação Municipal (4 Clusters)
<table>
<tr>
<th>Cluster</th>
<th>Características</th>
</tr>
<tr>
<td><strong>Cluster 0</strong></td>
<td>Municípios menores com baixa criminalidade e alta variabilidade</td>
</tr>
<tr>
<td><strong>Cluster 1</strong></td>
<td>Centros urbanos densos com alta atividade econômica</td>
</tr>
<tr>
<td><strong>Cluster 2</strong></td>
<td>Cidades de médio porte com altas taxas de roubo/furto</td>
</tr>
<tr>
<td><strong>Cluster 3</strong></td>
<td>Regiões extensas com densidade populacional moderada</td>
</tr>
</table>
Insights Socioeconômicos

Correlação entre PIB per capita elevado e maiores taxas de criminalidade
Disparidade nos investimentos em segurança entre municípios
Relação entre densidade demográfica e incidência de crimes

Tecnologias Utilizadas
Python 3.11.4
Bibliotecas principais:

pandas - Manipulação e análise de dados
scikit-learn - K-Means, PCA, métricas de avaliação
scipy - Testes estatísticos e correlações
prince - Análise de correspondência (ANACOR)
seaborn e matplotlib - Visualizações
yellowbrick - Método do cotovelo
numpy - Operações numéricas

Estrutura do Projeto
<pre>
<strong>analise-roubos-veiculos-sp/</strong>
│
├── <strong>data/</strong>
│   ├── <strong>raw/</strong>                        <em># Dados originais (SSP, IBGE, SEFAZ)</em>
│   │   ├── ocorrencias_2021.csv
│   │   ├── dados_ibge.csv
│   │   └── investimentos_sefaz.csv
│   └── <strong>processed/</strong>                  <em># Dados processados e integrados</em>
│       └── dataset_final.csv
│
├── <strong>notebooks/</strong>
│   ├── 01_preprocessing.ipynb      <em># Limpeza e integração dos dados</em>
│   ├── 02_eda.ipynb               <em># Análise exploratória completa</em>
│   ├── 03_statistical_tests.ipynb  <em># Spearman e ANACOR</em>
│   ├── 04_pca_analysis.ipynb      <em># Redução de dimensionalidade</em>
│   └── 05_clustering.ipynb        <em># K-Means e análise dos clusters</em>
│
├── <strong>src/</strong>
│   ├── data_processing.py         <em># Funções de pré-processamento</em>
│   ├── statistical_analysis.py    <em># Implementação dos testes</em>
│   ├── clustering.py              <em># Pipeline do K-Means</em>
│   └── visualization.py           <em># Funções de visualização</em>
│
├── <strong>results/</strong>
│   ├── <strong>figures/</strong>                   <em># Gráficos e visualizações</em>
│   └── <strong>reports/</strong>                   <em># Relatórios detalhados</em>
│
├── requirements.txt               <em># Dependências do projeto</em>
├── README.md                      <em># Este arquivo</em>
└── LICENSE                        <em># MIT License</em>
</pre>
Como Executar
1. Clone o repositório
bashgit clone https://github.com/SEU_USUARIO/analise-roubos-veiculos-sp.git
cd analise-roubos-veiculos-sp
2. Configure o ambiente virtual
bashpython -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
3. Instale as dependências
bashpip install -r requirements.txt
4. Execute os notebooks na ordem
bashjupyter lab
Conjunto de Dados
Fontes
<table>
<tr>
<th>Fonte</th>
<th>Descrição</th>
</tr>
<tr>
<td><strong>SSP-SP</strong></td>
<td>172.000 registros de ocorrências (filtrados para 10.777 após pré-processamento)</td>
</tr>
<tr>
<td><strong>IBGE</strong></td>
<td>Dados demográficos e socioeconômicos dos 645 municípios</td>
</tr>
<tr>
<td><strong>SEFAZ-SP</strong></td>
<td>Investimentos em segurança pública por município</td>
</tr>
</table>
Variáveis Principais

Temporais: data, hora, dia da semana, período do dia
Geográficas: cidade, região, coordenadas
Socioeconômicas: população, PIB per capita, renda média
Segurança: investimentos, taxa de roubos por 1000 veículos
Mobilidade: frota de automóveis, taxa de veículos por pessoa

Aplicações Práticas

Alocação de recursos - Direcionamento estratégico de efetivo policial
Políticas públicas - Evidências para tomada de decisão
Planejamento urbano - Identificação de áreas críticas
Gestão de segurança - Otimização de investimentos por região

Referências Principais

Cohen, J. (1988). Statistical Power Analysis for the Behavioral Sciences
Greenacre, M. J. (2017). Correspondence Analysis in Practice
Géron, A. (2021). Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow
Everitt, B. S. et al. (2011). Cluster Analysis

Contribuições
Contribuições são bem-vindas! Por favor, abra uma issue para discutir mudanças propostas ou envie um pull request.
Contato
