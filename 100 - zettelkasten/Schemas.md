17-02-2023 - 19:15
Status: #idea
Tags: [[ideas]]

# Schemas

Schemas são maneiras que o mongo usa, para modelar os dados antes de salvar eles no banco, basicamente nele você define os atributos e métodos que aquele objeto terá.

Geralmente a gente define esses modelos dentro de uma pasta  `models` (:O), é dentro dela que vai ter todo o "esqueleto" dos objetos que serão guardados no BD.
```ts
/models/User.ts

interface UserInterface {
	name: string,
	age: number,
	createdAt: Date,
	posts: Types.ObjectId[]
}

const UserSchema = new Schema<UserInterface>({
	name: String,
	age: Number,
	createdAt: Date,
	posts: [SchemaTypes.ObjectId],
})

```

Nesse snippet eu to basicamente modelando um novo tipo que será salvo dentro do banco de dados, o `User`, que implementa a interface `UserInterface` (por segurança e confiabilidade de código, já que caso se falte algum dos campos da interface no schema ele vai dar erro e nem compilar).

Esse Usuário tem um id que será uma string única, um nome que é uma string, idade que é um número, a data que foi criado e uma lista de posts, que tem um tipo diferenciado, porque é desse jeito que se modela as relações dentro do mongoDB, na tradução livre isso seria uma lista de IDs que referenciam outros objetos dentro do banco de dados.

**ObjectId é um id especial que o mongo cria para definir unicamente cada objeto, então não precisamos de um id criado para nenhum dos modelos**

Post também terá seu próprio schema e id únicos, mas também terá um atributo `author`, que seria o ID do seu usuário autor.
```ts
/models/Post.ts

interface PostInterface {
	author: Types.ObjectId,
	title: string,
	createdAt: Date
}

const PostSchema = new Schema<PostInterface>({
	author: SchemaTypes.ObjectId,
	title: String,
	createdAt: Date,
})
```

Depois de criar o schema, a gente precisa converter ele pra um modelo no banco de dados, que seria uma espécie de tabela, pra fazer isso a gente pode usar o método `model` do mongoose.
```ts
export const Users = mongoose.model("Users", UserSchema);
export const Posts = mongoose.model("Posts", PostSchema);
```

---
# Referências

Doc oficial mongoose:
https://mongoosejs.com/docs/4.x/docs/guide.html