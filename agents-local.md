# agents-local.md

Este arquivo funciona como orquestrador local do projeto.

Use este arquivo quando o projeto consumir documentacao compartilhada, mas ainda precisar manter contexto proprio, regras locais e excecoes especificas.

## Ordem de leitura recomendada

1. `docs-shared/estrutura.md`
2. `docs-shared/manutencao.md`
3. arquivo da stack usada em `docs-shared/`, como `react.md`, `python.md`, `csharp.md`, `flutter.md`, `sqlserver.md` ou `postgresql.md`
4. `regrasnegocio.md`
5. `arquitetura-local.md`
6. outros arquivos locais relevantes para o projeto

## Regras de precedencia

- A documentacao compartilhada em `docs-shared/` define o padrao global.
- Os arquivos locais do projeto definem contexto, excecoes e regras especificas deste repositorio.
- Em caso de conflito, a regra local prevalece apenas para este projeto.

## Objetivo do arquivo local

- apontar a ordem correta de leitura;
- indicar quais documentos compartilhados devem ser usados;
- registrar quais arquivos locais complementam o padrao global;
- evitar duplicacao desnecessaria da documentacao central.

## Estrutura minima sugerida no projeto

```txt
meu-projeto/
|-- docs-shared/
|-- agents.md
`-- restante do projeto
```

## Modelo base

```md
# agents.md

Leia nesta ordem:

1. `docs-shared/estrutura.md`
2. `docs-shared/manutencao.md`
3. `docs-shared/react.md`
4. `regrasnegocio.md`
5. `arquitetura-local.md`

Regras:
- `docs-shared/` define o padrao global.
- `regrasnegocio.md` define o dominio deste projeto.
- `arquitetura-local.md` registra decisoes tecnicas especificas.
- Em caso de conflito, a regra local prevalece neste repositorio.
```
