17-02-2023 - 18:12
Status: #idea
Tags: [[ideas]]

# MongoDB

Mongo é um banco de dados não relacional, diferente dos SQL based, ou seja, não é baseado em tabelas como eles, ele utiliza uma metodologia de modelagem de dados baseada em objetos, então se dá bem com linguagens que possuem orientação a objetos como JS e Java (mas tudo é um tradeoff, então tem coisas boas em usá-lo e coisas ruins, que você teria mais facilidade em um SQL).

Nessa nota eu vou escrever snippets e conceitos sobre Mongo que eu for aprendendo, pra poder voltar aqui no futuro e rever, do mesmo jeito que eu fiz com o Context API.

Pra conectar o mongo em uma aplicação fastify (framework que eu to usando), precisa do mongoose (que na verdade vai precisar dele pra fazer tudo no app)

```bash
npm i mongoose
```

E a configuração do banco pode ser feita ou localmente, com o mongo rodando num container ou no próprio pc, ou no atlas.

```ts
const connectDB = (connectionURL: string) => {
	mongoose.connect(connectionURL, {// Aqui ficam as opções de conexão})
	mongoose.connection.on("error", (error) => {
		console.log(error
		process.exit()
	)})
}}
```

Então é só chamar essa função no momento que for rodar a API (ideal que seja antes, pra poder recuperar toda a informação salva no BD antes de rodar a API).

É melhor ir separando em várias notas os conceitos pra deixar mais organizado, então vou deixar listado aqui abaixo os conceitos:
- [[Schemas]]
- 

---
# Referências