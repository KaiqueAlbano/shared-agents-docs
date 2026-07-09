# Flutter

## Objetivo

Usar este guia para implementacao e revisao de telas, fluxos e componentes em Flutter e Dart.

## Checklist de pre-implementacao

- Identificar widgets necessarios.
- Definir estado da tela.
- Escolher gerenciamento de estado apropriado.
- Revisar responsividade.
- Revisar comportamento mobile.
- Avaliar performance.
- Planejar navegacao.
- Planejar validacoes.
- Cobrir `loading`, tratamento de erro e `empty state`.
- Revisar acessibilidade.

## Diretrizes de implementacao

Antes de implementar, analisar:

- arquitetura da tela;
- risco de rebuilds desnecessarios;
- separacao entre UI e logica;
- possibilidade de reutilizacao;
- impacto em manutencao futura.

## Code review

Ao revisar codigo Flutter, procurar:

- widgets grandes demais;
- logica dentro da UI;
- rebuilds desnecessarios;
- falta de `const`;
- gerenciamento de estado confuso;
- navegacao acoplada;
- falta de responsividade;
- problemas de performance;
- codigo duplicado;
- tratamento de erro fraco.

## Seguranca e performance

- Nao expor segredos no app.
- Validar fluxos sensiveis e persistencia local.
- Reduzir rebuilds e manter a interface previsivel.
