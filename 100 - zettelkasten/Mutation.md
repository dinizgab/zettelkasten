Status: #ideas
Tags: [[GraphQL]] [[Query]]

# Mutation

É a requisição do GraphQL que é equivalente aos métodos POST, PUT, PATCH e DELETE dentro do padrão [[REST APIs|Rest]] e funcionam muito parecidos com as [[Query|Queries]], porem elas provavelmente terão payloads dentro delas (Informações para a alteração do objeto no BD)

Nós podemos declarar elas dentro de um tipo do mesmo jeito das Queries
```js
type Mutation {
	createUser(name: String, age: Int)
}

type User {
	_id: ID!
	name: String!
	email: String!
	active: Boolean!
}
```

Esse é um exemplo de uma Mutation declarada dentro de um tipo (Talvez com typescript seja diferente), e depois nós podemos declarar o que ela fará dentro dos resolvers

```js
const resolvers = {
	Mutation {
		createUser(_, args) => {
			prisma.users.create({
				data: {
					name: args.name,
					age: args.age
				}
			})
	}}
}
```

Esse é um exemplo de criação de um novo usuário em um BD usando prisma e mutations, declarando a mutation createUser dentro do resolver (Provavelmente dá pra botar essa função dentro de um arquivo separado assim como a gente faz com os Controllers)

# Referências

- Curso GraphQL
https://www.youtube.com/watch?v=iUYabIGhJYk