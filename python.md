# Python

## Implementacao especifica

- Projetos Python podem abranger APIs, automacoes, filas, CLIs e servicos.
- Concentrar integracoes externas em modulos dedicados.
- Evitar scripts monoliticos com muitas responsabilidades.
- Manter configuracoes sensiveis em variaveis de ambiente.
- Validar entradas e saidas de API, fila, CLI ou automacao.

## Revisao especifica

Ao revisar codigo Python, verificar:

- funcoes ou classes com responsabilidade excessiva;
- uso inadequado de estado global;
- excecoes engolidas ou mal tratadas;
- validacao insuficiente de entrada;
- acoplamento excessivo com infraestrutura;
