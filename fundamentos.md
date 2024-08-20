### Fundamentos de JavaScript

---

#### Lista Básica

1. **Declarar Variáveis e Exibir Resultados**

   ```javascript
   let a = 1, b = 2;
   let c = 'Lucas e ', d = 'Beatriz';
   let e = '1', f = '4';
   console.log(a + b);
   console.log(c + d);
   console.log(e + f);
   ```

2. **Mensagem de Boas-Vindas**

   ```javascript
   let nome = 'Lucas';
   console.log('Boas-vindas, ' + nome);
   ```

3. **Cálculo da Área de um Retângulo**

   ```javascript
   let base = 12, altura = 15;
   console.log('A área do retângulo corresponde a: ' + base * altura);
   ```

4. **Verificar Maioridade**

   ```javascript
   let idade = 17;
   if (idade >= 18) {
       console.log('Maior de idade **Liberado');
   } else {
       console.log('Menor de idade **Bloqueado');
   }
   ```

5. **Verificar Paridade de um Número**

   ```javascript
   let num = 2;
   if (num % 2 == 0) {
       console.log('O número é par');
   } else {
       console.log('O número é ímpar');
   }
   ```

---

#### Comentários em JavaScript

- **Comentário de uma Linha**
  
  ```javascript
  // Este é um comentário de uma linha
  ```

- **Comentário Multilinha**

  ```javascript
  /* Este é um
     comentário
     multilinha */
  ```

---

#### Alert e Confirm

```javascript
alert('Isso é um alerta!');
let resposta = confirm('Seus dados estão corretos?');
```

---

#### Entrada e Saída de Dados

- **Entrada de Dados**

  ```javascript
  let nomen = prompt('Informe seu nome:');
  let idaden = prompt('Informe sua idade:');
  console.log('Seu nome é ' + nomen + ' e você tem ' + idaden + ' anos');
  ```

- **Saída de Dados pelo Console**

  ```javascript
  let minhaVariavel = 'Olá, mundo!';
  console.log(minhaVariavel);
  ```

- **Saída de Dados por meio de Documento HTML**

  ```javascript
  document.write('Saída de dados por meio de documento HTML utilizando JavaScript!');
  ```

---

#### Tipos de Dados

- **Tipos Primitivos**: 
  - `Number` (inteiros e ponto flutuante)
  - `String` (cadeia de caracteres)
  - `Boolean` (true or false)
  - `Undefined` (variável declarada, mas sem valor definido)
  - `Null` (ausência de valor ou valor nulo)
  - `Symbol` (ES6)

- **Tipos de Referência**:
  - `Objeto (Object)`: { nome: 'Alice', idade: 30 }
  - `Array`: [1, 2, 3]
  - `Função (Function)`
  - `Data (Date)`
  - `RegExp (Expressões Regulares)`

- **Tipos Especiais**:
  - `NaN` (Not-a-Number)
  - `Infinity` e `-Infinity`

- **Tipagem Dinâmica**: JavaScript é uma linguagem de tipagem dinâmica, onde o tipo é determinado em tempo de execução.

---

#### Variáveis

- **Regras de Nomenclatura**:
  - Devem começar com uma letra, sublinhado `_`, ou cifrão `$`.
  - Podem conter letras, números, sublinhados e cifrões.
  - Sensíveis a maiúsculas e minúsculas.
  - Não podem usar palavras-chave reservadas.

- **Exemplos**:

  ```javascript
  let num = 10; // tipo inteiro
  let nums = '10'; // tipo string
  console.log(num);
  console.log(num + nums);
  console.log(num + 10);
  console.log(num + nums + 20);
  ```

- **Reatribuição de Variáveis**:

  ```javascript
  let x = 10;
  x = 5;
  console.log(x);
  ```

- **Variáveis de Bloco (Escopo de Variáveis)**:

  ```javascript
  if (true) {
      let bloco = 'Está dentro deste bloco';
      console.log(bloco);
  }
  // console.log(bloco) // ERRO: variável fora do escopo
  ```

- **Hoisting (Içamento)**:

  ```javascript
  console.log(numero);
  var numero = 14; // undefined
  ```

  > As variáveis declaradas com `var` são içadas para o topo do escopo, enquanto `let` e `const` não são.

---

#### Tipos de Dados Especiais: `null` e `undefined`

- **`null`**: Ausência intencional de valor.
- **`undefined`**: Variável declarada, mas sem valor atribuído.

---

#### Operadores e Funções

- **Operadores Aritméticos**:

  ```javascript
  console.log(a + b); // Adição
  console.log(a - b); // Subtração
  console.log(a * b); // Multiplicação
  console.log(a / b); // Divisão
  console.log(a ** b); // Exponenciação
  console.log(b % 2); // Módulo
  ```

- **Operadores de Atribuição**:

  ```javascript
  let n = 40;
  n += 1; // Incremento
  console.log(n);
  ```

- **Funções Matemáticas (Math)**:

  ```javascript
  console.log(Math.round(3.5)); // Arredondamento
  console.log(Math.sqrt(16)); // Raiz Quadrada
  ```

- **Operadores de Comparação**:

  ```javascript
  console.log(a == b); // Igual
  console.log('5' == b); // Igual (independentemente do tipo de dado)
  console.log('5' === b); // Estritamente Igual
  console.log(a != b); // Diferente
  console.log('5' !== b); // Estritamente Diferente
  ```

- **Operadores Lógico-Relacionais**:

  ```javascript
  console.log(a > b && b < a); // true
  console.log(a > b || b > a); // true
  ```

- **Conversão de Tipos de Variáveis**:

  ```javascript
  const num2 = "123";
  const num2c = +num2; // Conversão para número
  console.log(typeof num2c); // number
  ```

---

#### Estruturas Condicionais e de Repetição

- **Condicional `if-else`**:

  ```javascript
  const idade = 18;
  if (idade < 13) {
      console.log('Criança');
  } else if (idade >= 13 && idade < 18) {
      console.log('Adolescente');
  } else {
      console.log('Adulto');
  }
  ```

- **Switch Case**:

  ```javascript
  const fruta = 'banana';
  switch(fruta) {
      case 'banana':
          console.log('A fruta é uma banana');
          break;
      case 'laranja':
          console.log('A fruta é uma laranja');
          break;
      default:
          console.log('A fruta não foi encontrada');
          break;
  }
  ```

- **Laços de Repetição (`for`, `while`, `do-while`)**:

  ```javascript
  for (let i = 1; i <= 5; i++) {
      console.log(i);
  }

  let k = 1;
  while (k <= 3) {
      console.log(k);
      k++;
  }

  let j = 1;
  do {
      console.log(j);
      j++;
  } while (j < 4);
  ```

---

#### Funções

- **Definindo Funções**:

  ```javascript
  function saudacao() {
      console.log('Olá! Aqui estou utilizando uma função.');
  }
  saudacao();

  function cumprimento(nome) {
      console.log('Olá, ' + nome);
  }
  cumprimento('Lucas');
  ```

- **Funções com Valor de Retorno**:

  ```javascript
  function fsoma(a, b) {
      return a + b;
  }
  let resultado = fsoma(100, 5);
  console.log(resultado);
  ```

- **Arrow Function**:

  ```javascript
  const arrowTeste = () => console.log('Aqui também deu certo!');
  arrowTeste();
  ```

---

#### Arrays e Strings

- **Manipulação de Arrays**:

  ```javascript
  const numeros = [1, 2, 3, 4, 5];
  console.log(numeros);
  numeros.push('maçã', 7, 8);
  console.log(numeros);
  numeros.pop();
  console.log(numeros);
  numeros.shift();
  console.log(numeros);
  let indice = numeros.indexOf("maçã");
  console.log('Índice do elemento "maçã": ' + indice);
  let tamanho = numeros.length;
  console.log('Tamanho do array: ' + tamanho

);
  ```

- **Métodos de String**:

  ```javascript
  const nome2 = 'Lucas';
  console.log(nome2.length);
  console.log(nome2.indexOf('L'));
  console.log(nome2.toUpperCase());
  console.log(nome2.toLowerCase());
  ```

---

#### Funções de Tempo e Trabalhando com Datas

- **Funções de Tempo (`setTimeout` e `setInterval`)**:

  ```javascript
  setTimeout(() => {
      console.log('Executado após 2 segundos');
  }, 2000);

  let contador = 0;
  const interval = setInterval(() => {
      console.log(contador);
      contador++;
      if (contador === 5) {
          clearInterval(interval);
      }
  }, 1000);
  ```

- **Trabalhando com Datas (`Date`)**:

  ```javascript
  const agora = new Date();
  console.log(agora.toLocaleString());
  console.log(agora.getFullYear());
  console.log(agora.getMonth() + 1);
  console.log(agora.getDate());
  ```

---

Esta estrutura cobre os fundamentos essenciais de JavaScript, preparando o terreno para exploração mais aprofundada em desenvolvimento web e frameworks modernos como React.