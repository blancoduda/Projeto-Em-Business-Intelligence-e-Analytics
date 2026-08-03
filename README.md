# Business Intelligence e Analytics aplicados ao desempenho escolar

Projeto acadêmico desenvolvido na disciplina de **Projeto em Business Intelligence e Analytics**, da PUCRS Online.

A proposta consiste no desenvolvimento de uma solução analítica para identificar fatores escolares associados às taxas de aprovação das escolas públicas de ensino fundamental de Porto Alegre.

O projeto utiliza dados educacionais públicos, técnicas de análise exploratória, visualização de dados e modelos preditivos para transformar informações dispersas em indicadores úteis para análise e apoio à tomada de decisão.

---

## Visão geral

A educação pública brasileira disponibiliza uma quantidade significativa de dados sobre escolas, matrículas, infraestrutura, rendimento e avaliações educacionais.

Entretanto, essas informações são publicadas em diferentes arquivos, estruturas e períodos, dificultando sua utilização direta por gestores, pesquisadores e demais interessados.

Este projeto propõe a integração dessas fontes em uma base analítica única, com granularidade por escola e ano, permitindo:

- acompanhar a evolução dos indicadores educacionais;
- comparar escolas e redes administrativas;
- analisar características de infraestrutura;
- identificar fatores associados à taxa de aprovação;
- construir dashboards interativos;
- avaliar modelos preditivos para estimar a taxa de aprovação.

---

## Problema de pesquisa

Quais fatores escolares estão associados às taxas de aprovação das escolas públicas de ensino fundamental de Porto Alegre entre 2018 e 2023, e em que medida esses fatores permitem estimar o indicador de aprovação?

---

## Objetivo geral

Desenvolver uma solução de Business Intelligence e Analytics para analisar fatores escolares associados às taxas de aprovação das escolas públicas de ensino fundamental de Porto Alegre.

---

## Objetivos específicos

- coletar dados educacionais públicos referentes ao período de 2018 a 2023;
- selecionar as escolas públicas de ensino fundamental de Porto Alegre;
- avaliar a qualidade e a compatibilidade das bases utilizadas;
- tratar valores ausentes, duplicidades e inconsistências;
- padronizar nomes, códigos e tipos de dados;
- integrar as bases pelo código da escola e pelo ano de referência;
- construir uma base analítica com granularidade por escola e ano;
- desenvolver indicadores educacionais e escolares;
- analisar a evolução das taxas de aprovação;
- comparar escolas das redes municipal e estadual;
- identificar fatores associados ao desempenho escolar;
- desenvolver dashboards no Power BI;
- treinar e avaliar modelos de regressão;
- documentar o processo, as limitações e os resultados encontrados.

---

## Recorte da pesquisa

O projeto considera:

- **Localidade:** Porto Alegre, Rio Grande do Sul;
- **Rede de ensino:** escolas públicas;
- **Dependência administrativa:** municipal e estadual;
- **Etapa de ensino:** ensino fundamental;
- **Período analisado:** 2018 a 2023;
- **Unidade de análise:** escola e ano;
- **Indicador principal:** taxa de aprovação.

---

## Fontes de dados

As principais fontes previstas são bases públicas disponibilizadas pelo Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira — Inep.

### Fontes principais

- Censo Escolar da Educação Básica;
- Taxas de Rendimento Escolar;
- Média de Alunos por Turma.

### Fontes complementares

- Índice de Desenvolvimento da Educação Básica — Ideb;
- Sistema de Avaliação da Educação Básica — Saeb.

As fontes complementares serão utilizadas conforme sua disponibilidade e compatibilidade com a granularidade adotada no projeto.

---

## Variáveis previstas

### Variável de resposta

- taxa de aprovação.

### Variáveis explicativas

Entre as variáveis que poderão ser consideradas estão:

- infraestrutura escolar;
- disponibilidade de internet;
- existência de biblioteca ou sala de leitura;
- disponibilidade de laboratório;
- equipamentos de informática;
- condições de acessibilidade;
- serviços básicos;
- quantidade de matrículas;
- quantidade de turmas;
- média de alunos por turma;
- porte da escola;
- dependência administrativa;
- ano de referência.

A seleção final das variáveis dependerá da qualidade, completude e compatibilidade dos dados disponíveis.

---

## Hipóteses

O projeto parte das seguintes hipóteses:

1. Escolas com melhores condições gerais de infraestrutura apresentam maiores taxas de aprovação.

2. A presença de recursos pedagógicos e tecnológicos apresenta associação positiva com a taxa de aprovação.

3. Escolas com melhores condições de acessibilidade e serviços básicos apresentam melhores indicadores de rendimento.

4. Uma maior média de alunos por turma pode estar associada a menores taxas de aprovação.

5. Existem diferenças nos indicadores de aprovação entre escolas municipais e estaduais.

6. Modelos que utilizam variáveis de infraestrutura, porte, organização e dependência administrativa podem apresentar desempenho superior a um modelo baseado apenas na média histórica.

As hipóteses ainda não foram confirmadas ou rejeitadas. Sua avaliação será realizada durante a execução das análises.

---

## Metodologia

O projeto será desenvolvido com base na metodologia **CRISP-DM**, composta por seis fases.

### 1. Compreensão do problema

- definição do problema de pesquisa;
- definição dos objetivos;
- levantamento das hipóteses;
- identificação das restrições;
- definição dos critérios de sucesso.

### 2. Compreensão dos dados

- coleta das bases;
- descrição das variáveis;
- análise da estrutura dos arquivos;
- exploração inicial dos dados;
- avaliação da qualidade e da completude.

### 3. Preparação dos dados

- seleção dos registros;
- filtragem das escolas de Porto Alegre;
- tratamento de valores ausentes;
- remoção de duplicidades;
- correção de inconsistências;
- padronização de nomes e códigos;
- integração das bases;
- criação de variáveis derivadas.

### 4. Modelagem

Serão avaliados modelos de regressão, incluindo:

- regressão linear;
- árvore de decisão para regressão;
- Random Forest para regressão.

### 5. Avaliação

Os modelos serão avaliados com as seguintes métricas:

- MAE — Mean Absolute Error;
- RMSE — Root Mean Squared Error;
- R² — coeficiente de determinação.

O desempenho também será comparado com um modelo de referência baseado na média histórica.

### 6. Implantação e apresentação

- construção dos dashboards;
- publicação das análises;
- documentação do processo;
- organização dos códigos e notebooks;
- apresentação dos resultados e limitações.

---

## Estratégia de treinamento e teste

Para preservar a ordem temporal dos dados, será utilizada a seguinte divisão:

- **Treinamento:** dados de 2018 a 2022;
- **Teste:** dados de 2023.

Essa estratégia permite avaliar o desempenho dos modelos em um período posterior ao utilizado durante o treinamento.

---

## Indicadores previstos

Entre os principais indicadores estão:

- taxa de aprovação;
- taxa de reprovação;
- taxa de abandono;
- quantidade de matrículas;
- média de alunos por turma;
- porte da escola;
- indicadores de infraestrutura;
- disponibilidade de recursos pedagógicos;
- disponibilidade de recursos tecnológicos;
- distribuição das escolas por dependência administrativa;
- evolução temporal dos indicadores.

---

## Desenho da solução

O fluxo da solução foi estruturado nas seguintes etapas:

1. coleta dos dados;
2. preparação dos dados;
3. integração das bases;
4. análise descritiva;
5. identificação de fatores associados;
6. construção dos indicadores;
7. desenvolvimento dos dashboards;
8. treinamento dos modelos preditivos;
9. avaliação dos resultados;
10. geração de informações para apoio à gestão educacional.

---

## Tecnologias utilizadas

### Processamento e análise

- Python;
- Pandas;
- NumPy;
- Scikit-learn;
- Matplotlib;
- Plotly;
- Google Colab.

### Business Intelligence

- Power BI;
- Power Query;
- modelagem de dados;
- criação de indicadores;
- desenvolvimento de dashboards.

### Documentação e versionamento

- Git;
- GitHub;
- Markdown;
- LaTeX;
- Overleaf.

---

## Estrutura prevista do repositório

```text
projeto-bi-desempenho-escolar/
├── README.md
├── LICENSE
├── docs/
│   ├── projeto-fase-1.pdf
│   └── desenho-da-solucao.pdf
├── data/
├── notebooks/
├── src/
├── imagens/
└── requirements.txt
```

## Limitações

Este projeto apresenta algumas limitações que devem ser consideradas na interpretação dos resultados:

- diferenças na estrutura e na nomenclatura das bases entre os anos analisados;
- presença de valores ausentes, inconsistentes ou incompletos;
- possíveis mudanças nos códigos e nas classificações das escolas;
- incompatibilidade de granularidade entre algumas fontes de dados;
- indisponibilidade de determinados indicadores para todo o período de 2018 a 2023;
- ausência de fatores socioeconômicos, familiares e pedagógicos nas bases principais;
- impossibilidade de estabelecer relações de causa e efeito apenas com dados observacionais.

As associações encontradas entre as características escolares e a taxa de aprovação não deverão ser interpretadas automaticamente como relações causais.

## Uso responsável dos dados

O projeto utiliza dados públicos relacionados às instituições de ensino.

Não está prevista a utilização de informações pessoais diretamente identificáveis de estudantes, professores ou responsáveis.

Os resultados deverão ser analisados considerando:

- a qualidade e a completude das bases;
- o contexto das escolas;
- possíveis vieses nos dados;
- as limitações dos modelos estatísticos;
- a necessidade de validação por especialistas da área educacional.

As previsões e os indicadores produzidos deverão ser utilizados como apoio à análise e à tomada de decisão, e não como critério único para avaliar ou classificar escolas.

## Licença

Este projeto está licenciado sob a licença MIT.

O código-fonte, os scripts e os notebooks podem ser utilizados, modificados e distribuídos conforme os termos disponíveis no arquivo [LICENSE](LICENSE).

Os dados utilizados pertencem às respectivas fontes oficiais e não são abrangidos automaticamente pela licença deste repositório. Artigos científicos, materiais acadêmicos e conteúdos de terceiros permanecem sujeitos aos direitos e termos definidos por seus respectivos autores e instituições.