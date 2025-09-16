## Milestone 1: MVP - Autenticação e Coleta de Dados

**Objetivo:** Ter um sistema onde um usuário pode se cadastrar, logar, e a aplicação desktop começa a rastrear e sincronizar o tempo de programação com o servidor. Esta é a funcionalidade core da aplicação.

| Prioridade | Tarefa                                                                                                                                                                            | Componentes Envolvidos | Requisitos Relacionados                |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- | -------------------------------------- |
| 1          | **API de Autenticação**: Implementar os endpoints de cadastro (e-mail/senha) e login na API Go, integrando com Supabase Auth (`gotrue-go`) e salvando usuários no banco de dados. | api                    | RF-001, RF-002, RF-003, RF-004, RD-332 |
| 2          | **UI de Autenticação**: Criar as telas de Login e Cadastro no React/Tauri.                                                                                                        | desktop (UI)           | RF-006, RF-007                         |
| 3          | **Detecção de Atividade**: Implementar no Core (Rust) a lógica para detectar o editor ativo e a extensão do arquivo para identificar a linguagem.                                 | desktop (Core)         | RD-300                                 |
| 4          | **Detecção de Ociosidade**: Implementar o tracker de inatividade (teclado/mouse) no Core.                                                                                         | desktop (Core)         | RF-020                                 |
| 5          | **Armazenamento Local**: Usar `rusqlite` para salvar os blocos de tempo de atividade localmente no SQLite.                                                                        | desktop (Core)         | 0-stack-and-devops.md                  |
| 6          | **Sincronização de Dados**: Criar um endpoint na API para receber os dados de atividade. Implementar a lógica de sincronização periódica no Core (Rust) usando `reqwest`.         | api, desktop (Core)    | RD-303                                 |
