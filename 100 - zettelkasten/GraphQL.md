01-02-2023 - 14:48
Status: #idea
Tags: [[ideas]]

# GraphQL

Uma ideia pra eu escrever o que eu for aprendendo sobre GraphQL e talvez linkando com [[REST APIs]].

- **[[Projeto Node com Typescript|Como iniciar um projeto GraphQL com typescript]]**

O GraphQL é uma alternativa para o padrão RESTful, ou seja, é uma maneira de fazer requisições para o sistema (Query Language), sendo de leitura ou escrita, se tornando uma maneira mais prática de criar essas requisições, já que não depende de nenhuma tecnologia específica usada no seu sistema e pelo falo de só precisar dizer o que nós precisamos.

O GraphQL resolve o problema de OverFetching e de UnderFetching, ja que so temos um endpoint com todas as informacoes que nos precisamos e enviamos uma query dizendo apenas o que nos precisamos do BD.

As requisições possuem 2 tipos, são as Queries e as Mutations.
	- [[Query]] -> Usadas para recuperação de dados (GET);
	- [[Mutation]] -> Usadas para a manipulação de dados (POST, PATCH, PUT e DELETE)
- E elas podem ser declaradas dentro de um Type para mostrar o que elas retornam (Usar o Type como uma Interface) e declaradas depois dentro dos `resolvers` da aplicação; 

No GraphQL, existem 5 tipos primitivos, `String, Int, Boolean, Float e ID`, em que o ID é um tipo especial do GraphQL que determina a chave primaria do objeto que você tá declarando no tipo.

# Referências

Documentação oficial:
- https://graphql.org/learn/

Vídeo Rockeseat:
- https://youtu.be/6SZOPKs9SUg?t=293