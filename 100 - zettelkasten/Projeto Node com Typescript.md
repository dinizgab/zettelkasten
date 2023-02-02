02-02-2023 - 13:48
Status: #idea
Tags: [[ideas]]

# Iniciando um projeto Node com Typescript

Essa nota tem o objetivo de me lembrar como utilizar e inicializar um projeto node para API com [[GraphQL]] e [[REST APIs|REST]] utilizando Typescript.

## Projeto Node comum
``` bash
npm init -y
npm i typescript ts-node nodemon
npx tsc --init  // Iniciando o tsconfig.json
```

## Projeto GraphQL
```bash
npm init -y
npm i -D typescript ts-node nodemon // Instalando o Typescript
npm i type-graphql graphql apollo-server class-validator reflect-metadata // Instalando o GraphQL
```

Depois de iniciar o projeto e instalar as dependências, voce precisa colocar o script npm para rodar o servidor.
``` json
{
"scripts": {
	"dev": "tsx watch ./src/server.ts",  // Path para o servidor
}
}
```