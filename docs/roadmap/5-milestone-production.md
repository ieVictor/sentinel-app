# Milestone 5: Polimento e Preparação para Produção

**Objetivo:** Finalizar a aplicação, cuidando de casos de uso secundários, otimizações de performance e o processo de deploy.

| Prioridade | Tarefa                                                                                                                                                          | Componentes Envolvidos | Requisitos Relacionados |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- | ----------------------- |
| 1          | **Finalizar CI/CD**: Configurar e testar os workflows `api-deploy.yml` e `desktop-release.yml`.                                                                 | .github, api, desktop  | 0-stack-and-devops.md   |
| 2          | **Deploy da API**: Publicar a API no Render.                                                                                                                    | api                    | 0-stack-and-devops.md   |
| 3          | **Assinatura e Auto-Update**: Adquirir os certificados de código e configurar o auto-update do Tauri.                                                           | desktop                | 0-stack-and-devops.md   |
| 4          | **Funcionalidades Adicionais**: Implementar login social (SSO), recuperação de senha e vinculação de contas.                                                    | api, desktop (UI)      | RF-005, RD-310, RD-311  |
| 5          | **Página de Configurações**: Criar a página de configurações para gerenciar perfil, ociosidade e privacidade.                                                   | desktop (UI)           | RD-320                  |
| 6          | **Otimização de Performance**: Realizar testes de carga na API e monitorar o consumo de recursos do cliente desktop para atender aos requisitos não-funcionais. | api, desktop (Core)    | RD-330, RD-331          |
