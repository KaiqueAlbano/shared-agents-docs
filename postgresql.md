# PostgreSQL

## Implementacao especifica

- Avaliar joins, filtros, ordenacao e agrupamentos.
- Estimar volume de dados e impacto em transacoes.
- Revisar indices necessarios.
- Considerar uso de CTE e janela analitica quando fizer sentido.
- Revisar concorrencia e rollback em rotinas criticas.

## Revisao especifica

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
