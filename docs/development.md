# Desenvolvimento

Para só rodar o projeto, o [README](../README.md) basta. Aqui fica o que é
preciso para mudá-lo.

## Requisitos

| Ferramenta | Versão | Conferir |
| --- | --- | --- |
| <Ferramenta> | <versão> | `<ferramenta> --version` |

## Stack e arquitetura

<Framework, linguagem e gerenciador de pacotes em uma linha.> Stack completa,
dependências e features em [architecture.md](architecture.md).

## Comandos

| Para | Comando |
| --- | --- |
| Instalar dependências | `<comando>` |
| Rodar localmente | `<comando>` |
| Lint | `<comando>` |
| Checagem de tipos | `<comando>` |
| Testes unitários | `<comando>` |
| Todos os testes (igual à CI) | `<comando>` |
| Build | `<comando>` |

## Variáveis de ambiente

`cp .env.example .env` e preencha conforme o [README](../README.md#3-configure).

<!-- Como o framework lê o .env e quais variáveis chegam ao navegador (ex.: no Next.js, só as NEXT_PUBLIC_*). -->

## Integração contínua

| Workflow | O que faz |
| --- | --- |
| `.github/workflows/conventions.yml` | Falha se o título do PR ou algum commit não segue o Conventional Commits |

O Dependabot (`.github/dependabot.yml`) abre PRs semanais de atualização.

## Commits e pull requests

Toda mudança chega à `main` por pull request a partir de uma branch. Commits
e títulos de PR seguem o [Conventional Commits](https://www.conventionalcommits.org/):
`<type>(<scope opcional>): <descrição>`, com a feature como escopo.

| Tipo | Quando |
| --- | --- |
| `feat` | Funcionalidade nova |
| `fix` | Correção de bug |
| `refactor` | Mudança de código sem mudar comportamento |
| `test` | Só testes |
| `docs` | Só documentação |
| `chore` | Manutenção que não entra em outro tipo |
| `build` | Build e dependências |
| `ci` | Workflows de CI |

`!` antes do `:` marca uma mudança incompatível. Rode uma vez depois de clonar:

```bash
git config core.hooksPath .githooks       # recusa commits fora da convenção
git config commit.template .gitmessage    # abre o modelo no git commit
```

O PR é preenchido com `.github/pull_request_template.md`. Nele vão a spec, as
mudanças em [architecture.md](architecture.md) e [api.md](api.md) e as
decisões novas.
