Status: #concepts
Tags: [[Concepts]] [[GraphQL]]

# Query

As Queries no GraphQL são as requisições que nós fazemos para recuperar valores do servidor, seria equivalente aos endpoints do método GET no padrão [[REST APIs|Rest]].

Elas são declaradas sempre dentro dos resolvers do servidor (Mostrando mais uma vez que seria uma espécie de endpoint).
-- Tudo tá fazendo mais sentido agora

Nós podemos declarar um tipo com as queries que nós queremos ter na nossa aplicação e determinar o seu nome e seu retorno. Deixando o código mais limpo e fácil de se ler.
```js
type Query {
	hello: String
	users: [User!]!
}

type User {
	_id: ID!
	name: String!
	email: String!
	active: Boolean!
}
```
- Nesse exemplo, tem um tipo Query, que dentro dele têm 2 campos que são queries que teremos na nossa aplicação, o primeiro, `hello`, é uma query que retorna uma string e o segundo, `users`, retorna um array de usuários.
---
```js
const resolvers = {
	Query {
		hello: () => "Hello World!"
		users: () => [
			{_id: 1, name: "Gabriel", email: "gabrieldiniz@gmail.com", active: false },
			{_id: 2, name: "Marcos", email: "marcos123@gmail.com", active: true }
		]
	}
}
```
- Isso é um exemplo de declaração de uma Query já dentro do `resolver` e utilizando o tipo `Query` para criar ela dentro do resolver;
- Dá pra perceber que dentro do resolver nós colocamos exatamente o que aquele "endpoint" vai retornar quando nós batermos nele;

Depois de declarar a `Query` dentro do `resolver`, nós podemos escolar exatamente o que queremos daquela `Query` quando formos chamar aquele endpoint.
- Podemos retornar apenas o nome do usuário ou apenas o email e etc.

# Referências

- Curso GraphQL
https://www.youtube.com/watch?v=iUYabIGhJYk