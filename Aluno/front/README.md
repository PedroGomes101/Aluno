# Frontend — Aluno (Nuxt 3)

Aplicação frontend construída com Nuxt 3 (Vue 3).

## Pré-requisitos

- Node.js (recomendo Node 18 ou 20)
- npm

Verifique com (PowerShell):

```powershell
node -v
npm -v
```

## Instalação (na pasta `front`)

Abra um PowerShell na pasta `front` e instale dependências:

```powershell
cd 'c:\Users\Pedro\Documents\Programas\Aluno_TS\Aluno\front'
npm install
```

## Rodar em desenvolvimento

```powershell
npm run dev
```

Por padrão o Nuxt irá rodar em `http://localhost:3000` (a URL exata aparece no console). Se o frontend precisa acessar a API do backend, ajuste a URL base para `http://localhost:3002` conforme necessário no código fonte ou via variável de ambiente.

## Build e preview

Construir para produção:

```powershell
npm run build
npm run preview
```

## Observações

- O código do frontend está em `front/pages` e `front/app.vue`.
- Se houver problemas relacionados à versão do Node, atualize para a versão compatível com Nuxt 3.

## Troubleshooting rápido

- Erro ao iniciar: verifique `npm install` e a versão do Node.
- Se o front não conseguir chamar a API, confirme que o backend está rodando em `http://localhost:3002`.# Front-end Nuxt

Este projeto utiliza Nuxt.js para o front-end.

## Como rodar o projeto

Agora, para rodar o front-end e o back-end juntos, basta executar na raiz do projeto:

```sh
npm install
npm run dev
```

Isso irá iniciar tanto o back-end quanto o front-end simultaneamente.

## Estrutura
- O código-fonte do front-end está nesta pasta.
- O código-fonte do back-end está em `../../back`.

## Observações
- A pasta `backup` foi removida, pois continha arquivos antigos e não é mais necessária.
