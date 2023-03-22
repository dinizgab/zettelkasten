27-01-2023 - 14:22
Status: #idea
Tags: [[ideas]]

# Context API

O contexto no React é uma maneira de mantar um estado universal na sua aplicação, assim, a gente não precisa ficar passando um estado que surgiu em um componente muito antigo de filho em filho até chegar no componente que a gente quer.

![[context_api|800|center]] 

**No primeiro caso, tem um exemplo de uma aplicação que não tá usando o contexto e no segundo caso uma que tá usando.**

No primeiro caso tem um problema, onde os 2 componenetes descendentes do componente 1 precisam da propriedade `nome`. Então, sem usar contexto, nós precisariamos fazer uma "corrente" entre os 3 componentes, passando o `nome` do componente 1 para o 2 e do 2 para o 3.

Já o segundo caso, é um exemplo gráfico de como usar um contexto, tem um [[Context Provider]] para o contexto, e a partir dele, os componentes acessarão a propriedade nome, nesse caso, o Componente 1 apenas seta o valor de `nome` e os proximos componentes só precisam usar o hook useContext e ter acesso a esse estado

(Acredito que o Redux faz um trabalho parecido ou até o mesmo trabalho do )

---
# Referências
https://www.youtube.com/watch?v=H6bCSzxxiNc