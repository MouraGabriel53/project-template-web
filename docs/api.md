# API

As APIs que o app consome. Os campos e erros de cada chamada ficam na spec
que a usa; aqui fica onde ver cada API.

| API | URL base (variável) | Swagger | Usada por |
| --- | --- | --- | --- |
| <Backend> | `<API_URL>` | <http://localhost:8080/swagger-ui/index.html> | `features/<nome>` |

## Endpoints usados

<!-- Uma linha por endpoint que o app chama. -->

| Método | Endpoint | Operação |
| --- | --- | --- |
| `POST` | `/api/v1/<recurso>` | [NNN - <Operação>](<contexto>/NNN_<operação>.md) |

## Erros

<!-- Como o app trata o formato de erro comum das APIs (ex.: Problem Details, RFC 9457). -->
