# Roteiro de entrevista

## Introdução [3 min]

- Como você entrou na área de desenvolvimento?

## Conceitos [15 min]

### Orientação a objetos

- O que é orientação a objetos?
  - [R]: É um paradigma de programação que permite a criação de objetos que possuem atributos e comportamentos.

- Quais são os pilares da OO?
  - [R]: Abstração, Encapsulamento, Herança e Polimorfismo

- Qual é a deferença de uma interface e uma classe abstração?
  - [R]: Uma interface é um contrato que define o que uma classe deve fazer, enquanto uma classe abstrata é uma classe que não pode ser instanciada, mas pode ser herdada.

- O que é um método abstrato?
  - [R]: um método que não tem implementação

### Clean Code

- O que é um código limpo?
  - [R]: É um código que segue as boas práticas de programação, como nomes significativos, funções pequenas, comentários, formatação e estrutura de código.

- Quais são as 5 regras do clean code?
  - [R]: 1. Nomes significativos
        EX: `int d;` é ruim, `int elapsedTimeInDays;` é bom
  - [R]: 2. Funções pequenas
  - [R]: 3. Evitar uso de Comentários
  - [R]: 4. Formatação
  - [R]: 5. Estrutura de código

- O que é um código legado?
  - [R]: É um código que não segue as boas práticas de programação, como nomes sem significado, funções grandes, comentários desnecessários, formatação e estrutura de código.

- O que é um código morto?
  - [R]: É um código que não é utilizado, mas não foi removido.

### Refactoring

- O que é refactoring?
  - [R]: É uma técnica de melhoria de código que visa melhorar a estrutura e a legibilidade do código sem alterar seu comportamento.

- Quais são os benefícios do refactoring?
  - [R]: 1. Melhora a legibilidade do código
            2. Melhora a manutenibilidade do código
            3. Melhora a performance do código
            4. Melhora a qualidade do código

- Qual é a melhor forma de refatorar um código?
  - [R]: Refatorar um código é uma tarefa que deve ser feita com calma, pois qualquer erro pode causar um bug no código. Por isso, é importante fazer testes unitários e testes de integração para garantir que o código não foi quebrado.

### TDD

- O que é TDD?
  - [R]: É uma técnica de desenvolvimento de software que visa escrever testes antes de escrever o código.

- Quais são os passos do TDD?
  - [R]: ```
        1. Escrever um teste
        2. Executar o teste e ver se ele falha
        3. Escrever o código
        4. Executar o teste e ver se ele passa
        5. Refatorar o código 

### SOLID

- [S] Qual é o princípio de responsabilidade única?
  - [R] Uma classe deve ter apenas uma responsabilidade e essa responsabilidade deve ser totalmente encapsulada pela classe.

- [O] Qual é o princípio de aberto/fechado?
  - [R] Entidades de software (classes, módulos, funções, etc.) devem estar abertas para extensão, mas fechadas para modificação.

- [L] Qual é o princípio de substituição de Liskov?
  - [R] Se S é um subtipo de T, então objetos do tipo T podem ser substituídos por objetos do tipo S (ou seja, objetos do tipo S podem substituir objetos do tipo T) sem quebrar o programa (ou seja, sem que o comportamento do programa mude).

- [I] Qual é o princípio de segregação de interfaces?
  - [R] Muitas interfaces específicas são melhores do que uma interface única.

- [D] Qual é o princípio de inversão de dependência?
  - [R] Dependa de uma abstração e não de uma implementação.

### Design Patterns

- O que é um design pattern?
  - [R]: É uma solução para um problema recorrente em um contexto específico.

- Para que serve um design pattern?
  - [R]: Para resolver um problema recorrente em um contexto específico.

- Qual é o padrão de projeto mais utilizado?
  - [R]: O padrão de projeto mais utilizado é o Singleton, que é um padrão de criação que garante que uma classe tenha apenas uma instância e fornece um ponto de acesso global a ela.

- Qual é o padrão de projeto mais complexo?
  - [R]: O padrão de projeto mais complexo é o Composite, que é um padrão estrutural que permite que você componha objetos em estruturas de árvore e trabalhe com essas estruturas como se fossem objetos individuais.

- Qual é o padrão de projeto mais simples?
  - [R]: O padrão de projeto mais simples é o Factory Method, que é um padrão de criação que define uma interface para criar um objeto, mas deixa as subclasses decidirem qual classe instanciar. Factory Method permite que uma classe adie a instanciação para subclasses.

- Quais são a lista de desing patterns?
  - [R]: ```
    1. Singleton
    2. Factory Method
    3. Abstract Factory
    4. Builder
    5. Prototype
    6. Adapter
    7. Bridge
    8. Composite
    9. Decorator
    10. Facade
    11. Flyweight
    12. Proxy
    13. Chain of Responsibility
    14. Command
    15. Interpreter
    16. Iterator
    17. Mediator
    18. Memento
    19. Observer
    20. State
    21. Strategy
    22. Template Method
    23. Visitor

### Clean Architecture

- O que é clean architecture?
  - [R]: É um conjunto de princípios que visa separar a lógica de negócio da lógica de infraestrutura.

- Quais são os sinais de uma arquitetura não limpa?
  - [R]: ```
    1. Código duplicado
    2. Código espaguete
    3. Código difícil de testar
    4. Código difícil de entender
    5. Código difícil de manter
    6. Auto acoplamento
- Quais são os princípios da clean architecture?
  - [R]: ```
    1. Independência de frameworks
    2. Independência de banco de dados
    3. Independência de UI
    4. Testabilidade
- Quais são os níveis da clean architecture?
  - [R]: ```
    1. Entities
        - EX: User, Post, Comment, etc.
    2. Use Cases
        - EX: Login, Cadastro, etc.
    3. Interface Adapters
        - EX: Controllers, Presenters, Gateways, etc.
    4. Frameworks & Drivers
        - EX: Express, TypeORM, Socket.io, CLI, Database, etc.

- O que é Arquitetura Hexagonal?
  - [R]: É uma arquitetura que visa separar a lógica de negócio da lógica de infraestrutura.

### Arquitetura de Software

- O que é arquitetura de software?
  - [R]: É a estrutura de um sistema, ou seja, como as partes do sistema se relacionam entre si.

- Arquitetura de software é o mesmo que design de software?
  - [R]: Não, design de software é a forma como o software é implementado, enquanto a arquitetura de software é a estrutura do software.

- Arquitetura de software é organização de pastas?
  - [R]: Não, organização de pastas é uma parte da arquitetura de software, mas não é a arquitetura de software.

- O que é design de software?
  - [R]: É a forma como o software é implementado.
         EX: MVC, MVP, MVVM, etc.

- O que é um monolito?
  - [R]: É um sistema que possui todas as suas funcionalidades em um único repositório.

- O que é um microserviço?
  - [R]: É um sistema que possui todas as suas funcionalidades em repositórios separados.

- O que é um sistema distribuído?
  - [R]: É um sistema que possui partes que estão em diferentes máquinas.

- O que é um sistema centralizado?
  - [R]: É um sistema que possui todas as suas partes em uma única máquina.

## Perguntas específicas [8 min]

Ver o template de perguntas especificas

- [React Native](TEMPLATE-REACT-NATIVE.md)
- [Swift](src/TEMPLATE-SWIFT.md)
- [.NET](src/TEMPLATE-NET.md)
- [Java](TEMPLATE-JAVA.md)
- [NodeJs](TEMPLATE-NODE.md)
- [Typescript](TEMPLATE-TYPESCRIPT.md)
- [Kotlin](src/TEMPLATE-KOTLIN.md)
- [Flutter](TEMPLATE-FLUTTER.md)
- [React](TEMPLATE-REACT.md)
- [Angular](TEMPLATE-ANGULAR.md)
- [Vue](TEMPLATE-VUE.md)
- [PHP](TEMPLATE-PHP.md)
- [Python](TEMPLATE-PYTHON.md)
- [Serverless](TEMPLATE-SERVERLESS.md)

## Perguntas abertas - motivação a vaga [5 min]

- Por que você quer sair da sua empresa atual?
  - [R]: Porque eu quero trabalhar em uma empresa que me dê mais autonomia e me permita crescer mais rápido.

- O que te motiva a trabalhar na empresa?
  - [R]: A empresa tem um propósito muito legal, que é ajudar as pessoas a se desenvolverem e a crescerem profissionalmente.

- O que te motiva a trabalhar na vaga?
  - [R]: A vaga tem um propósito muito legal, que é ajudar as pessoas a se desenvolverem e a crescerem profissionalmente.
  
## Agradecer e encerrar [1 min]

- Agradecer a oportunidade de participar do processo seletivo.
- Dizer que está ansioso para trabalhar na empresa.
- Dizer que está ansioso para trabalhar na vaga.
