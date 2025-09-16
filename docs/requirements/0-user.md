# Requisitos de Usuário e Funcionalidades Essenciais

_Este documento detalha os requisitos funcionais relacionados à autenticação, perfil do usuário e funcionalidades essenciais do sistema Sentinel._

---

## 00X - Autenticação

| ID     | Título                | Descrição                                                                                                              |
| ------ | --------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| RF-001 | Cadastro de Usuário   | O sistema deve permitir o cadastro de novos usuários através de nome, e-mail e senha.                                  |
| RF-002 | Requisito de Senha    | A senha definida pelo usuário deve conter, no mínimo, 8 caracteres para garantir a segurança.                          |
| RF-003 | Validação de E-mail   | O e-mail fornecido no cadastro deve ser único na plataforma e seguir um formato válido.                                |
| RF-004 | Login com Credenciais | O sistema deve autenticar usuários existentes utilizando e-mail e senha.                                               |
| RF-005 | Login Social (SSO)    | O usuário deve poder se cadastrar e autenticar utilizando suas contas do Google ou Github.                             |
| RF-006 | Tratamento de Erros   | Em caso de falha no login ou registro, uma mensagem clara e informativa deve ser exibida ao usuário.                   |
| RF-007 | Login Pós-Registro    | Após concluir o cadastro com sucesso, o usuário deve ser automaticamente autenticado e redirecionado para a aplicação. |

---

## 01X - Perfil e Funcionalidades Core

| ID     | Título                    | Descrição                                                                                                                                                                       |
| ------ | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RF-010 | Perfil de Usuário         | Cada usuário deve possuir um perfil público que exibe sua imagem, nome e uma breve descrição pessoal.                                                                           |
| RF-011 | Edição de Perfil          | O usuário deve ter a capacidade de alterar as informações do seu perfil, como imagem, nome e descrição.                                                                         |
| RF-012 | Sistema de Conexões       | O usuário A pode seguir o usuário B. Se B seguir A de volta, eles se tornam "conexões", permitindo comparações diretas em leaderboards e dashboards.                            |
| RF-020 | Detecção de Status Ocioso | O cliente desktop (core) deve identificar inatividade do usuário (ausência de teclado/mouse) por um período configurável (padrão de 5 minutos) para pausar a contagem de tempo. |
