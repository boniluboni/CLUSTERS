<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Análise de Padrões em Roubos e Furtos de Veículos SP</title>
  <style>
    body { font-family: Arial, sans-serif; line-height: 1.6; margin: 20px; }
    h1, h2, h3, h4 { color: #2c3e50; }
    nav ul { list-style: none; padding: 0; }
    nav ul li { margin: 5px 0; }
    table { width: 100%; border-collapse: collapse; margin-bottom: 20px; }
    table, th, td { border: 1px solid #ddd; }
    th, td { padding: 8px; text-align: left; }
    th { background-color: #f4f4f4; }
  </style>
</head>
<body>

  <h1>Análise de Padrões em Roubos e Furtos de Veículos no Estado de São Paulo</h1>

  <section id="visao-geral">
    <h2>Visão Geral do Projeto</h2>
    <p>Este projeto implementa técnicas avançadas de análise de dados e machine learning para identificar padrões em ocorrências de roubos e furtos de veículos no Estado de São Paulo. A análise integra dados de segurança pública com variáveis socioeconômicas e demográficas, oferecendo insights valiosos para o direcionamento estratégico de políticas públicas e alocação de recursos de segurança.</p>
  </section>

  <nav>
    <h2>Índice</h2>
    <ul>
      <li><a href="#objetivos">Objetivos</a></li>
      <li><a href="#metodologia">Metodologia e Técnicas Aplicadas</a>
        <ul>
          <li><a href="#eda">Análise Exploratória de Dados (EDA)</a></li>
          <li><a href="#testes-hipoteses">Testes de Hipóteses e Correlação</a></li>
          <li><a href="#anacor">Análise de Correspondência Simples (ANACOR)</a></li>
          <li><a href="#pca">Análise de Componentes Principais (PCA)</a></li>
          <li><a href="#kmeans">Clustering com K-Means</a></li>
        </ul>
      </li>
      <li><a href="#descobertas">Principais Descobertas</a>
        <ul>
          <li><a href="#temporais">Padrões Temporais</a></li>
          <li><a href="#segmentation">Segmentação Municipal</a></li>
          <li><a href="#insights-socioeconomicos">Insights Socioeconômicos</a></li>
        </ul>
      </li>
      <li><a href="#tecnologias">Tecnologias Utilizadas</a></li>
      <li><a href="#estrutura">Estrutura do Projeto</a></li>
      <li><a href="#como-executar">Como Executar</a></li>
      <li><a href="#fontes">Conjunto de Dados e Fontes</a></li>
      <li><a href="#variaveis">Variáveis Principais</a></li>
      <li><a href="#aplicacoes">Aplicações Práticas</a></li>
      <li><a href="#referencias">Referências Principais</a></li>
      <li><a href="#contribuicoes">Contribuições</a></li>
    </ul>
  </nav>

  <section id="objetivos">
    <h2>Objetivos</h2>
    <ul>
      <li>Identificar padrões temporais e geográficos em roubos e furtos de veículos</li>
      <li>Segmentar municípios com base em características socioeconômicas e criminais</li>
      <li>Fornecer evidências estatísticas para apoiar decisões estratégicas em segurança pública</li>
      <li>Demonstrar a eficácia de algoritmos de clustering na análise criminal</li>
    </ul>
  </section>

  <section id="metodologia">
    <h2>Metodologia e Técnicas Aplicadas</h2>

    <h3 id="eda">Análise Exploratória de Dados (EDA)</h3>
    <ul>
      <li>Visualização de distribuições temporais (hora, dia da semana, período do dia)</li>
      <li>Análise geográfica por sub-regiões do estado</li>
      <li>Identificação de padrões e formulação de hipóteses</li>
      <li>Criação de heatmaps e gráficos de cascata para variações percentuais</li>
    </ul>

    <h3 id="testes-hipoteses">Testes de Hipóteses e Correlação</h3>
    <ul>
      <li>Correlação de Spearman: Análise da associação entre horário e quantidade de ocorrências</li>
      <li>Resultado: ρ = 0,7965 (p-valor = 0,0032) – Forte correlação positiva confirmada estatisticamente</li>
    </ul>

    <h3 id="anacor">Análise de Correspondência Simples (ANACOR)</h3>
    <ul>
      <li>Investigação da relação entre dias da semana e períodos do dia</li>
      <li>Teste qui-quadrado: χ² = 398,48 (p &lt; 0,001)</li>
      <li>Identificação de padrões: maior incidência nas madrugadas de fim de semana</li>
    </ul>

    <h3 id="pca">Análise de Componentes Principais (PCA)</h3>
    <ul>
      <li>Redução de dimensionalidade preservando 91,09% da variância</li>
      <li>Otimização para visualização e melhoria do desempenho do clustering</li>
      <li>Facilitação da interpretação dos agrupamentos</li>
    </ul>

    <h3 id="kmeans">Clustering com K-Means</h3>
    <ul>
      <li>Determinação do número ótimo de clusters: método do cotovelo (K=4)</li>
      <li>Segmentação de 645 municípios paulistas</li>
      <li>Avaliação com coeficiente de silhueta: 0,80</li>
      <li>Análise detalhada de cada cluster com estatísticas descritivas</li>
    </ul>
  </section>

  <section id="descobertas">
    <h2>Principais Descobertas</h2>

    <section id="temporais">
      <h3>Padrões Temporais</h3>
      <table>
        <tr><th>Aspecto</th><th>Descrição</th></tr>
        <tr><td>Horário de pico</td><td>19h às 21h (concentração de 50% das ocorrências no período noturno)</td></tr>
        <tr><td>Dias críticos</td><td>Sextas-feiras (noite) e fins de semana (madrugada)</td></tr>
        <tr><td>Correlação horária</td><td>Aumento progressivo de ocorrências ao longo do dia</td></tr>
      </table>
    </section>

    <section id="segmentation">
      <h3>Segmentação Municipal (4 Clusters)</h3>
      <table>
        <tr><th>Cluster</th><th>Características</th></tr>
        <tr><td>Cluster 0</td><td>Municípios menores com baixa criminalidade e alta variabilidade</td></tr>
        <tr><td>Cluster 1</td><td>Centros urbanos densos com alta atividade econômica</td></tr>
        <tr><td>Cluster 2</td><td>Cidades de médio porte com altas taxas de roubo/furto</td></tr>
        <tr><td>Cluster 3</td><td>Regiões extensas com densidade populacional moderada</td></tr>
      </table>
    </section>

    <section id="insights-socioeconomicos">
      <h3>Insights Socioeconômicos</h3>
      <ul>
        <li>Correlação entre PIB per capita elevado e maiores taxas de criminalidade</li>
        <li>Disparidade nos investimentos em segurança entre municípios</li>
        <li>Relação entre densidade demográfica e incidência de crimes</li>
      </ul>
    </section>
  </section>

  <section id="tecnologias">
    <h2>Tecnologias Utilizadas</h2>
    <p><strong>Python 3.11.4</strong></p>
    <ul>
      <li><code>pandas</code> - Manipulação e análise de dados</li>
      <li><code>scikit-learn</code> - K-Means, PCA, métricas de avaliação</li>
      <li><code>scipy</code> - Testes estatísticos e correlações</li>
      <li><code>prince</code> - Análise de correspondência (ANACOR)</li>
      <li><code>seaborn</code> e <code>matplotlib</code> - Visualizações</li>
      <li><code>yellowbrick</code> - Método do cotovelo</li>
      <li><code>numpy</code> - Operações numéricas</li>
    </ul>
  </section>

  <section id="estrutura">
    <h2>Estrutura do Projeto</h2>
    <pre>
analise-roubos-veiculos-sp/
│
├── data/
│   ├── raw/                        # Dados originais (SSP, IBGE, SEFAZ)
│   │   ├── ocorrencias_2021.csv
│   │   ├── dados_ibge.csv
│   │   └── investimentos_sefaz.csv
│   └── processed/                  # Dados processados e integrados
│       └── dataset_final.csv
│
├── notebooks/
│   ├── 01_preprocessing.ipynb      # Limpeza e integração dos dados
│   ├── 02_eda.ipynb               # Análise exploratória completa
│   ├── 03_statistical_tests.ipynb  # Spearman e ANACOR
│   ├── 04_pca_analysis.ipynb      # Redução de dimensionalidade
│   └── 05_clustering.ipynb        # K-Means e análise dos clusters
│
├── src/
│   ├── data_processing.py         # Funções de pré-processamento
│   ├── statistical_analysis.py    # Implementação dos testes
│   ├── clustering.py              # Pipeline do K-Means
│   └── visualization.py           # Funções de visualização
│
├── results/
│   ├── figures/                   # Gráficos e visualizações
│   └── reports/                   # Relatórios detalhados
│
├── requirements.txt               # Dependências do projeto
├── README.md                      # Este arquivo
└── LICENSE                        # MIT License
    </pre>
  </section>

  <section id="como-executar">
    <h2>Como Executar</h2>
    <ol>
      <li>Clone o repositório:
        <pre><code>git clone https://github.com/SEU_USUARIO/analise-roubos-veiculos-sp.git
cd analise-roubos-veiculos-sp</code></pre>
      </li>
      <li>Configure o ambiente virtual:
        <pre><code>python -m venv venv
# Linux/macOS
source venv/bin/activate
# Windows
venv\Scripts\activate</code></pre>
      </li>
      <li>Instale as dependências:
        <pre><code>pip install -r requirements.txt</code></pre>
      </li>
      <li>Execute os notebooks na ordem:
        <pre><code>jupyter lab</code></pre>
      </li>
    </ol>
  </section>

  <section id="fontes">
    <h2>Conjunto de Dados e Fontes</h2>
    <table>
      <tr><th>Fonte</th><th>Descrição</th></tr>
      <tr><td>SSP-SP</td><td>172.000 registros de ocorrências (filtrados para 10.777 após pré-processamento)</td></tr>
      <tr><td>IBGE</td><td>Dados demográficos e socioeconômicos dos 645 municípios</td></tr>
      <tr><td>SEFAZ-SP</td><td>Investimentos em segurança pública por município</td></tr>
    </table>
  </section>

  <section id="variaveis">
    <h2>Variáveis Principais</h2>
    <ul>
      <li><strong>Temporais:</strong> data, hora, dia da semana, período do dia</li>
      <li><strong>Geográficas:</strong> cidade, região, coordenadas</li>
      <li><strong>Socioeconômicas:</strong> população, PIB per capita, renda média</li>
      <li><strong>Segurança:</strong> investimentos, taxa de roubos por 1000 veículos</li>
      <li><strong>Mobilidade:</strong> frota de automóveis, taxa de veículos por pessoa</li>
    </ul>
  </section>

  <section id="aplicacoes">
    <h2>Aplicações Práticas</h2>
    <ul>
      <li>Alocação de recursos - Direcionamento estratégico de efetivo policial</li>
      <li>Políticas públicas - Evidências para tomada de decisão</li>
      <li>Planejamento urbano - Identificação de áreas críticas</li>
      <li>Gestão de segurança - Otimização de investimentos por região</li>
    </ul>
  </section>

  <section id="referencias">
    <h2>Referências Principais</h2>
    <ul>
      <li>Cohen, J. (1988). <em>Statistical Power Analysis for the Behavioral Sciences</em></li>
      <li>Greenacre, M. J. (2017). <em>Correspondence Analysis in Practice</em></li>
      <li>Géron, A. (2021). <em>Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow</em></li>
      <li>Everitt, B. S. et al. (2011). <em>Cluster Analysis</em></li>
    </ul>
  </section>

  <section id="contribuicoes">
    <h2>Contribuições</h2>
    <p>Contribuições são bem-vindas! Por favor, abra uma issue para discutir mudanças propostas ou envie um pull request.</p>
    <p><strong>Contato:</strong> [seu.email@exemplo.com]</p>
  </section>

</body>
</html>
