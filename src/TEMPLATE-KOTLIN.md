# KOTLIN

- O que é Kotlin?
  - [R]: Kotlin é uma linguagem de programação multiplataforma, orientada a objetos e funcional, desenvolvida pela JetBrains sob a licença Apache 2.0. É compatível com Java, ou seja, o código Kotlin pode ser executado em uma JVM (Java Virtual Machine) sem a necessidade de compilação. O Kotlin é uma linguagem de programação estática, fortemente tipada e concisa, que visa reduzir a quantidade de código escrito sem perder a legibilidade. O Kotlin é uma linguagem de programação que pode ser usada tanto para desenvolvimento backend quanto frontend.

- Qual a diferença entre Kotlin e Java?
  - [R]: A principal diferença entre Kotlin e Java é que o Kotlin é uma linguagem de programação estática, fortemente tipada e concisa, que visa reduzir a quantidade de código escrito sem perder a legibilidade. O Kotlin é uma linguagem de programação que pode ser usada tanto para desenvolvimento backend quanto frontend.

- O que é JUnit?
  - [R]: JUnit é um framework de testes unitários para a linguagem de programação Java.

- Como se cria um teste com JUnit?
  - [R]: Para criar um teste com JUnit, basta criar uma classe com a anotação @Test e adicionar o código do teste dentro do método. Exemplo:

```java
import org.junit.Test;

public class Teste {
    @Test
    public void teste() {
        // código do teste
    }
}
```

- O que é Constraint Layout?
  - [R]: Constraint Layout é um layout que permite criar layouts complexos de maneira simples e intuitiva. Ele permite que você crie layouts hierárquicos, onde um elemento pode ser pai de outro elemento. Além disso, ele permite que você crie layouts com elementos que se sobrepõem, como por exemplo, um TextView sobre um ImageView.

- O que é Koin?
  - [R]: Koin é um framework de injeção de dependências para Kotlin. Ele permite que você injete objetos em classes sem a necessidade de criar um construtor para cada classe que precisa de um objeto.

- Usar Koin fere o SOLID ?
  - [R]: Não. Koin é um framework de injeção de dependências, que permite que você injete objetos em classes sem a necessidade de criar um construtor para cada classe que precisa de um objeto. O SOLID é um conjunto de princípios de programação orientada a objetos que visa facilitar a manutenção de código. O princípio da injeção de dependências é um dos princípios do SOLID, que diz que uma classe não deve ser responsável por criar objetos que ela precisa. O Koin é um framework que permite que você injete objetos em classes sem a necessidade de criar um construtor para cada classe que precisa de um objeto. Portanto, o Koin não fere o princípio da injeção de dependências.

- O que é Retrofit?
  - [R]: Retrofit é uma biblioteca para requisições HTTP para Kotlin e Java. Ele permite que você faça requisições HTTP de maneira simples e intuitiva. Ele também permite que você faça requisições assíncronas.
