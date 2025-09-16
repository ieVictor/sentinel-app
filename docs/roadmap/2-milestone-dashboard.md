## Milestone 2: Visualização de Dados - O Dashboard Pessoal

**Objetivo:** Permitir que o usuário visualize os dados que estão sendo coletados de forma clara e útil.

| Prioridade | Tarefa                                                                                                                                        | Componentes Envolvidos | Requisitos Relacionados |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- | ----------------------- |
| 1          | **API do Dashboard**: Criar os endpoints na API Go que agregam e retornam os dados de atividade do usuário, permitindo filtragem por período. | api                    | RF-100, RF-101, RF-102  |
| 2          | **Construção do UI do Dashboard**: Desenvolver a página do dashboard em React, consumindo os dados da API.                                    | desktop (UI)           | RF-101, RF-102          |
| 3          | **Implementar Filtros**: Adicionar os controles de filtro de período ("Hoje", "Esta Semana", etc.) no frontend.                               | desktop (UI)           | RF-100                  |
| 4          | **Gráficos de Atividade**: Integrar uma biblioteca de gráficos (ex: Recharts) para exibir a distribuição de linguagens e atividade semanal.   | desktop (UI)           | RF-104                  |
| 5          | **Design de "Estado Vazio"**: Implementar as telas para novos usuários que ainda não possuem dados.                                           | desktop (UI)           | RD-322                  |
