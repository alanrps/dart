## Fundamentos

| Tipos básicos  | Características                                          | Observação                                                              |
|----------------|-----------------------------------------------------------| -------------------------------------------------------------------------|
| var            | Dart faz a inferência de tipo da variável                 | Não permite fazer a alteração do tipo da variável, valor pode ser alterado                        |
| final          | Definida em tempo de execução                             | ``final String entradaUsuario = stdin.readLineSync();``                                                             |
| const          | Definida em tempo de compilação                           |  ``const PI = 3.14;``                                                                        |
| dynamic        | Não tem um tipo definido, muda de acordo com os valores que são atribuídos |   ``dynamic variavel = "abc"; variavel = 3;``                                                  |
| List           | Conhecido como array ou vetor, valores indexados, aceita repetições, heterogêneo |   ``List numeros = [1,2,3,4]; ou var numeros = [1,2,3,4];``                                                  |
| Set            | Conhecido como conjuntos, não indexados, não aceita repetições, heterogêneo e possui operações de conjunto  |   ``Set<String> times = {"Santos", "Flamengo"}; ou  var times = {"Santos", "Flamengo"}; ou Set<Object> times = {"Santos", 123};``                                                  |
| Map            | Conhecido como objeto, chaves e valores, heterogêneo  |   ``Map<int, String> pessoas = {1: "Alan"} ou var pessoas = {1: "Alan"};``                                                  |

### Cuidados

#### final
- O tipo ``final`` é constante, ou seja, o seu valor não pode ser alterado, mas no caso de um array, objeto ou conjunto, não é guardado o valor e sim a referência para outra variável, então não pode ser atribuido um novo valor ou referência, no entanto, a referência que está sendo apontada ainda pode ser modificada, a menos que seja especificado o bloqueio.

Exemplo:
- Permite adicionar novos valores: ``final valores = [1,2,3,4]; valores.add(5);``

- Não permite adicionar novos valores: ``final valores = const [1,2,3,4];``

#### var
- Se fosse uma ``var`` com o literal ``const`` como no exemplo acima, não seria possível fazer a modificação da referência recebida, no entanto, ainda seria possível atribuir uma nova referência, pois a variável do tipo ``var`` pode ser modificada.

Exemplo:

- A variável receberá a referência da nova, podendo assim ser modificada: ``var valores = const[1,2,4,5]; valores = [1,2];``

#### const
- No caso do tipo ``const`` tanto a variável quanto o literal, este que é o valor recebido também é atribuído como ``const`` por padrão. 

### Operados Lógicos

| Operados      | Representação | Descrição | 
|---------------|---------------|-----------|
|  AND          | &&            | Binário   |
|  OR           | &#124;&#124;  | Binário   |
|  Exclusive OR | ^             | Binário (retorna verdadeiro apenas se um dos valores for verdadeiro)  |
|  Negação      | !             | Unário    |


### Precedência de Operadores
1. Operadores aritméticos

2. Operadores relacionais

3. Operadores lógicos

### Curiosidades

#### Operadores Lógicos
- Possível fazer comparação de bits entre números utilizando operadores lógicos: ``3 & 7`` igual a ``(11) & (111) -> 3``

#### Comparação de valores
- Realzada de acordo com o tipo: ``3 == '3'`` -> false 
