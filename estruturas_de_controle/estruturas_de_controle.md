## Estruturas de controle

1. Estruturas de sequência

2. Estruturas de selecão

3. Estruturas de repetição

### Estruturas de sequência

Basicamente se refere ao conjunto de instruções predeterminadas de um programa dispostos de forma sequêncial em um código fonte.

### Estruturas de seleção

São estruturas que utilizam expressões condicionais como base elaborar um programa. Estas condições retornam verdadeiro ou falso, ou seja, um booleano, podendo ser representado com estruturas como o if e else por exemplo.

| Estruturas  | 
|-------------|
|  if         |
|  else       |
|  else if    |
|  switch/case|

#### Exemplo de Switch Case

- Com base no valor da variável `opcao` é com que o caso irá ser escolhido, no exemplo a baixo como a opção não se trata de nenhuma das disponíveis o caso `default` será executado. As opções representadas como números também poderiam ser caracteres como `case 'a':`, por exemplo.  

~~~dart
const opcao = 10;

switch (opcao) {
    case 1:
      print("Caso 01");
      break;
    case 2:
      print("Caso 02");
      break;
    default:
      print("Caso padrão");
  }

~~~

### Estruturas de repetição

Realizam a repetição de operações com base em condições.

| Estruturas |
|------------|
| for        |
| while      |
| do/while   |


#### Estrutura do comando for

- Utilizado quando se sabe a quantidade de vezes necessária de repetições para se executar

`for(inicialização, expressão, incremento)`

##### Exemplo de for
~~~dart
// Apenas imprime os valores pares
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) {
       print(i);
    }
  }
~~~

##### Exemplo for in
~~~dart
Map<String, double> notas = {
    'João Pedro': 6,
    'Alanzin': 9.5,
  };

  // funções Map -> .keys, .values and .entries
  for (final nome in notas.keys) {
    print('O nome é $nome e a nota é: ${notas[nome]}');
  }
~~~

#### Estrutura de comando while e do/while

- Utilizado qunado irá repetir uma quantidade indeterminada de valores, ou seja, sem saber a quantiade exata de execuções 

###### Estrutura while

- Repete a execução enquanto a condição do while for válida

~~~dart
var condicao;

while (condicao != true){
    condicao = false;
}
~~~

###### Estrutura do/while

- A prinicipal diferença do do/while para o while é que o do/while executa pelo menos uma vez, enquanto o while, pode executar nenhuma ou várias vezes.

~~~dart
var digitado;

do {
    stdout.write("Digite algo ou sair: ");

    digitado = stdin.readLineSync();
  } while (digitado != 'sair');
~~~

#### Funções para controle de loop ou switch/case

##### break
- Interrompe o fluxo de controle do loop, ou seja, também finaliza um caso do switch/case

##### continue
- Ao invés de interromper o loop, o continue apenas finaliza a iteração, passando assim para a próxima e no caso do switch/case é preciso criar uma label, ou seja, um rótulo para que de um caso seja possível acessar outros.

~~~dart
const valor = 'a';

  switch (valor) {
    case 'a':
      print("Caso 01");
      continue label;
    label:
    case 'b':
      print("Caso 02");
      break;
  }
~~~






