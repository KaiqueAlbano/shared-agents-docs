# Estrutura do Projeto

## Estrutura obrigatoria

Todo desenvolvimento deve manter a seguinte estrutura padrao, aplicavel para projetos com React, Flutter e stacks equivalentes.

```txt
meu-projeto/
|
|-- front/
|   |-- src/
|   |   |-- assets/
|   |   |-- components/
|   |   |   |-- ui/
|   |   |   |-- layout/
|   |   |   `-- shared/
|   |   |-- hooks/
|   |   |-- routes/
|   |   |-- services/
|   |   |-- pages/
|   |   |-- styles/
|   |   |-- context/
|   |   |-- utils/
|   |   |-- constants/
|   |   |-- App.jsx
|   |   `-- main.jsx
|   |-- public/
|   |-- package.json
|   `-- .env
|
|-- mobile/
|   |-- lib/
|   |   |-- core/
|   |   |-- pages/
|   |   |-- widgets/
|   |   |-- services/
|   |   |-- models/
|   |   `-- main.dart
|   |-- test/
|   |-- pubspec.yaml
|   `-- .env
|
|-- api/
|   |-- src/
|   |   |-- controllers/
|   |   |-- routes/
|   |   |-- services/
|   |   |-- repositories/
|   |   |-- middlewares/
|   |   |-- config/
|   |   |-- utils/
|   |   `-- app.js
|   |-- package.json
|   `-- .env
|
|-- .db/
|   |-- <schema1>/
|   |   |-- tables/
|   |   |-- procedures/
|   |   |-- views/
|   |   |-- functions/
|   |   |-- seeds/
|   |   `-- migrations/
|   |-- <schema2>/
|   |   `-- ...
|
|-- scripts/
|   |-- deploy.sh
|   |-- backup-db.sql
|   `-- restore-db.sql
|
|-- agents.md
|-- .gitignore
`-- docker-compose.yml
```

## Regras para a pasta `.db`

- Todos os objetos do banco devem ficar em `.db/<schema>/...`.
- Cada objeto deve ter seu proprio arquivo com nome claro, por exemplo `users.table.sql` ou `create_user_function.sql`.
- Nao espalhar SQL fora da pasta `.db`.

## Regras gerais do projeto

- Nunca criar arquivos fora da estrutura definida sem necessidade tecnica real.
- Nao criar novas pastas sem justificativa tecnica.
- Nao duplicar codigo.
- Nao criar logica repetida.
- Manter o projeto organizado, escalavel e de facil manutencao.
- Remover codigo morto e dependencias nao utilizadas.
- Nao alterar funcionalidades existentes sem demanda explicita.

Prioridades: organizacao, manutencao, responsividade, escalabilidade, seguranca e performance.

## Arquitetura obrigatoria

Frontend:
- Componentes em `components/`.
- Hooks em `hooks/`.
- Rotas em `routes/`.
- Comunicacao com API em `services/`.
- Telas em `pages/`.

Mobile Flutter:
- Widgets em `widgets/`.
- Telas em `pages/`.
- Servicos em `services/`.
- Modelos em `models/`.
- Configuracoes compartilhadas em `core/`.

Backend:
- Separar `controllers`, `services`, `repositories`, `routes`, `middlewares` e `config`.

Banco:
- Usar exclusivamente `.db/` por schema para todo SQL.

## Regras para alteracao de objetos SQL

Antes de alterar qualquer `procedure`, `view`, `function` ou `table`:

1. Buscar o objeto no banco correspondente ao contexto.
2. Trazer apenas os objetos envolvidos na mudanca.
3. Comparar a versao local com a versao do banco e atualizar a copia local se necessario.
4. Evitar sobrescrever alteracoes de outros desenvolvedores.

## Seguranca, qualidade e nao regressao

- Nunca expor senhas ou tokens no codigo.
- Usar variaveis de ambiente.
- Validar todas as entradas da API.
- Antes de concluir, revisar imports nao usados, arquivos nao usados, codigo duplicado, responsividade, tratamento de erros e mensagens ao usuario.

## Publicacao

- E proibido executar `commit`, `push`, `release`, `deploy` ou acesso SSH para publicacao sem autorizacao explicita do solicitante.

## Checklist obrigatorio antes de finalizar alteracoes

1. Consultei o `agents.md`.
2. Mantive a estrutura oficial de pastas.
3. Evitei duplicacao de codigo.
4. Nao quebrei funcionalidades existentes.
5. Validei responsividade em diferentes tamanhos.
6. Mantive dados individuais por usuario quando aplicavel.
7. Respeitei balanceamento e regras de negocio.
8. Evitei repetir itens na mesma sessao.
9. Validei impactos em banco, API, front e documentacao.
10. Nao publiquei nada sem autorizacao explicita.
