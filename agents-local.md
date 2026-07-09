# AGENTS

Este arquivo e o orquestrador local do projeto.

Ele aponta para a documentacao compartilhada em `docs-shared/` e para os arquivos locais deste repositorio.

`docs-shared/arquitetura.md` e `docs-shared/manutencao.md` sao obrigatorios em qualquer projeto que consumir esta documentacao.

Ele nao precisa ler todos os arquivos de `docs-shared`; deve ler obrigatoriamente a base comum e depois o arquivo da stack usada no projeto.

Leia nesta ordem:

1. `docs-shared/arquitetura.md`
2. `docs-shared/manutencao.md`
3. `regras-negocio.md`
4. arquivo da stack usada em `docs-shared/`
5. arquivos locais do projeto, quando existirem

Regras:

- `docs-shared/arquitetura.md` e `docs-shared/manutencao.md` sao obrigatorios.
- `regras-negocio.md` e obrigatorio neste repositorio.
- `docs-shared/` define o padrao global.
- Os arquivos locais do projeto definem contexto especifico.
- Em caso de conflito, a regra local prevalece neste repositorio.

```

Arquivos compartilhados disponiveis em `docs-shared/`:

- `arquitetura.md`
- `manutencao.md`
- `react.md`
- `csharp.md`
- `python.md`
- `flutter.md`
- `sqlserver.md`
- `postgresql.md`
- `documentacao-para-uso.md`
```
