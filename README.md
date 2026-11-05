# QUALITY-TEST — Testes de QA da API Clyvo Vet

Entrega da sprint **Compliance, Quality Assurance & Tests** (FIAP).
Este repositório reúne a evidência da **automação de testes** da API
[DotNet](https://github.com/FIAP-2026-CHALLENGE/DotNet), em ASP.NET Core.

## Links da entrega

| Item | Link |
|---|---|
| Azure Boards (testes manuais) | https://dev.azure.com/RM562145/FIAP-CHALLENGE |
| Plano de testes no Azure Test Plans | https://dev.azure.com/RM562145/FIAP-CHALLENGE/_testPlans/execute?planId=369&suiteId=396 |
| Vídeo da automação | https://youtu.be/DHg2T0sYve0 |

## Testes automatizados (Postman)

A coleção está em `postman/FIAP-QA-API-Testes.postman_collection.json`.


| # | Teste | Entrada | Saída esperada |
|---|---|---|---|
| 1 | Login válido | usuário e senha corretos | 200 e `accessToken` |
| 2 | Login com senha incorreta | senha errada | 401 e ProblemDetails "Não autorizado" |
| 3 | Listagem de animais sem token | requisição sem autenticação | 401 e nenhum dado de animal |
| 4 | Cadastro de responsável com token | JWT válido, CPF e e-mail gerados | 201 e responsável criado |

## Resultados dos testes manuais (Azure Test Plans)

Plano com 23 casos de teste executados: 100% Passed.

<img width="999" height="384" alt="image" src="https://github.com/user-attachments/assets/a35c515b-12bf-4918-a174-3d8a31fe4c55" />

## Resultados dos testes automatizados (Postman)

Execução da coleção no Collection Runner: 4 requisições, 8 testes aprovados, 0 falhas.

<img width="1357" height="660" alt="image" src="https://github.com/user-attachments/assets/0898e26d-9a04-4f1d-8f6f-65f35cda177a" />



