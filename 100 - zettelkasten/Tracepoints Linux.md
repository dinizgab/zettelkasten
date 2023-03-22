09-03-2023 - 14:23
Status: #idea
Tags: [[ideas]]

# Tracepoints Linux

Tracepoints são uma parada meio complexa de se explicar, mas são parecidos com funções de callbacks do JS, mas funcionando no nível do kernel do linux, mas ainda assim são diferentes dos callbacks. Eles são maneiras de capturar eventos ou executar funções quando esses eventos acontecem, e essas funções são chamadas de probes.

O tracepoint pode estar "ligado" ou "desligado". Quando ele está ligado, é porque tem uma função que eu criei que será chamada todas as vezes que ele for executado, quando está desligado é porque não temos essa função, mas também não gera nenhuma diferença na execução das funções do kernel, só um pequeno tempo que será perdido quando for checar a condição para executar a função e um pequeno gasto de memória, mas não é nada demais.


---
# Referências

https://www.kernel.org/doc/html/latest/trace/tracepoints.html