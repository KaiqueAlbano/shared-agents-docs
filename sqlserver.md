# SQL Server

## Objetivo

Usar este guia para criacao e revisao de queries, procedures e funcoes em SQL Server e T-SQL.

## Checklist de pre-implementacao

- Definir o objetivo da consulta.
- Mapear tabelas envolvidas.
- Definir joins necessarios.
- Definir filtros e ordenacao.
- Avaliar agrupamentos.
- Avaliar indices necessarios.
- Estimar volume de dados.
- Revisar risco de lock e deadlock.
- Considerar impacto em objetos existentes.

## Diretrizes de implementacao

Antes de escrever SQL, analisar:

- plano de execucao esperado;
- possibilidade de uso de CTE, temp table ou window function;
- impacto em concorrencia;
- impacto em performance;
- estrategia de rollback quando aplicavel.

## Code review

Ao revisar SQL Server, verificar:

- uso de `SELECT *`;
- joins desnecessarios;
- filtros nao SARGable;
- funcoes em colunas filtradas;
- conversoes implicitas;
- indices ausentes;
- agrupamentos caros;
- ordenacao custosa;
- uso inadequado de temp table;
- risco de lock;
- risco de deadlock;
- performance em grande volume;
- legibilidade.

## Seguranca e performance

- Evitar SQL inseguro e acesso desnecessario a dados sensiveis.
- Priorizar consultas previsiveis e bem indexadas.
- Comparar a versao local com o banco antes de alterar objetos existentes.
