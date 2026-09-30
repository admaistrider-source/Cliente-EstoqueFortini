# Equipe de agentes de desenvolvimento

Subagentes do Claude Code para o sistema de estoque Fortini. O Claude Code os carrega automaticamente desta pasta; chame um pelo nome (por exemplo, "use o agente arquiteto para planejar o cadastro de produtos") ou deixe o Claude escolher pela descrição.

| Agente | Papel | Edita código? |
|---|---|---|
| `arquiteto` | Planeja funcionalidades, decide stack e modelo de domínio | Não |
| `backend` | Regras de negócio, APIs, banco de dados, migrações e importação de dados | Sim |
| `frontend` | Telas, formulários e relatórios | Sim |
| `devops` | Ambiente, CI/CD, deploy, backups e monitoramento | Sim |
| `qa-testes` | Testes automatizados e reprodução de bugs | Sim |
| `revisor-codigo` | Revisão de código antes do PR | Não |

## Fluxo sugerido
1. `arquiteto` transforma o pedido em plano e tarefas.
2. `backend` e `frontend` implementam as tarefas.
3. `qa-testes` cobre e valida os fluxos.
4. `revisor-codigo` revisa o diff; os achados voltam para quem implementou.
5. `devops` mantém CI, deploy e backups funcionando.

O repositório ainda não tem stack definida. Quando ela for escolhida, atualize os agentes com as ferramentas e comandos concretos (framework, gerenciador de pacotes, comandos de teste e lint).
