# C# e .NET

## Particularidades de arquitetura

Fluxo recomendado:

Request
-> Controller
-> Service
-> Repository
-> Banco
-> Response

## Implementacao especifica

- Verificar controller, service e repository necessarios.
- Mapear DTOs e entities envolvidos.
- Validar autenticacao e autorizacao da API.
- Verificar `global.json` e a versao do SDK.
- Checar migrations em `.db/<schema>/migrations` quando houver impacto de banco.
- Preferir uso correto de `CancellationToken`.
- Garantir uso correto de `async/await`.

## Revisao especifica

Ao revisar codigo .NET, procurar:

- regra de negocio em controller;
- service com responsabilidade excessiva;
- repository com regra de negocio;
- DTO mal definido;
- entity exposta na API;
- falta de validacao;
- falta de `CancellationToken`;
- uso incorreto de `async/await`;
- tratamento ruim de exceptions;
