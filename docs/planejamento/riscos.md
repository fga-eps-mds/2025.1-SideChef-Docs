# Gerenciamento de riscos

## Histórico de versões

| Versão | Alteração       | Responsável         | Data Alteração |
|--------|-----------------|---------------------|----------------|
| 1.0    | Versão inicial do documento, incluindo introdução, planejamento, métricas, análise e resposta aos riscos  | Bruno Seiji Kishibe | 30/04/2025 |
| 1.1    | Remove resposta aos Riscos e Monitoramento  | Diógenes Dantas Lélis Júinior | 14/07/2025 |

## Introdução

O gerênciamento de riscos representa um elemento importante dentro do gerênciamento de projetos, sendo uma das áreas de conhecimento embutidas dentro do PMBOK.

Este documento tem como objetivo explicitar como foram definidas e calculadas as métricas de risco, além de mostrar quais serão as respostas para a mitigação ao erro e a monitoração da evolução desses riscos ao longo do projeto.

## Planejamento gerênciamento de riscos

Nessa etapa definimos como conduzir as atividades de gerenciamento dos riscos de um projeto.

### Métricas

A magnitude de um risco pode ser definida por: 

$magnitude = (probabilidade * impacto)$.

Em que a probalidade representa o quão provavel é de o risco associado acontecer, já o impacto, o quanto impactará no desenvolvimento do time se o risco vier a acontecer. Em ambos será utilizada uma escala de 1 a 10, sendo 1 menor probabilidade/impacto e 10 maior probabilidade/impacto.

### Probabilidade

No que se refere à probabilidade de ocorrência dos riscos do projeto, foram definidos 11 níveis de risco, com base em intervalos graduais de probabilidade. Cada nível foi associado a um score correspondente de 0 a 10, conforme mostrado na tabela abaixo:

| Nível de Risco          | Score (0 a 10) |
|--------------------------|----------------|
| Quase Impossível         | 0              |
| Extremamente Raro        | 1              |
| Muito Raro               | 2              |
| Raro                     | 3              |
| Improvável               | 4              |
| Possível                 | 5              |
| Moderadamente Provável   | 6              |
| Provável                 | 7              |
| Muito Provável           | 8              |
| Altamente Provável       | 9              |
| Quase Certo              | 10             |

### Impacto

No que se refere ao impacto de cada risco no projeto, foram definidos 11 níveis de impacto, organizados em buckets. Cada nível recebeu um score de 0 a 10, com incrementos de 1 ponto, conforme a tabela a seguir:

| Nível de Impacto        | Score (0 a 10) |
|--------------------------|----------------|
| Quase Nulo               | 0              |
| Extremamente Baixo       | 1              |
| Muito Baixo              | 2              |
| Baixo                    | 3              |
| Ligeiramente Baixo       | 4              |
| Moderado                 | 5              |
| Ligeiramente Alto        | 6              |
| Alto                     | 7              |
| Muito Alto               | 8              |
| Extremamente Alto        | 9              |
| Catastrófico             | 10             |


## Identificação de riscos e análise quantitativa

Para a identificação dos riscos o time utiliza das reuniões para identificar dificuldades e impedimentos apresentados pelos membros da equipe.

Abaixo estão listados os riscos e a análise quantitativa dos riscos identificados.

| Quando foi Identificado | Descrição                                           | Probabilidade | Impacto |
| ----------------------- | --------------------------------------------------- | ------------- | ------- |
| Sprint 1                | Baixo conhecimento a respeito das tecnologias       | 10            | 10      |
| Sprint 1                | Erros arquiteturais                                 | 7             | 10      |
| Sprint 1                | Não participação dos membros da equipe nas reuniões | 9             | 7       |
| Sprint 2                | Baixa disponibilidade de tempo por alguns membros   | 7             | 10      |
| Sprint 3                | Outras Disciplinas                                  | 7             | 10      |
| Sprint 6                | Demora na revisão dos Pull Requests                 | 7             | 10      |


## Referências

> [1] PROJECT MANAGEMENT INSTITUTE (PMI). Guia PMBOK: Um Guia do Conhecimento em Gerenciamento de Projetos [4ª ed.]. São Paulo: Project Management Institute, 2013.

> [2] Ray, Stephanie. The Risk Management Process in Project Management. ProjectManager, 27 de fev. de 2021. Disponível em : https://www.projectmanager.com/blog/risk-management-process-steps. Acesso em 28 de abr. de 2025.

> [3] PROJECT MANAGEMENT INSTITUTE. Risk burndown. Disponível em: https://www.pmi.org/disciplined-agile/agile/riskburndown. Acesso em: 28 abr. 2025.


