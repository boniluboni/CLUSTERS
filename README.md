# Análise de Padrões em Roubos e Furtos de Veículos no Estado de São Paulo

<div id="visao-geral">
  <h2>Visão Geral do Projeto</h2>
  <p>Este projeto implementa técnicas avançadas de análise de dados e machine learning para identificar padrões em ocorrências de roubos e furtos de veículos no Estado de São Paulo. A análise integra dados de segurança pública com variáveis socioeconômicas e demográficas, oferecendo insights valiosos para o direcionamento estratégico de políticas públicas e alocação de recursos de segurança.</p>
</div>

<h2>Índice</h2>
<ul>
  <li><a href="#objetivos">Objetivos</a></li>
  <li><a href="#metodologia">Metodologia e Técnicas Aplicadas</a>
    <ul>
      <li><a href="#eda">EDA</a></li>
      <li><a href="#testes-hipoteses">Testes de Hipóteses</a></li>
      <li><a href="#anacor">ANACOR</a></li>
      <li><a href="#pca">PCA</a></li>
      <li><a href="#kmeans">K-Means</a></li>
    </ul>
  </li>
  <li><a href="#descobertas">Principais Descobertas</a>
    <ul>
      <li><a href="#temporais">Padrões Temporais</a></li>
      <li><a href="#segmentation">Segmentação</a></li>
      <li><a href="#insights-socioeconomicos">Insights</a></li>
    </ul>
  </li>
  <li><a href="#tecnologias">Tecnologias Utilizadas</a></li>
  <li><a href="#estrutura">Estrutura do Projeto</a></li>
  <li><a href="#como-executar">Como Executar</a></li>
  <li><a href="#fontes">Fontes</a></li>
  <li><a href="#variaveis">Variáveis Principais</a></li>
  <li><a href="#aplicacoes">Aplicações Práticas</a></li>
  <li><a href="#referencias">Referências</a></li>
  <li><a href="#contribuicoes">Contribuições</a></li>
</ul>

<div id="objetivos">
  <h2>Objetivos</h2>
  <ul>
    <li>Identificar padrões temporais e geográficos em roubos e furtos de veículos</li>
    <li>Segmentar municípios com base em características socioeconômicas e criminais</li>
    <li>Fornecer evidências estatísticas para apoiar decisões estratégicas em segurança pública</li>
    <li>Demonstrar a eficácia de algoritmos de clustering na análise criminal</li>
  </ul>
</div>

<div id="metodologia">
  <h2>Metodologia e Técnicas Aplicadas</h2>

  <div id="eda">
    <h3>Análise Exploratória de Dados (EDA)</h3>
    <ul>
      <li>Visualização de distribuições temporais (hora, dia da semana, período do dia)</li>
      <li>Análise geográfica por sub-regiões do estado</li>
      <li>Identificação de padrões e formulação de hipóteses</li>
      <li>Criação de heatmaps e gráficos de cascata para variações percentuais</li>
    </ul>
  </div>

  <div id="testes-hipoteses">
    <h3>Testes de Hipóteses e Correlação</h3>
    <ul>
      <li>Correlação de Spearman: Análise da associação entre horário e quantidade de ocorrências</li>
      <li>Resultado: ρ = 0,7965 (p-valor = 0,0032) – Forte correlação positiva confirmada estatisticamente</li>
    </ul>
  </div>

  <div id="anacor">
    <h3>Análise de Correspondência Simples (ANACOR)</h3>
    <ul>
      <li>Investigação da relação entre dias da semana e períodos do dia</li>
      <li>Teste qui-quadrado: χ² = 398,48 (p &lt; 0,001)</li>
      <li>Identificação de padrões: maior incidência nas madrugadas de fim de semana</li>
    </ul>
  </div>

  <div id="pca">
    <h3>Análise de Componentes Principais (PCA)</h3>
    <ul>
      <li>Redução de dimensionalidade preservando 91,09% da variância</li>
      <li>Otimização para visualização e melhoria do desempenho do clustering</li>
      <li>Facilitação da interpretação dos agrupamentos</li>
    </ul>
  </div>

  <div id="kmeans">
    <h3>Clustering com K-Means</h3>
    <ul>
      <li>Determinação do número ótimo de clusters: método do cotovelo (K=4)</li>
      <li>Segmentação de 645 municípios paulistas</li>
      <li>Avaliação com coeficiente de silhueta: 0,80</li>
      <li>Análise detalhada de cada cluster com estatísticas descritivas</li>
    </ul>
  </div>
</div>

<div id="descobertas">
  <h2>Principais Descobertas</h2>

  <div id="temporais">
    <h3>Padrões Temporais</h3>
    <table>
      <tr><th>Aspecto</th><th>Descrição</th></tr>
      <tr><td>Horário de pico</td><td>19h às 21h (concentração de 50% das ocorrências no período noturno)</td></tr>
      <tr><td>Dias críticos</td><td>Sextas-feiras (noite) e fins de semana (madrugada)</td></tr>
      <tr><td>Correlação horária</td><td>Aumento progressivo de ocorrências ao longo do dia</td></tr>
    </table>
  </div>

  <div id="segmentation">
    <h3>Segmentação Municipal (4 Clusters)</h3>
    <table>
      <tr><th>Cluster</th><th>Características</th></tr>
      <tr><td>Cluster 0</td><td>Municípios menores com baixa criminalidade e alta variabilidade</td></tr>
      <tr><td>Cluster 1</td><td>Centros urbanos densos com alta atividade econômica</td></tr>
      <tr><td>Cluster 2</td><td>Cidades de médio porte com altas taxas de roubo/furto</td></tr>
      <tr><td>Cluster 3</td><td>Regiões extensas com densidade populacional moderada</td></tr>
    </table>
  </div>

  <div id="insights-socioeconomicos">
    <h3>Insights Socioeconômicos</h3>
    <ul>
      <li>Correlação entre PIB per capita elevado e maiores taxas de criminalidade</li>
      <li>Disparidade nos investimentos em segurança entre municípios</li>
      <li>Relação entre densidade demográfica e incidência de crimes</li>
    </ul>
  </div>
</div>

<div id="tecnologias">
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
</div>

<div id="estrutura">
  <h2>Estrutura do Projeto</h2>
  <pre>
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
  </pre>
</div>

<div id="como-executar">
  <h2>Como Executar</h2>
  <ol>
    <li><strong>Clone o repositório</strong></li>
    <pre><code>git clone https://github.com/seu-usuario/analise-roubos-furtos-sp.git
cd analise-roubos-furtos-sp</code></pre>
    
    <li><strong>Instale as dependências</strong></li>
    <pre><code>pip install -r requirements.txt</code></pre>
    
    <li><strong>Execute os notebooks</strong></li>
    <pre><code>jupyter notebook notebooks/</code></pre>
  </ol>
</div>

<div id="fontes">
  <h2>Fontes</h2>
  <ul>
    <li>Secretaria de Segurança Pública do Estado de São Paulo</li>
    <li>IBGE - Dados demográficos e socioeconômicos</li>
    <li>SEADE - Fundação Sistema Estadual de Análise de Dados</li>
  </ul>
</div>

<div id="variaveis">
  <h2>Variáveis Principais</h2>
  <ul>
    <li><strong>Temporais:</strong> Hora, dia da semana, mês, período do dia</li>
    <li><strong>Geográficas:</strong> Município, região, coordenadas</li>
    <li><strong>Criminais:</strong> Tipo de ocorrência, local, circunstâncias</li>
    <li><strong>Socioeconômicas:</strong> PIB per capita, densidade populacional, IDH</li>
  </ul>
</div>

<div id="aplicacoes">
  <h2>Aplicações Práticas</h2>
  <ul>
    <li><strong>Planejamento policial:</strong> Alocação otimizada de recursos</li>
    <li><strong>Políticas públicas:</strong> Direcionamento de investimentos em segurança</li>
    <li><strong>Prevenção:</strong> Identificação de áreas e horários de risco</li>
    <li><strong>Monitoramento:</strong> Acompanhamento da eficácia de intervenções</li>
  </ul>
</div>

<div id="referencias">
  <h2>Referências</h2>
  <ul>
    <li>Hair Jr., J. F., et al. (2019). <em>Multivariate Data Analysis</em></li>
    <li>James, G., et al. (2021). <em>An Introduction to Statistical Learning</em></li>
    <li>Python Software Foundation. (2023). <em>Python Documentation</em></li>
  </ul>
</div>

<div id="contribuicoes">
  <h2>Contribuições</h2>
  <p>Contribuições são bem-vindas! Por favor:</p>
  <ol>
    <li>Fork o projeto</li>
    <li>Crie uma branch para sua feature (<code>git checkout -b feature/AmazingFeature</code>)</li>
    <li>Commit suas mudanças (<code>git commit -m 'Add some AmazingFeature'</code>)</li>
    <li>Push para a branch (<code>git push origin feature/AmazingFeature</code>)</li>
    <li>Abra um Pull Request</li>
  </ol>
</div>

---
<p align="center"><strong>Desenvolvido com ❤️ para análise de segurança pública</strong></p>
