# C# e .NET

## Objetivo

Usar este guia para implementacao, revisao e explicacao de codigo em .NET e C#.

## Checklist de pre-implementacao

- Verificar controller necessario.
- Verificar service necessario.
- Verificar repository necessario.
- Mapear DTOs e entities envolvidos.
- Validar autenticacao e autorizacao.
- Avaliar impacto no banco.
- Avaliar impacto em testes.
- Avaliar risco de regressao.

## Build, teste e deploy

- Verificar `global.json` e a versao do SDK.
- Rodar restore, build e testes automatizados da solucao quando existirem.
- Checar migrations em `.db/<schema>/migrations`.
- Nao executar publicacao sem autorizacao explicita.

## Fluxo arquitetural recomendado

Request
-> Controller
-> Service
-> Repository
-> Banco
-> Response

## Diretrizes de implementacao

Antes de implementar, analisar:

- validacoes;
- logs;
- tratamento de erros;
- responsabilidade de cada camada;
- risco de acoplamento;
- possibilidade de reutilizacao.

Depois dividir a implementacao em etapas pequenas.

## Code review

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
- logs insuficientes;
- problemas de performance;
- problemas de seguranca;
- acoplamento excessivo;
- violacao de SOLID.

## Seguranca e performance

- Nao expor dados sensiveis.
- Validar entrada e saida.
- Evitar consultas desnecessarias e processamento redundante.
- Priorizar clareza, manutencao e baixo risco de regressao.
