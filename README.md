# Implementação de Clusterização na Detecção de Padrões em Roubos e Furtos de Veículos



¹ Aluno do curso em Data Science e Analytics do MBA USP/Esalq  
² Alvarez. Head in R&D and Customer Experience. Av. Ayrton Senna da Silva, 600 – Sala 602 – Gleba Fazenda Palhano; 86050-460. Londrina, Paraná, Brasil  

*Autor correspondente: macrobonillo@gmail.com*

---

## 📖 Resumo

Roubos e furtos de veículos emergiram como desafios de segurança pública em centros urbanos. Neste trabalho, analisamos ocorrências de 2021 no Estado de São Paulo (SSP), incorporando dados socioeconômicos do IBGE e investimentos em segurança da SEFAZ. Utilizamos:

- **Análise Exploratória (EDA):** para entender relações temporais, geográficas e distribuição de delitos.  
- **Correlação de Spearman:** testando associação entre hora do dia e número de ocorrências (ρ ≈ 0,80).  
- **Análise de Correspondência Simples (ANACOR):** avaliando dependência entre dia da semana e períodos do dia, revelando maior incidência na madrugada de fim de semana.  
- **PCA (Análise de Componentes Principais):** reduzindo dimensionalidade para visualização e refinamento do K-Means.  
- **K-Means:** segmentando municípios em quatro clusters, destacando perfis diferenciados de risco e investimento.

Palavras-chave: Segurança pública · Roubos e furtos · Atividade econômica · Análise exploratória · K-Means

---

## 🗂️ Estrutura do Repositório

```text
├── data/                    # Dados brutos (.csv) e pré-processados (dataframes)
│   ├── raw/                 # Arquivos originais baixados do SSP, IBGE e SEFAZ
│   └── processed/           # Bases tratadas para análise
├── notebooks/               # Jupyter Notebooks
│   ├── 01_EDA.ipynb         # EDA e visualizações (histogramas, heatmaps)
│   ├── 02_Stats.ipynb       # Correlação de Spearman e ANACOR
│   └── 03_Clustering.ipynb  # PCA, método do cotovelo e K-Means
├── src/                     # Scripts Python modulares (.py)
├── requirements.txt         # Dependências (pandas, numpy, scikit-learn, scipy, prince, yellowbrick, etc.)
├── LICENSE                  # Licença de uso (ex: MIT)
└── README.md                # Este documento
```

---

## 🚀 Como Executar

1. **Clonar o repositório**:
   ```bash
   git clone https://github.com/SEU_USUARIO/NOME_DO_REPO.git
   cd NOME_DO_REPO
   ```
2. **Criar e ativar venv**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate    # Unix/macOS
   venv\Scripts\activate       # Windows
   ```
3. **Instalar dependências**:
   ```bash
   pip install -r requirements.txt
   ```
4. **Rodar Jupyter Lab**:
   ```bash
   jupyter lab
   ```
   - Execute sequencialmente os notebooks em `notebooks/`.

---

## 🔧 Metodologia (Resumo)

1. **Coleta e Pré-processamento**
2. **Análise Exploratória (EDA)**
3. **Testes Estatísticos**
4. **PCA**
5. **K-Means**
---

## 📊 Principais Resultados
- **Spearman (HORA×OCORRÊNCIAS):** ρ = 0,7965, p = 0,0032 – forte associação.
- **ANACOR:** χ² = 398,48; p < 0,001 – pico de furtos na madrugada de fins de semana.
- **Clusters (K=4):**  
  - Cluster 0: centros urbanos densos.
  - Cluster 1 & 2: média-alta renda, investimento variável.
  - Cluster 3: regiões extensas, menor densidade.

---

## 📚 Referências Selecionadas
- Cohen, J. (1988). *Statistical Power Analysis for the Behavioral Sciences.*
- Greenacre, M. J. (2017). *Correspondence Analysis in Practice.*
- Géron, A. (2021). *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow.*
- Everitt, B. S. et al. (2011). *Cluster Analysis.*

---

## 🤝 Contato
Para dúvidas, sugestões ou colaborações, abra uma issue ou envie e-mail para **macrobonillo@gmail.com**.