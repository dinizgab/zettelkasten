22-03-2023 - 10:48
Status: #idea
Tags: [[ideas]]

# Testes de software

Anotações sobre testes de software e conceitos necessários para aprender sobre teste e validação de software

**Driver** = A classe ou método que está recebendo os dados para ser testada;

**Stub** =  Um método "burro", ele serve só para retornar um valor necessário para criar e continuar com os testes da classe driver;
- Quando o **Driver** está nas camadas (arquitetura de camadas) mais superiores da aplicação nós precisamos simular as camadas mais inferiores para que a gente consiga testar todo o sistema. Então, nós usamos os **Stubs** para simular esses métodos inferiores necessários;
- Talvez o **Mock** seja mais eficiente do que o **Stub**, porque nós não precisamos criar o método e o retorno do método para testar;

```java
public int somador(int a, int b) {
	return a + b;
}

public int somadorStub() {
	return 30;
}
```
- Um exemplo de um **Stub** no snippet de cima, o segundo método só simula o resultado da soma do primeiro método;


**Mock** = Presets de informações e dados, servem para definir expectativas do que precisamos e para os testes que estamos fazendo (Ex.: retorno de um json);


---
# Referências