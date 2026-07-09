# Manutencao

## Debug

### Investigar bug

Antes de corrigir o codigo, investigar:

- qual e o sintoma;
- qual e a causa provavel;
- quais hipoteses existem;
- como reproduzir;
- onde colocar logs;
- onde colocar breakpoint;
- quais dados verificar;
- quais arquivos podem estar envolvidos;
- quais mudancas recentes podem ter causado o problema.

Depois montar um plano de investigacao passo a passo.

### Corrigir bug com seguranca

Antes de corrigir um bug, explicar:

- causa raiz;
- por que o bug acontece;
- qual e a correcao minima;
- qual e a correcao ideal;
- risco da correcao;
- impactos colaterais;
- testes necessarios;
- como evitar regressao.

## Performance

Ao fazer analise de performance, verificar:

- complexidade Big O;
- loops caros;
- chamadas duplicadas;
- consultas repetidas;
- N+1;
- cache;
- memoria;
- renderizacoes desnecessarias;
- gargalos de rede;
- gargalos de banco;
- concorrencia;
- escalabilidade.

Explicar onde pode ficar lento e como melhorar.

## Testes

Ao montar um plano de testes, incluir:

- testes unitarios;
- testes de integracao;
- testes manuais;
- casos felizes;
- casos de erro;
- casos extremos;
- validacoes;
- permissoes;
- performance;
- seguranca;
- regressao.

Para cada teste, registrar:

- cenario;
- entrada;
- acao;
- resultado esperado.

## Seguranca

Ao fazer revisao de seguranca, verificar:

- autenticacao;
- autorizacao;
- JWT;
- roles e claims;
- SQL Injection;
- XSS;
- CSRF;
- CORS;
- exposicao de dados sensiveis;
- logs com informacao sensivel;
- validacao de entrada;
- upload de arquivos;
- rate limiting;
- secrets;
- criptografia;
- permissoes.

Explicar riscos e correcoes recomendadas.
