27-01-2023 - 16:20
Status: #idea
Tags: [[ideas]]

# Refresh Token

Basicamente é uma maneira de revalidar o token JWT quando o token expirar ou se tornar inválido.

O `refresh token` será criado no momento em que o usuário criar um novo token JWT (Login/Cadastro) e será enviado para ele como resposta do servidor juntamente com o token JWT, assim, o JWT ficará guardado no estado da aplicação e o `refresh token` em um cookie no cliente, diminuindo as chances de ataques (Cross-Site Scripting e Cross-Site Request Forgery), já uqe o JWT fica salvo na memória enquanto o `refresh token` fica salvo em um cookie.

Essa revalidação é feita no momento em que o Token JWT perde a sua validade ou o usuário dá refresh na página e o token se perde (Meu problema), nesse momento será feita uma chamada para um endpoint específico no servidor com esse `refresh token`  e o servidor retornará um novo JWT válido para aquele usuário.

![[Pasted image 20230127162447.png]]

# Referências

https://www.youtube.com/watch?v=BSHxBJAy-sE
https://www.youtube.com/watch?v=iD49_NIQ-R4
https://www.youtube.com/watch?v=t5iumvSNbgM