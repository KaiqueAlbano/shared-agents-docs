# Documentacao para Uso

## Objetivo

Este arquivo mostra o jeito mais simples de usar `shared-agents-docs` em outros projetos.

`arquitetura.md` e `manutencao.md` sao obrigatorios em qualquer projeto que usar `shared-agents-docs`.

## Passo a passo

### 1. Entrar no projeto

```powershell
cd C:\caminho\do\meu-projeto
```

### 2. Adicionar a documentacao compartilhada

```powershell
git submodule add https://github.com/KaiqueAlbano/shared-agents-docs.git docs-shared
```

### 3. Criar o `agents.md` local

Copie o conteudo de `agents-local.md` deste repositorio e cole no `agents.md` da raiz do projeto local.

### 4. Salvar no projeto

```powershell
git add .gitmodules docs-shared agents.md
git commit -m "Adiciona shared-agents-docs ao projeto"
```

## Se quiser atualizar depois

```powershell
cd docs-shared
git pull origin main
cd ..
git add docs-shared
git commit -m "Atualiza shared-agents-docs"
```
