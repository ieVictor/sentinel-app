# Requisitos do Dashboard

*Este documento especifica os requisitos funcionais para os dashboards, tanto o pessoal (visível apenas para o próprio usuário) quanto o público (visível para outros usuários).*

---

## 10X - Dashboard Pessoal

| ID      | Título                 | Descrição                                                                                                                                |
|---------|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| RF-100  | Filtros de Período     | O dashboard deve permitir a filtragem de todos os dados por períodos de tempo: "Desde Sempre" (All-time), "Este Mês", "Esta Semana" e "Hoje". |
| RF-101  | Detalhes por Linguagem | Deve ser exibida uma tabela listando todas as linguagens programadas, com o tempo total gasto e o tier/ranking atual do usuário em cada uma. |
| RF-102  | Detalhes por Projeto   | O dashboard deve apresentar uma tabela com os projetos em que o usuário trabalhou, exibindo o tempo total gasto em cada um.              |
| RF-103  | Definição de Projeto   | Um "projeto" é identificado pela pasta raiz aberta no editor de código/IDE (geralmente um repositório Git). O nome do projeto será o nome da pasta. |
| RF-104  | Visualização Gráfica   | O dashboard deve incluir visualizações gráficas, como um gráfico de pizza para a distribuição de tempo entre linguagens e um gráfico de linhas para a atividade da semana. |
| RF-105  | Metas Pessoais         | O usuário deve poder definir metas semanais de tempo para linguagens específicas (ex: 10 horas de Rust). O progresso em relação a essas metas deve ser exibido. |

---

## 11X - Dashboard Público de Outros Usuários

| ID      | Título                        | Descrição                                                                                                                         |
|---------|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| RF-110  | Resumo do Usuário             | O dashboard público de outro usuário deve exibir um resumo, mostrando as horas gastas em sua linguagem principal e seu tier/ranking nela. |
| RF-111  | Linguagens Principais         | Deve ser exibida uma tabela com as 10 principais linguagens do usuário, juntamente com o tempo total e o tier/ranking correspondente em cada uma. |
| RF-112  | Comparação Direta com Conexões| No próprio dashboard, ao visualizar uma linguagem, o usuário deve ver um bloco comparativo que mostra seu desempenho (tempo/ranking) em relação às suas conexões. |
