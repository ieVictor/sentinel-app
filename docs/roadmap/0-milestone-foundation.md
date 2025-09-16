# Milestone 0: Fundação e Estrutura do Projeto (Sprint 0)

**Objetivo:** Configurar o ambiente de desenvolvimento, a estrutura do projeto e o CI/CD básico para garantir qualidade desde o primeiro commit.

| Prioridade | Tarefa                                                                                                                                                     | Componentes Envolvidos | Requisitos Relacionados |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- | ----------------------- |
| 1          | **Setup do Monorepo**: Criar a estrutura de pastas conforme o `1-folder-structure-and-architecture.md`.                                                    | Geral                  | -                       |
| 2          | **"Hello World" da API**: Iniciar o projeto Go, configurar o Gin e criar um endpoint `/health` que retorna `200 OK`.                                       | api                    | -                       |
| 3          | **"Hello World" do Desktop**: Iniciar o projeto Tauri com React, garantindo que a janela da aplicação abra.                                                | desktop                | -                       |
| 4          | **CI Básico**: Configurar o workflow `lint-test.yml` no GitHub Actions para rodar formatadores (`gofmt`, `cargo fmt`, `prettier`) e linters a cada push.   | .github                | 0-stack-and-devops.md   |
| 5          | **Definição do Schema do Banco de Dados**: Modelar e criar as tabelas iniciais no Supabase (ex: `users`, `programming_activity`, `projects`, `languages`). | database               | RF-001, RF-101, RF-102  |
