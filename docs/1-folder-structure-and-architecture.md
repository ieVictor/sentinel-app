# Folder structure

```bash
/sentinel-app/
├── .github/
│   └── workflows/
│       ├── api-deploy.yml         # Workflow para deploy da API no Render
│       ├── desktop-release.yml    # Workflow para build e release do app Tauri
│       └── lint-test.yml          # Workflow para rodar linters e testes em cada push
│
├── .vscode/
│   └── settings.json            # Configurações do editor para formatação e lint
│
├── api/                         # Código da API em Go
│   ├── cmd/
│   │   └── server/
│   │       └── main.go          # Ponto de entrada da aplicação
│   ├── internal/                # Lógica principal da API (padrão Go)
│   │   ├── handler/             # Handlers HTTP (onde o Gin vive)
│   │   ├── service/             # Lógica de negócio (ex: calcular rankings)
│   │   ├── storage/             # Lógica de acesso ao banco de dados (pgx)
│   │   └── model/               # Structs de domínio e de DTOs
│   ├── go.mod
│   ├── go.sum
│   └── Dockerfile               # Para construir a imagem da API
│
├── desktop/                     # Código do App Desktop (Tauri + React)
│   ├── src/                     # Código do Frontend (React)
│   │   ├── assets/              # Imagens, fontes, etc.
│   │   ├── components/          # Componentes React reutilizáveis
│   │   ├── hooks/               # Custom hooks (ex: useUserData)
│   │   ├── pages/               # Componentes de página (ex: Dashboard, Ranking)
│   │   ├── services/            # Lógica de comunicação com o Core (invokes)
│   │   ├── store/               # Lojas do Zustand
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── src-tauri/               # Código do Core (Rust)
│   │   ├── src/
│   │   │   ├── commands.rs      # Funções expostas para o frontend (`#[tauri::command]`)
│   │   │   ├── core/            # Módulo para a lógica principal
│   │   │   │   ├── detector.rs  # Lógica para detectar atividade, IDE, linguagem
│   │   │   │   ├── db.rs        # Interação com o SQLite local
│   │   │   │   └── sync.rs      # Lógica para sincronizar dados com a API (reqwest)
│   │   │   ├── error.rs         # Definição de erros customizados
│   │   │   └── main.rs          # Ponto de entrada do backend Tauri
│   │   ├── Cargo.toml
│   │   └── tauri.conf.json
│   ├── package.json
│   └── tailwind.config.js
│
├── docs/                        # Documentação
│   └── ARCHITECTURE.md          # Este documento que estamos discutindo :)
│
├── .editorconfig
├── .gitignore
└── README.md                    # Instruções de setup, como rodar, etc.
```

---

# Arquiteturas utilizadas

## DESKTOP

**Model-View-Controller**

- View (React)
- Controller (Comandos Tauri)
- Model (Lógica Core em Rust)

## API

**Controller-Service-Storage**

- Handler (Controller)
- Service
- Storage (Repository)

**Dependency Injection**
