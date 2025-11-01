# Backend — Aluno (Node + TypeScript + Express + SQLite)

> API simples para gerenciar alunos (lista, criar, atualizar, buscar por matrícula e excluir).

## Pré-requisitos

- Node.js (recomendo Node 18 ou 20)
- npm (vem com Node)

Verifique com (PowerShell):

```powershell
node -v
npm -v
```

## Instalação (na pasta `back`)

Abra um PowerShell na pasta `back` e instale dependências:

```powershell
cd 'c:\Users\Pedro\Documents\Programas\Aluno_TS\Aluno\back'
npm install
```

Se quiser instalar as dependências de desenvolvimento (útil para rodar o TypeScript diretamente):

```powershell
npm install -D typescript ts-node-dev @types/express @types/cors @types/node
```

## Rodar em desenvolvimento

Use `ts-node-dev` para reinício automático ao alterar arquivos:

```powershell
npx ts-node-dev --respawn --transpile-only src/api/routes.ts
```

O servidor por padrão escuta na porta `3002`. Você verá no console algo como:

```
Servidor no ar..., na porta: 3002
```

Para alterar a porta temporariamente (PowerShell):

```powershell
$env:PORT=3003; npx ts-node-dev --respawn --transpile-only src/api/routes.ts
```

## Build e execução em produção

Compile e execute o código gerado em `dist`:

```powershell
npx tsc
node dist/api/routes.js
```

## Banco de dados

O backend usa SQLite e cria o arquivo `database.sqlite` na raiz da pasta `back` automaticamente.

## Endpoints principais

- GET /alunos — listar todos os alunos
- POST /alunos — criar novo aluno (body JSON: `{ "nome": "x", "turma": "y" }`)
- PUT /alunos/:matricula — atualizar aluno
- GET /alunos/matricula/:matricula — buscar por matrícula
- DELETE /alunos/:matricula — excluir

Exemplo de chamada com curl:

```powershell
curl http://localhost:3002/alunos
```

## Problemas comuns

- Erro "Cannot find module 'express'": rode `npm install` na pasta `back`.
- Erros de TypeScript em tempo de execução: em dev use `--transpile-only` com `ts-node-dev`.
- Permissões/arquivo do SQLite: verifique se o processo tem permissão para criar `database.sqlite` na pasta `back`.

## Observações

O arquivo principal que inicia o servidor é `src/api/routes.ts`.
