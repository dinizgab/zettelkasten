02-02-2023 - 11:44
Status: #idea
Tags: [[ideas]]

# Branches

O conceito de branche e basicamente uma copia do repositorio que voce esta editando para deixar a branche (repo) principal segura de qualquer besteira que for feita nessa outra branch, e uma maneira de isolar o ambiente de producao de eventuais problemas e erros

Na maioria das vezes, branches sao usadas para implementar novas fixes, releases e ate features dentro do projeto, evitando problemas na branch master.

Um bom exemplo de uso real das branches, e justamente o que ta na documentacao oficial do git (Primeiro link nas referencias). La, ele te da um exemplo de uma nova feature no projeto, entao voce vai la e cria uma branch pra a feature, mas enquanto isso, aparece uma hotfix urgente, entao voce volta pra a branch master e faz outra branch para a hotfix, conserta a hotfix e faz merge na master e depois volta para a branch da feature. Assim, a branch master sempre ficara 

# Referências

- Doc oficial  (Artigo de branches)
https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging

- The coding train
https://www.youtube.com/watch?v=oPpnCh7InLY