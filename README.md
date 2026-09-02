# Business Intelligence e Analytics aplicados ao desempenho escolar

Projeto acadêmico da disciplina **Projeto em Business Intelligence e Analytics**, da PUCRS Online.

O objetivo é analisar fatores escolares associados às taxas de aprovação das escolas públicas de Ensino Fundamental de Porto Alegre entre 2018 e 2023, utilizando dados públicos do Inep.

## Problema de pesquisa

**Quais fatores escolares estão associados às taxas de aprovação das escolas públicas de Ensino Fundamental de Porto Alegre entre 2018 e 2023, e em que medida esses fatores permitem estimar o indicador de aprovação?**

## Recorte

- **Localidade:** Porto Alegre — RS
- **Rede:** pública
- **Dependência administrativa:** Federal, Estadual e Municipal
- **Etapa:** Ensino Fundamental
- **Período:** 2018–2023
- **Granularidade:** escola/ano
- **Indicador principal:** taxa de aprovação

## Fontes de dados

Dados públicos do **Inep**:

- Censo Escolar da Educação Básica
- Taxas de Rendimento Escolar
- Média de Alunos por Turma

Os arquivos brutos e processados não são versionados no Git.

## Preparação dos dados

O processo inclui:

1. coleta e compreensão das fontes;
2. mapeamento das diferenças de layout entre os anos;
3. auditoria de qualidade;
4. limpeza e padronização;
5. integração pela chave `ano + codigo_escola`.

Valores `--` são tratados como ausentes, e não como zero.

## Base analítica

A integração utiliza o Censo Escolar como universo principal.

- **1.621 registros**
- **51 variáveis**
- **Período:** 2018–2023
- **Granularidade:** escola/ano
- **Chave:** `ano + codigo_escola`

Não foram identificadas duplicidades na chave após o tratamento.

## Metodologia

O projeto segue a metodologia **CRISP-DM**:

1. compreensão do problema;
2. compreensão dos dados;
3. preparação dos dados;
4. modelagem;
5. avaliação;
6. apresentação dos resultados.

Na etapa preditiva serão avaliados:

- Regressão Linear
- Decision Tree Regressor
- Random Forest Regressor

Métricas previstas:

- MAE
- RMSE
- R²

Treinamento: **2018–2022**  
Teste: **2023**

## Estrutura do repositório

```text
Projeto-Em-Business-Intelligence-e-Analytics/
├── data/
│   ├── raw/
│   └── processed/
├── docs/
├── notebooks/
│   ├── 01_compreensao_preparacao_dados.ipynb
│   ├── 02_limpeza_padronizacao_dados.ipynb
│   └── 03_integracao_bases.ipynb
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Status

- [x] Coleta
- [x] Compreensão e mapeamento
- [x] Auditoria de qualidade
- [x] Limpeza e padronização
- [x] Integração das bases
- [ ] Análise exploratória
- [ ] Indicadores e Power BI
- [ ] Modelagem preditiva
- [ ] Avaliação
- [ ] Relatório e apresentação

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

## Limitações

Os resultados devem ser interpretados considerando dados ausentes, mudanças de estrutura entre anos, diferenças de cobertura entre as fontes e os efeitos específicos do período de 2020 e 2021.

As associações encontradas não devem ser interpretadas automaticamente como relações de causa e efeito.

## Licença

O código e os notebooks deste projeto estão sob licença MIT.

Os dados pertencem às respectivas fontes oficiais e não são abrangidos automaticamente pela licença do repositório.
