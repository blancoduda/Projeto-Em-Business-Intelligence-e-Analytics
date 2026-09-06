# Business Intelligence e Analytics aplicados ao desempenho escolar

Projeto acadêmico da disciplina **Projeto em Business Intelligence e Analytics**, da PUCRS Online.

O projeto analisa fatores escolares associados às taxas de aprovação das escolas públicas de Ensino Fundamental de Porto Alegre entre 2018 e 2023, utilizando dados públicos do Inep, técnicas de Business Intelligence e modelos de Machine Learning.

---

## Problema de pesquisa

**Quais fatores escolares estão associados às taxas de aprovação das escolas públicas de Ensino Fundamental de Porto Alegre entre 2018 e 2023, e em que medida esses fatores permitem estimar o indicador de aprovação?**

---

## Recorte

- **Localidade:** Porto Alegre — RS
- **Rede:** pública
- **Dependência administrativa:** Federal, Estadual e Municipal
- **Etapa:** Ensino Fundamental
- **Período:** 2018–2023
- **Granularidade:** escola/ano
- **Indicador principal:** taxa de aprovação

---

## Fontes de dados

Foram utilizados dados públicos disponibilizados pelo **Inep**:

- Censo Escolar da Educação Básica
- Taxas de Rendimento Escolar
- Média de Alunos por Turma

Os arquivos brutos são mantidos apenas localmente e não são versionados no Git.

Os arquivos processados utilizados diretamente pelo Power BI são disponibilizados em:

```text
data/processed/bi/
```

---

## Preparação dos dados

O processo de preparação contemplou:

1. coleta e compreensão das fontes;
2. mapeamento das diferenças de layout entre os anos;
3. auditoria de qualidade;
4. tratamento de valores ausentes;
5. limpeza e padronização;
6. integração das bases pela chave `ano + codigo_escola`;
7. construção da base analítica;
8. geração das tabelas utilizadas no Power BI.

Valores representados por `--` nas fontes originais foram tratados como **ausentes**, e não como zero.

O **Censo Escolar** foi utilizado como universo principal da integração.

---

## Base analítica

A base analítica consolidada possui:

- **1.621 registros**
- **51 variáveis**
- **276 escolas**
- **Período:** 2018–2023
- **Granularidade:** escola/ano
- **Chave:** `ano + codigo_escola`

Não foram identificadas duplicidades na chave após o tratamento.

Foram encontrados **1.571 registros com taxa de aprovação válida** para análise e modelagem.

---

## Metodologia

O projeto segue a metodologia **CRISP-DM**:

1. compreensão do problema;
2. compreensão dos dados;
3. preparação dos dados;
4. modelagem;
5. avaliação;
6. apresentação dos resultados.

Além da análise exploratória e da construção dos indicadores de BI, foram avaliados três algoritmos de regressão:

- Regressão Linear
- Decision Tree Regressor
- Random Forest Regressor

Também foi utilizado um **baseline baseado na média histórica da taxa de aprovação**.

### Divisão temporal

- **Treinamento:** 2018–2022
- **Teste:** 2023

A divisão temporal foi utilizada para avaliar os modelos em um período posterior aos dados utilizados no treinamento.

### Métricas

- MAE — Mean Absolute Error
- RMSE — Root Mean Squared Error
- R² — Coeficiente de Determinação

---

## Resultados da modelagem

| Modelo | MAE | RMSE | R² |
|---|---:|---:|---:|
| Baseline | 5,79 | 7,44 | -0,0005 |
| Regressão Linear | 5,62 | 7,16 | 0,0736 |
| Árvore de Decisão | 5,53 | 7,06 | 0,0975 |
| **Random Forest** | **5,27** | **6,82** | **0,1577** |

O **Random Forest apresentou o melhor desempenho**, superando o baseline e os demais modelos nas três métricas avaliadas.

Apesar da melhora, o R² de **0,1577** indica que as características disponíveis explicam apenas parte da variação observada na taxa de aprovação em 2023.

### Importância das variáveis

A análise de importância do Random Forest mostrou forte influência do contexto temporal:

| Variável | Importância |
|---|---:|
| Período | 75,95% |
| Média de alunos por turma | 7,10% |
| Quantidade de docentes | 6,95% |
| Quantidade de matrículas | 4,63% |
| Quantidade de turmas | 2,81% |

Os indicadores individuais de infraestrutura apresentaram menor contribuição relativa para a capacidade preditiva do modelo.

A importância das variáveis representa contribuição para a previsão e **não deve ser interpretada como relação causal**.

---

## Dashboard Power BI

O dashboard foi desenvolvido no **Power BI Desktop** e está disponível em:

```text
powerbi/desempenho_escolar_porto_alegre.pbix
```

O relatório contém as páginas:

- **Capa**
- **Visão Geral**
- **Infraestrutura Escolar**
- **Infraestrutura x Desempenho**
- **Perfil Escolar**
- **Evolução Temporal**
- **Modelagem e Analytics**

Entre os principais indicadores apresentados estão:

- taxa média de aprovação;
- taxa média de reprovação;
- taxa média de abandono;
- média de alunos por turma;
- matrículas médias;
- quantidade de escolas;
- disponibilidade de recursos de infraestrutura;
- diferenças de aprovação entre escolas com e sem determinados recursos;
- evolução temporal dos indicadores;
- comparação entre modelos preditivos;
- importância das variáveis;
- taxa de aprovação real x prevista em 2023.

---

## Estrutura do repositório

```text
Projeto-Em-Business-Intelligence-e-Analytics/
│
├── data/
│   ├── raw/
│   └── processed/
│       └── bi/
│           ├── dim_escola.csv
│           ├── dim_tempo.csv
│           ├── fato_desempenho.csv
│           ├── importancia_modelo.csv
│           ├── previsoes_2023.csv
│           └── resultados_modelos.csv
│
├── docs/
│   ├── projeto-fase-1.pdf
│   └── variaveis_consolidadas.md
│
├── notebooks/
│   ├── 01_compreensao_preparacao_dados.ipynb
│   ├── 02_limpeza_padronizacao_dados.ipynb
│   ├── 03_integracao_bases.ipynb
│   ├── 04_analise_exploratoria.ipynb
│   ├── 05_kpis.ipynb
│   ├── 06_modelagem_bi.ipynb
│   └── 07_modelagem_preditiva.ipynb
│
├── powerbi/
│   └── desempenho_escolar_porto_alegre.pbix
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

## Status

- [x] Coleta dos dados
- [x] Compreensão e mapeamento das fontes
- [x] Auditoria de qualidade
- [x] Limpeza e padronização
- [x] Integração das bases
- [x] Construção da base analítica
- [x] Análise exploratória
- [x] Definição de KPIs
- [x] Modelagem de dados para BI
- [x] Dashboard Power BI
- [x] Modelagem preditiva
- [x] Avaliação dos modelos
- [x] Relatório final
- [x] Apresentação final

---

## Tecnologias

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Plotly
- Power BI
- Git
- GitHub
- Jupyter Notebook

---

## Limitações

Os resultados devem ser interpretados considerando:

- dados ausentes em parte dos indicadores;
- mudanças de estrutura e nomenclatura entre os anos;
- diferenças de cobertura entre as fontes;
- alterações relevantes observadas durante os anos de 2020 e 2021;
- número reduzido de escolas federais no recorte;
- ausência de variáveis socioeconômicas e contextuais que podem contribuir para explicar o desempenho escolar.

As associações e importâncias identificadas pelos modelos **não devem ser interpretadas automaticamente como relações de causa e efeito**.

---

## Licença

O código e os notebooks deste projeto estão sob licença **MIT**.

Os dados pertencem às respectivas fontes oficiais e não são abrangidos automaticamente pela licença do repositório.
