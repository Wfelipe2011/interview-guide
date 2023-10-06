# Node

- O que é Node.js?
    
    [R]: Node.js é um ambiente de tempo de execução JavaScript de código aberto que permite aos desenvolvedores executar JavaScript no lado do servidor. Ele é baseado no motor JavaScript V8 do Google Chrome e permite que você crie aplicativos de rede escaláveis ​​e de alto desempenho.

- Explique o Event Loop em Node.js.
    
    [R]: O Event Loop é o mecanismo que permite que Node.js seja assíncrono. Ele permite que o Node.js execute operações de I/O não bloqueantes, como leitura de arquivos e chamadas de rede, sem bloquear a execução do código.

- O que são Callbacks em Node.js?
    
    [R]: Callbacks são funções que são passadas como argumentos para outras funções. Quando a função é executada, ela chama a função de retorno de chamada.
    Exemplo:
    ```javascript
    const fs = require('fs');

    function readFileCallback(filePath, callback) {
        fs.readFile(filePath, 'utf8', (err, data) => {
            if (err) {
                callback(err);
            } else {
                callback(null, data);
            }
        });
    }

    readFileCallback('arquivo.txt', (err, data) => {
        if (err) {
            console.error(err);
        } else {
            console.log(data);
        }
    });
    ```

- O que são Promises em Node.js?
    
    [R]: Promises são objetos que representam um valor futuro em Node.js. Elas são usadas para lidar com operações assíncronas de forma mais legível e fácil de manter do que os callbacks. Elas também permitem que você lide com erros de forma mais fácil do que os callbacks.
    Exemplo:
    ```javascript
    const fs = require('fs');

    function readFilePromise(filePath) {
        return new Promise((resolve, reject) => {
            fs.readFile(filePath, 'utf8', (err, data) => {
            if (err) {
                reject(err);
            } else {
                resolve(data);
            }
            });
        });
    }

    async function main() {
        try {
            const data = await readFilePromise('arquivo.txt');
            console.log(data);
        } catch (err) {
            console.error(err);
        }
    }
    ```

- O que é NPM em Node.js?
    
    [R]: NPM é o gerenciador de pacotes padrão para Node.js. Ele permite que você instale pacotes de terceiros e gerencie dependências de maneira fácil e intuitiva.

- O que são Streams em Node.js?
    
    [R]: Streams são objetos que permitem que você leia e escreva dados de maneira assíncrona. Elas são usadas para lidar com grandes quantidades de dados de maneira eficiente e escalável.
    
    Exemplo:
    - Instale o pacote csv-parser:
        ```bash
        npm install csv-parser
        ```
    - Usando o csv-parser para ler um arquivo CSV e escrever um arquivo JSON:
        ```javascript
        const fs = require('fs');
        const csv = require('csv-parser');

        const inputStream = fs.createReadStream('dados.csv');
        const csvParser = csv();
        const outputStream = fs.createWriteStream('output.json');

        inputStream
            .pipe(csvParser)
            .pipe(outputStream);

        csvParser.on('data', (data) => {
            // Aqui, você pode fazer o que desejar com cada objeto JSON
            console.log('Objeto JSON:', data);
        });

        csvParser.on('error', (error) => {
            console.error('Erro ao fazer parse do CSV:', error);
        });

        inputStream.on('end', () => {
            console.log('Leitura do CSV concluída.');
        });

        ```

- Qual a diferença entre Arrow Functions de Funções normais em Node.js.

    [R]: As Arrow Functions são uma forma mais concisa de escrever funções em JavaScript e têm um comportamento diferente em relação ao escopo de `this` em comparação com as funções normais.
    
    Exemplo: 
    ```javascript
    // Função normal
    function soma(a, b) {
        return a + b;
    }

    // Arrow Function
    const soma = (a, b) => a + b;
    ```

    Exemplo que ilustra a diferença no contexto léxico (escopo)
    ```javascript
    const obj1 = {
        name: 'Objeto 1',
        sayHello: function() {
            console.log(`Olá de ${this.name}`);
        }
    };
    
    obj1.sayHello(); // Output: Olá de Objeto 1
    
    // Usando uma arrow function
    const obj2 = {
        name: 'Objeto 2',
        sayHello: () => {
            console.log(`Olá de ${this.name}`);
        }
    };
    
    obj2.sayHello(); // Output: Olá de undefined
    ```

    Neste exemplo, obj1 usa uma função tradicional dentro do método sayHello(), e quando chamamos obj1.sayHello(), ele corretamente imprime "Olá de Objeto 1" porque a função tradicional mantém o contexto léxico do objeto obj1.

    Por outro lado, obj2 usa uma arrow function no método sayHello(). Quando chamamos obj2.sayHello(), ele imprime "Olá de undefined" porque as arrow functions não têm seu próprio contexto this e herdam o contexto léxico de onde foram definidas. 

- Explique o uso de const, `let` e `var` em Node.js.

    [R]: 
    - `const` é usado para declarar variáveis ​​que não podem ser reatribuídas. 
    - `let` é usado para declarar variáveis ​​que podem ser reatribuídas. 
    - ``var`` é usado para declarar variáveis ​​que podem ser reatribuídas e redeclaradas. 
        
    A diferença principal entre `let` ou `const` e `var` é que `let` ou `const` possuem escopo de bloco, enquanto `var` possui escopo de função. Variáveis declaradas com `let` ou `const` só podem ser acessadas dentro do bloco em que foram declaradas, enquanto variáveis declaradas com `var` podem ser acessadas dentro da função em que foram declaradas.

- Como você faz logs em Node.js?
    
    [R]: Você pode utilizar o console.log() para realizar logs no Node.js. Além disso, existem bibliotecas de terceiros que oferecem recursos adicionais de logging, como o Winston e o Pino. O Winston é uma biblioteca popular que fornece recursos como logging em arquivos, logging em vários níveis e logging em diversos destinos. O Pino é uma biblioteca de logging muito rápida e segura que oferece funcionalidades semelhantes ao Winston, sendo ainda mais veloz.