# Detalhamento de Requisitos e Casos de Uso

*Este documento complementa os requisitos existentes, detalhando regras de negócio, casos de uso específicos e requisitos não-funcionais para garantir clareza na implementação.*

---

## 30X - Detalhamento da Lógica "Core" e Fórmulas

| ID      | Título                              | Detalhamento                                                                                                                                                                                                                       |
|---------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RD-300  | Detecção de Linguagem/IDE           | O sistema **core** deve identificar a linguagem primária com base na extensão do arquivo ativo no editor de texto/IDE. Uma tabela de mapeamento (ex: `.py` -> Python, `.rs` -> Rust) deve ser definida. Para arquivos com múltiplas linguagens (ex: `.html`), a linguagem principal do arquivo deve ser considerada. |
| RD-301  | Fórmula de Cálculo de Tiers         | É necessário definir os marcos exatos para cada tier por linguagem. **Exemplo Sugerido:**<br>Bronze: 10 horas<br>Prata: 50 horas<br>Ouro: 150 horas<br>Platina: 300 horas<br>Diamante: 500+ horas                                         |
| RD-302  | Fórmula do "Tier Geral"             | A fórmula para o "Tier Geral" (RF-201) precisa ser especificada. **Sugestão:** Um sistema de pontos onde cada tier vale uma pontuação (Bronze=1, Prata=2, etc.). O "Tier Geral" é a soma dos pontos de todas as linguagens.              |
| RD-303  | Frequência de Sincronização         | O cliente desktop deve sincronizar os dados de tempo com a API em intervalos definidos (ex: a cada 15 minutos) ou ao encerrar a aplicação para garantir a consistência dos dados e permitir o funcionamento offline.                     |

---

## 31X - Casos de Uso e Edge Cases de Autenticação/Usuário

| ID      | Título                  | Detalhamento                                                                                                         |
|---------|-------------------------|---------------------------------------------------------------------------------------------------------------------|
| RD-310  | Recuperação de Senha    | Deve existir um fluxo de "Esqueci minha senha" onde o usuário pode solicitar um link de redefinição por e-mail.      |
| RD-311  | Vinculação de Contas    | O sistema deve gerenciar o caso de um usuário que se cadastra com e-mail/senha e depois tenta fazer login com SSO (Google/Github) usando o mesmo e-mail. As contas devem ser vinculadas para evitar duplicidade. |
| RD-312  | Controle de Privacidade | O usuário deve ter uma opção em seu perfil para tornar seu dashboard completamente privado, impedindo que outros usuários (mesmo conexões) vejam seus dados de atividade. |

---

## 32X - Detalhamento de UX e Interface

| ID      | Título                         | Detalhamento                                                                                                                             |
|---------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| RD-320  | Página de Configurações        | É necessário criar uma página de "Configurações" onde o usuário possa:<br>1. Editar seu perfil (RF-011)<br>2. Configurar o tempo de ociosidade (RF-020)<br>3. Gerenciar configurações de privacidade (RD-312)<br>4. Gerenciar notificações. |
| RD-321  | Sistema de Notificações        | O sistema deve notificar o usuário (dentro do app) quando:<br>- Uma meta semanal é atingida (RF-105).<br>- Uma nova conquista é desbloqueada (RF-202).<br>- Um novo tier é alcançado (RF-200).<br>- Recebe um novo seguidor.            |
| RD-322  | "Estados Vazios" do Dashboard  | O design do dashboard deve prever como a interface será exibida quando não houver dados. Por exemplo, um novo usuário que ainda não registrou nenhuma atividade de programação deve ver uma mensagem de boas-vindas e um guia de como começar. |

---

## 33X - Requisitos Não-Funcionais

| ID      | Título                   | Detalhamento                                                                                                                     |
|---------|--------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| RD-330  | Performance do Cliente   | O cliente desktop deve consumir recursos mínimos de CPU e Memória (<5% de CPU e <100MB de RAM em média) para não impactar o desempenho do desenvolvimento do usuário, já que rodará em segundo plano. |
| RD-331  | Performance da API       | As respostas da API para carregamento de dashboards e leaderboards devem ter um tempo médio de resposta inferior a 500ms para garantir uma experiência de usuário fluida.                             |
| RD-332  | Segurança de Dados       | Todas as senhas de usuário devem ser armazenadas utilizando algoritmos de hashing seguros (ex: bcrypt). Toda a comunicação entre o cliente desktop e a API deve ser feita via HTTPS.                  |
