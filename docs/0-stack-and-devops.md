# SENTINEL STACK
Aplicação leve que tem como objetivo ler informações como:
- Quanto tempo o usuário passou programando uma linguagem X;
- O usuário está ocioso ou programando?

Também inclui um sistema de gamificação:
- Rankings nacionais e globais do tempo passado em um linguagem;
- Tiers que o usuário pode alcançar (eg. bronze, silver, gold etc...);

## UI

| omponente        | Tecnologia         | Vantagem                  |
| ---------------- | ------------------ | ------------------------- |
| Framework        | Rust               | Leveza e Performance      |
| Biblioteca UI    | React              | Componentes reutilizáveis |
| Estilização      | Tailwind           | Produtividade             |
| Comunicação CORE | API TAURI `invoke` | Padronização              |

- Gerenciamento de estado: [Zustand](https://zustand-demo.pmnd.rs/)
- Icones: [Lucide](https://lucide.dev/icons/)

## CORE

| Componente        | Tecnologia | Vantagem                   |
| ----------------- | ---------- | -------------------------- |
| Framework         | 🦀 Rust    | Segurança e Memória        |
| Runtime           | `tokio`    | Performance e Concorrência |
| Acesso ao DBLocal | `rusqlite` | Segurança e Ergonomia      |
| Cliente HTTP      | `reqwest`  | Simplicidade               |

- Observabilidade: [tracing](https://docs.rs/tracing/latest/tracing/) + [anyhow](https://docs.rs/anyhow/latest/anyhow/)

## API

| Componente               | Tecnologia  | Vantagem                   |
| ------------------------ | ----------- | -------------------------- |
| Linguagem Principal      | Go          | Simplicidade e Performance |
| Roteamento               | `Gin`       | Leveza e Velocidade        |
| Acesso ao banco de dados | `pgx`       | Performance                |
| Testes                   | `net/http/htttest` | Testes unitários   |
| Token                    | `gotrue-go` | Integração com Supbase     |

- Enviroment Variables: [viper](https://github.com/spf13/viper)

## DATABASE

| Componente      | Tecnologia | Vantagem                |
| --------------- | ---------- | ----------------------- |
| Local (Desktop) | `Sqlite`   | Zero configuração       |
| Cloud           | `Supabase` | Performance e Segurança |

- Schema Migrations: [Supabase CLI](https://supabase.com/docs/guides/cli)

# DevOps

## Hospedagem da API

A API será hospedada no Render. Se no futuro for necessário otimizar o custo, será feito a migração para o
Google Cloud Run.

## Nome do domínio

O nome do domínio ainda não foi definido. Mas provavelmente será algo como `sentinel.app`.

## CI/CD

O CI/CD será feito com o Github Actions. Será utilizado o Docker para construir a imagem da aplicação.
Vamos utilizar as seguintes actions:

- Deploy API (Go) to Render
- Build & Release Desktop App (Tauri)

Talvez utilizaremos o Git Hooks para forçar a formatação com (`gofmt`, `cargofmt` `preetier` etc.)

## Deploy Desktop

- [ ] Será necessário adquirir um certificado para os arquivos `.msi` e `.dmg`.
- [ ] Configurar o Tauri auto-update.
