# React

## Objetivo

Usar este guia para implementacao e revisao de interfaces em React com TypeScript ou JavaScript.

## Checklist de pre-implementacao

- Definir a responsabilidade do componente ou da tela.
- Mapear props necessarias.
- Mapear estados necessarios.
- Identificar hooks necessarios.
- Avaliar chamadas de API.
- Cobrir `loading`, `error` e `empty state`.
- Revisar responsividade.
- Revisar acessibilidade.
- Avaliar possibilidade de reutilizacao.
- Verificar se ja existe componente semelhante.

## Estrutura recomendada

- Componentes em `components/`.
- Hooks em `hooks/`.
- Rotas em `routes/`.
- Servicos em `services/`.
- Paginas em `pages/`.
- Utilitarios, constantes e contexto em suas pastas dedicadas.

## Diretrizes de implementacao

Antes de criar um componente ou tela, analisar:

- responsabilidade unica;
- estrutura de estado;
- integracao com API;
- validacoes;
- comportamento em desktop, tablet e mobile;
- impacto de performance;
- acessibilidade e semantica.

## Code review

Ao revisar codigo React, verificar:

- renderizacoes desnecessarias;
- estado duplicado;
- props confusas;
- componente com responsabilidades demais;
- componente grande demais;
- hooks mal utilizados;
- `useEffect` desnecessario;
- problemas de acessibilidade;
- problemas de responsividade;
- ausencia de `loading`, `error` ou `empty state`;
- duplicacao de codigo;
- oportunidade de extrair hook customizado;
- problemas de tipagem em TypeScript;
- inconsistencias entre codigo TypeScript e JavaScript.

## Seguranca e performance

- Evitar expor dados sensiveis no cliente.
- Validar entradas de formularios.
- Reduzir renderizacoes e chamadas duplicadas.
- Priorizar componentes claros, reutilizaveis e escalaveis.
