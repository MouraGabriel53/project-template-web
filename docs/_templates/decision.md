# 0001 - Senhas com bcrypt

<!--
Modelo de decisão. Copie para docs/decisions/NNNN-titulo-curto.md com o
próximo número, troque o exemplo e adicione a linha no índice
(decisions/README.md). Depois do merge, nunca edite: escreva outra que a
substitua.
-->

| Status | Data | Spec |
| --- | --- | --- |
| Aceita | AAAA-MM-DD | [001 - Register User](../user/001_register_user.md) |

<!-- Status: Aceita, ou Substituída por NNNN. -->

## Contexto

A senha do usuário precisa ser guardada de forma que um vazamento do banco não revele a senha original.

## Decisão

Guardar a senha com bcrypt, custo 12, usando o encoder do framework.

## Alternativas

| Opção | Por que não |
| --- | --- |
| Argon2 | Exige dependência nova |
| SHA-256 com salt | Rápido demais: facilita ataque de força bruta |

## Consequências

| Fica mais fácil | Fica mais difícil |
| --- | --- |
| Nenhuma dependência nova | Cada login gasta ~100 ms de CPU |
