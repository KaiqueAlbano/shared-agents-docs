# Python

## Objetivo

Usar este guia para implementacao, revisao e manutencao de projetos Python, incluindo APIs, automacoes e servicos.

## Checklist de pre-implementacao

- Identificar o objetivo do modulo, servico ou script.
- Mapear dependencias internas e externas.
- Definir validacoes de entrada e saida.
- Verificar impacto em configuracao, banco e integracoes.
- Avaliar impacto em testes e risco de regressao.
- Procurar implementacao semelhante antes de criar nova logica.

## Estrutura recomendada

- Separar regras de negocio de infraestrutura.
- Concentrar integracoes externas em modulos dedicados.
- Evitar scripts monoliticos com muitas responsabilidades.
- Manter configuracoes sensiveis em variaveis de ambiente.
- Organizar utilitarios compartilhados sem duplicacao.

## Diretrizes de implementacao

Antes de implementar, analisar:

- responsabilidade da classe, funcao ou modulo;
- possibilidade de reutilizacao;
- validacoes necessarias;
- tratamento de erro;
- logs necessarios;
- impacto em performance;
- impacto em seguranca;
- clareza do fluxo e manutencao futura.

## Code review

Ao revisar codigo Python, verificar:

- funcoes ou classes com responsabilidade excessiva;
- duplicacao de logica;
- uso inadequado de estado global;
- excecoes engolidas ou mal tratadas;
- validacao insuficiente de entrada;
- acoplamento excessivo com infraestrutura;
- nomes pouco claros;
- ausencia de testes;
- pontos de performance sensiveis;
- exposicao de segredos ou dados sensiveis.

## Testes, seguranca e performance

- Criar testes unitarios e de integracao quando aplicavel.
- Validar entradas e saidas de API, fila, CLI ou automacao.
- Evitar processamento redundante e consultas repetidas.
- Nao expor tokens, senhas ou chaves no codigo.
- Priorizar codigo legivel, previsivel e facil de evoluir.
