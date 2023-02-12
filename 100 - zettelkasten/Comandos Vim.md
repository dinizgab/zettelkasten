12-02-2023 - 15:41
Status: #idea
Tags: [[ideas]]

# Comandos Vim

Nessa nota eu vou botar alguns comandos do [[Vim]] que eu fui aprendendo e que eu preciso decorar, a intencão aqui é de usar essa nota como uma maneira de revisar o que eu esqueci ou aprender coisas novas.

`h, j, k, l` = Os mais básicos, para movimentar o cursor;
`w, e`  = `w` move o cursor pra o inicio da próxima palavra e `e` para o fim
`W, E` = As mesmas coisas do de cima, mas ignoram os espaços e pontuações das entre as palavras 

`:w e :wq` = Salvam o arquivo que euu tô editando (`:wq` sai e salva);
`:q e :q!` = Saem do Vim sem salvar (`:q!` é a saída forçada);

`x` = Deleta apenas o digito que p cursor está;
`dd` = Deleta toda a linha que o cursor está;
`idk` = Deleta i linhas para cima do cursor;
`idj` = Deleta i linhas para baixo do cursor;
`daw e caw` = Os 2 deletam a palavra que o cursor está, mas o `caw` coloca no modo de inserção;
**Obs: Tudo o que foi deletado vai para o `Ctrl-v` ou `p`, no fim eles são meio que um recorte (`Ctrl-x`)**

`v` = Entra no modo visual;
`y e p` = `y` é o Ctrl-c e `p` o Ctrl-v (Mas para copiar tem que tá no modo Visual);

`u` = É o Ctrl-z do Vim;
`Ctrl-r` = É o Ctrl-y (Desfaz o que o de cima fez);

`Ctrl-t` = Cria um novo arquivo;
`Ctrl-h` = Troca para o arquivo à esquerda do atual;
`Ctrl-l` = Troca para a direita;

`\n` = Troca o foco do editor para o NERDTree (Cria uma se não existir uma aberta);
`Ctrl-f` = Abre o NERDTree no arquivo que eu tô editando no momento;
`Ctrl-n` = Abre e fecha o NERDTree



---