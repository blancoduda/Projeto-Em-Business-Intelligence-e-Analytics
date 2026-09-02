# Variáveis consolidadas do projeto

## 1. Identificação e localização

| Variável padronizada | Fonte | 2018–2020/2018 | 2021–2023/2019–2023 | Descrição |
|---|---|---|---|---|
| ano_censo | Todas | Ano / NU_ANO_CENSO | NU_ANO_CENSO | Ano de referência |
| codigo_escola | Todas | CO_ENTIDADE | CO_ENTIDADE | Código da escola |
| nome_escola | Todas | NO_ENTIDADE | NO_ENTIDADE | Nome da escola |
| codigo_municipio | Todas | CO_MUNICIPIO | CO_MUNICIPIO | Código do município |
| nome_municipio | Todas | NO_MUNICIPIO | NO_MUNICIPIO | Nome do município |
| uf | Todas | SG_UF | SG_UF | Unidade da Federação |

## 2. Caracterização da escola

| Variável padronizada | Fonte | Nome original | Descrição |
|---|---|---|---|
| dependencia_administrativa | Censo | TP_DEPENDENCIA | Dependência administrativa da escola |
| localizacao | Censo | TP_LOCALIZACAO | Localização urbana/rural |
| situacao_funcionamento | Censo | TP_SITUACAO_FUNCIONAMENTO | Situação de funcionamento |

## 3. Infraestrutura básica

- IN_AGUA_POTAVEL
- IN_AGUA_REDE_PUBLICA
- IN_ENERGIA_REDE_PUBLICA
- IN_ESGOTO_REDE_PUBLICA
- IN_BANHEIRO

## 4. Infraestrutura pedagógica

- IN_BIBLIOTECA
- IN_BIBLIOTECA_SALA_LEITURA
- IN_SALA_LEITURA
- IN_LABORATORIO_CIENCIAS
- IN_LABORATORIO_INFORMATICA

## 5. Tecnologia

- IN_COMPUTADOR
- IN_DESKTOP_ALUNO
- IN_COMP_PORTATIL_ALUNO
- IN_TABLET_ALUNO
- IN_INTERNET
- IN_INTERNET_ALUNOS
- IN_INTERNET_APRENDIZAGEM
- IN_BANDA_LARGA

## 6. Acessibilidade

- IN_BANHEIRO_PNE
- IN_ACESSIBILIDADE_RAMPAS
- IN_ACESSIBILIDADE_CORRIMAO
- IN_ACESSIBILIDADE_PISOS_TATEIS
- IN_ACESSIBILIDADE_SINAL_SONORO
- IN_ACESSIBILIDADE_SINAL_TATIL
- IN_ACESSIBILIDADE_SINAL_VISUAL
- IN_ACESSIBILIDADE_INEXISTENTE

## 7. Porte e organização escolar

- QT_MAT_FUND
- QT_MAT_FUND_AI
- QT_MAT_FUND_AF
- QT_DOC_FUND
- QT_DOC_FUND_AI
- QT_DOC_FUND_AF
- QT_TUR_FUND
- QT_TUR_FUND_AI
- QT_TUR_FUND_AF

## 8. Média de alunos por turma

| Variável padronizada | 2018 | 2019–2023 | Descrição |
|---|---|---|---|
| media_alunos_turma_fund | ATU_FUN | FUN_CAT_0 | Média de alunos por turma no Ensino Fundamental |
| media_alunos_turma_ai | ATU_F14 | FUN_AI_CAT_0 | Média nos anos iniciais |
| media_alunos_turma_af | ATU_F04 | FUN_AF_CAT_0 | Média nos anos finais |

## 9. Indicadores de rendimento

| Variável padronizada | 2018–2020 | 2021–2023 | Descrição |
|---|---|---|---|
| taxa_aprovacao_fund | tap_FUN | 1_CAT_FUN | Taxa de aprovação do Ensino Fundamental |
| taxa_aprovacao_ai | tap_F14 | 1_CAT_FUN_AI | Taxa de aprovação dos anos iniciais |
| taxa_aprovacao_af | tap_F04 | 1_CAT_FUN_AF | Taxa de aprovação dos anos finais |
| taxa_reprovacao_fund | tre_FUN | 2_CAT_FUN | Taxa de reprovação do Ensino Fundamental |
| taxa_reprovacao_ai | tre_F14 | 2_CAT_FUN_AI | Taxa de reprovação dos anos iniciais |
| taxa_reprovacao_af | tre_F04 | 2_CAT_FUN_AF | Taxa de reprovação dos anos finais |
| taxa_abandono_fund | tab_FUN | 3_CAT_FUN | Taxa de abandono do Ensino Fundamental |
| taxa_abandono_ai | tab_F14 | 3_CAT_FUN_AI | Taxa de abandono dos anos iniciais |
| taxa_abandono_af | tab_F04 | 3_CAT_FUN_AF | Taxa de abandono dos anos finais |

## 10. Variável-alvo

**taxa_aprovacao_fund**

Variável-alvo principal do projeto, utilizada nas análises explicativas e nos modelos preditivos.