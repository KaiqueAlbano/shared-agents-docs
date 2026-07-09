# Documentacao para Uso

## Objetivo

Este arquivo explica como reutilizar esta documentacao em mais de um projeto sem copiar os arquivos manualmente.

## Modelo recomendado

O modelo ideal e manter esta documentacao em um repositorio central e consumir esse repositorio nos projetos por meio de `git submodule`.

Exemplo:

- repositorio central: `shared-agents-docs`
- pasta consumida no projeto: `docs-shared`

## Estrutura sugerida

Repositorio central:

```txt
shared-agents-docs/
|-- agents.md
|-- estrutura.md
|-- manutencao.md
|-- react.md
|-- csharp.md
|-- python.md
|-- flutter.md
|-- sqlserver.md
`-- postgresql.md
```

Projeto consumidor:

```txt
meu-projeto/
|-- docs-shared/
|-- agents.md
`-- restante do projeto
```

## Passo a passo com git submodule

### 1. Criar o repositorio central

Crie um repositorio dedicado para os arquivos compartilhados de documentacao.

Exemplo:

```powershell
git init shared-agents-docs
```

Depois adicione os arquivos padrao e publique esse repositorio no servidor Git da equipe.

### 2. Adicionar o submodule no projeto

Dentro do projeto que vai consumir a documentacao, execute:

```powershell
git submodule add <URL_DO_REPOSITORIO> docs-shared
```

Exemplo:

```powershell
git submodule add https://github.com/sua-org/shared-agents-docs.git docs-shared
```

Esse comando cria:

- a pasta `docs-shared/`
- o arquivo `.gitmodules`

### 3. Criar o `agents.md` local do projeto

No projeto principal, mantenha um `agents.md` local apenas com as referencias para a documentacao compartilhada e para os arquivos especificos daquele projeto. Arquivos como `regrasnegocio.md` e `arquitetura-local.md` sao opcionais e devem existir somente quando fizerem sentido para aquele repositorio.

Exemplo:

```md
# agents.md

Leia nesta ordem:

1. `docs-shared/estrutura.md`
2. `docs-shared/manutencao.md`
3. `docs-shared/react.md` ou outro arquivo da stack usada
4. `regrasnegocio.md`
5. `arquitetura-local.md`

Regras:
- `docs-shared/` define o padrao global.
- Os arquivos locais definem contexto especifico do projeto.
- Em caso de conflito, a regra local do projeto prevalece apenas neste repositorio.
```

### 4. Commitar a referencia do submodule

Depois de adicionar o submodule, registre a configuracao no projeto:

```powershell
git add .gitmodules docs-shared
git commit -m "Adiciona documentacao compartilhada"
```

### 5. Clonar um projeto que usa submodule

Ao clonar um projeto novo, use:

```powershell
git clone --recurse-submodules <URL_DO_PROJETO>
```

Se o projeto ja foi clonado sem o submodule:

```powershell
git submodule update --init --recursive
```

### 6. Atualizar a documentacao compartilhada no projeto

Para apontar o projeto para a versao mais recente da documentacao:

```powershell
cd docs-shared
git pull origin main
cd ..
git add docs-shared
git commit -m "Atualiza documentacao compartilhada"
```

### 7. Alterar a documentacao central

Quando precisar mudar o padrao geral:

```powershell
cd docs-shared
git checkout main
git pull
```

Depois edite os arquivos, grave a mudanca e publique:

```powershell
git add .
git commit -m "Ajusta documentacao padrao"
git push
```

Por fim, volte ao projeto principal e atualize a referencia:

```powershell
cd ..
git add docs-shared
git commit -m "Aponta para nova versao da documentacao"
```

## Regras de precedencia

Use esta ordem de prioridade:

1. `agents.md` local do projeto
2. arquivos locais, como `regrasnegocio.md` e `arquitetura-local.md`
3. arquivos compartilhados em `docs-shared/`

## Boas praticas

- Nao duplicar os arquivos compartilhados manualmente em cada repositorio.
- Manter o `agents.md` local pequeno e objetivo.
- Centralizar apenas regras globais.
- Deixar regras de dominio no projeto consumidor.
- Atualizar o submodule de forma consciente, para evitar surpresa entre projetos.
