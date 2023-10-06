# TypeScript

- O que é TypeScript?
    
    [R]: TypeScript é uma linguagem de programação de código aberto desenvolvida pela Microsoft. É um superset do JavaScript que adiciona tipagem estática opcional ao JavaScript. Isso significa que você pode adicionar tipos a variáveis, parâmetros de função e retornos de função, o que ajuda a evitar erros de tipo durante o desenvolvimento.

- Quais são os benefícios do TypeScript?

    [R]: Os benefícios do TypeScript incluem:

    - Tipagem Estática: Ajuda a capturar erros de tipo em tempo de compilação.
    - Melhor Autocompletamento: IDEs podem oferecer sugestões de código mais precisas.
    - Leitura e Manutenção: Tipos bem definidos tornam o código mais claro e legível.
    - Refatoração Segura: Mudanças no código podem ser feitas com mais confiança.
    - Suporte a ES6+: TypeScript suporta as últimas funcionalidades do JavaScript.

- Qual é a diferença entre type e interface em TypeScript?
    [R]: type e interface são duas maneiras de definir tipos personalizados em TypeScript. A principal diferença é que type permite criar tipos e interface é usada principalmente para definir contratos.

    Exemplos: 
    ```typescript
    type Person = {
        name: string;
        age: number;
    };

    interface Person {
        name: string;
        age: number;
    }
    ```

- O que são Decorators em TypeScript?
    
    [R]: Decorators são uma característica experimental em TypeScript e JavaScript que permitem adicionar metadados a classes, métodos, propriedades e acessadores. Eles são comumente usados em estruturas como Angular para adicionar funcionalidades a classes.

    Exemplo de Decorator:
    ```typescript
    function log(target: any, key: string, descriptor: any) {
        console.log(key + ' was called');
    }

    class Person {
        private name: string;

        constructor(name: string) {
            this.name = name;
        }

        @log
        sayMyName() {
            console.log(this.name);
        }
    }
    ```
- O que são Generics em TypeScript?

    [R]: Generics permitem criar funções, classes e interfaces que trabalham com tipos variáveis, permitindo a reutilização de código com segurança de tipos.

    Exemplo de Generics em uma função:
    ```typescript
    function reverse<T>(items: T[]): T[] {
        const toreturn = [];
        for (let i = items.length - 1; i >= 0; i--) {
            toreturn.push(items[i]);
        }
        return toreturn;
    }

    const sample = [1, 2, 3];
    const reversed = reverse<number[]>(sample);
    console.log(reversed); // Output: [3, 2, 1]
    ```

- Como você compila um arquivo TypeScript?

    [R]: Para compilar um arquivo TypeScript, você pode usar o comando `tsc` no terminal. Por exemplo, se você tiver um arquivo chamado `index.ts`, você pode executar o comando `tsc index.ts` para compilar o arquivo TypeScript em JavaScript. Isso criará um arquivo `index.js` no mesmo diretório. 
    - ts-node: É uma ferramenta que permite executar arquivos TypeScript diretamente, sem a necessidade de compilação prévia para JavaScript. É útil para desenvolvimento e teste rápidos.
    - tsconfig.json: É um arquivo de configuração que permite definir opções de compilação para um projeto TypeScript. Ele permite que você especifique o arquivo de entrada, o diretório de saída, o nível de compatibilidade do ECMAScript e muitas outras opções.

- Quais são as boas práticas para desenvolvimento e produção em TypeScript?
    [R]: Alguns princípios das boas práticas em TypeScript incluem:

    - Usar tipagem estática para obter vantagens de autocompletamento e detecção de erros.
    - Evitar any sempre que possível para manter a segurança de tipos.
    - Usar interfaces e tipos para documentar estruturas de dados.
    - Manter código limpo e legível, seguindo padrões de nomenclatura consistentes.