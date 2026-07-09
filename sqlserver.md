# SQL Server

## Implementacao especifica

- Definir joins, filtros, ordenacao e agrupamentos necessarios.
- Avaliar indices, plano de execucao e volume de dados esperado.
- Considerar uso de CTE, temp table ou window function quando fizer sentido.
- Revisar risco de lock, deadlock e concorrencia.

## Revisao especifica

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
