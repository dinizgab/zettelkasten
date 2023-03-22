20-03-2023 - 08:44
Status: #idea
Tags: [[ideas]] [[Testes de software]]

# PSOFT - Projeto

O projeto de exemplo dessa cadeira foi um sistema de um mercado, com produtos e lotes.

Produto:
- ID;
- Nome;
- Fabricante;
- Preço;

Lote:
- Produto (Que será a referência daquele lote, Lote de Cerveja, Lote de Caneta, etc);
- Data de validade;
- Quantidade de produtos;

O cliente não deve acessar informações mais específicas do sistema, tipo as informações dos produtos, lotes e etc. Para evitar isso a gente pode criar uma classe de fachada ou controller, onde eu poderia chamar `prodFacade.create()` e a classe `prodFacade` seria a responsável por criar esse novo produto. Assim, teria um nível mais profundo de segurança e ocultação de informação.

Para deixar mais seguro ainda nós poderiamos criar uma classe Facade e uma classe Service, onde o Cliente acessaria o Facade e o Facade acessaria o Service, onde aí sim o Produto seria criado. Com isso, as informações do Produto estariam disponíveis apenas para a classe Service, que seria a responsável por criar, acessar, atualizar e deletar produtos.
`Cliente -> Facade -> Service (Produto criado nessa classe)`

Além disso, ainda precisaria de uma classe para armazenar os Produtos, uma classe `Repository` que seria chamada pela classe `Service` (Padrão de camadas). A diferença entre o Repository e o Service é que o Repository apenas faz o CRUD dos objetos, enquanto toda a lógica está dentro do Service
`Cliente -> Facade -> Service -> Repository`


---
# Referências