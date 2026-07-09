# PostgreSQL

## Objetivo

Usar este guia para criacao, revisao e manutencao de queries, funcoes e rotinas em PostgreSQL e PL/pgSQL.

## Checklist de pre-implementacao

- Definir o objetivo da query ou funcao.
- Mapear tabelas, visoes e funcoes envolvidas.
- Avaliar joins, filtros, ordenacao e agrupamentos.
- Estimar volume de dados.
- Revisar indices necessarios.
- Avaliar impacto em transacoes, concorrencia e rollback.
- Verificar impacto em objetos existentes.

## Diretrizes de implementacao

Antes de escrever SQL, analisar:

- plano esperado de execucao;
- risco de full scan;
- possibilidade de uso de CTE;
- possibilidade de usar janela analitica;
- impacto em concorrencia;
- impacto em performance;
- clareza e legibilidade da consulta.

## Code review

Ao revisar SQL PostgreSQL, verificar:

- full table scan desnecessario;
- indice ausente;
- joins caros;
- ordenacao pesada;
- filtros nao otimizados;
- funcoes impedindo uso de indice;
- uso inadequado de CTE;
- problemas de transacao;
- problemas de concorrencia;
- legibilidade e manutencao.

## Seguranca e performance

- Evitar acesso desnecessario a dados sensiveis.
- Priorizar consultas previsiveis e bem indexadas.
- Validar impacto de mudancas em objetos compartilhados.
- Comparar a versao local com a versao do banco antes de alterar funcoes, procedures, views e tabelas.
