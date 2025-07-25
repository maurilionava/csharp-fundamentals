**REVIEW**
- Memórias *Heap* e *Stack*
- Tipos de *valor* e *referência*: *ValueType* armazena um valor diretamente na memória enquanto *ReferenceType* armazena uma referência a um espaço da memória que contém os dados
- Campos vs propriedades
- Tipo e função anônimas: 
  - *tipo anônimo*
  - *função anônima* declaração in-line ou expressãp que pode ser usada sempre que um tipo delegate for esperado. São dois os tipos: métodos anônimos e expressões lambdas
- Classes parciais: funciona para classes, interfaces, structs e métodos
- Os pilares da POO
  - abstração
  - encapsulamento: recurso que impede o acesso direto aos atributos de uma classe
  - herança: recurso que permite a reutilização, extensão e modificação de comportamento definido em outras classes criando a relação de classe base e classe derivada
  - polimorfismo: habilidade de diferentes objetos responderem a uma mesma mensagem de formas diferentes 
- Composição vs agregação
- Classe vs objeto: *classe* é a estrutura enquanto *objeto* é a instância de uma classe
- Paradigmas de programação
- Downcasting e upcasting
- Boxing e unboxing: boxing é a conversão de *ValueType* para *ReferenceType*(int para object) e unboxing o inverso(object para int)
- *Delegates* é um tipo que representa referências a métodos, que pode ser alterada em tempo de execução, com uma *lista de parâmetros* e *um tipo de retorno*
  - Singlecast e multicast: single se refere a apenas um método, enquanto o multi se referencia a dois ou mais métodos em sequência
  - Métodos anônimos
  - Expressões lambdas: é uma função anônima que pode ser usada para criar *delegates*. Maneira mais curta de representar um método anônimo (sugar syntax). Permite criar métodos in-line sem precisar criar método nomeado separado
  - Delegates pré definidos: 
    - Predicate<T> : recebe um argumento do tipo T e retorna um booleano. Utilizado para testar se objeto satisfaz condição
    - Action<T> : recebe até 16 argumentos e não retorna valor. Utilizado para execução de ação sem retorno de valor
    - Function<T,TResult> : recebe até 16 argumentos do tipo T e retorno um valor do tipo TResult. Ideal para representar método que executa operação e retorna um resultado
    - EventHandler e EventHandler<TEventArgs> : utilizados para manipular eventos que não possui ou que possui dados, respectivamente
  - Eventos e seus manipuladores: mecanismos que permitem que uma classe ou objeto, *publisher*, notifique outras classes ou objetos, *subscriber*, quando alguma ação ocorre
- *Cast* e *convert*
- Structs: estrutura de dados armazenada em memória heap ideal para?
- Passagem de parâmetros por valor(cópia do valor armazenado em memória) e por referência(*ref* e *out*: referência do endereço de memória)
- Generics: significa a forma geral e não forma específica de forma a serem *parametrizados por tipo*. Possuem os métodos `GetHashCode()` e `Equals()`(compara igualdade de conteúdo)
  - Benefícios: reutilização de código, type safety, desempenho por não realizar operações de *boxing* e *unboxing*, são fortemente tipadas armazenando apenas um tipo de dados e evitando erros de incompatibilidade de tipo
- Coleções genéricas
  - List<T> coleção dinâmica e contígua de objetos = ArrayList
  - Dictionary<Tkey,TValue> coleção de pares chave-valor não ordenada = HashTable
  - Queue<T> coleção de objetos FIFO(first-in-first-out)
  - SortedList<T> coleção de pares chave-valor ordenados
  - Stack<T> coleção de objetos LIFO(last-int-first-out)
- Coleções não genéricas: armazenam dados do tipo *Object* fazendo com que sejam realizadas operações de *boxing* e *unboxing* de conversão implícita afetando desempenho
- *LINQ (Language Integrated Query)* conjunto de recursos para realizar consultas em diferentes coleções que implementem IEnumerable<T> ou IQueryable<T>. Retornos de tipo object e possui *deferred execution* onde somente é realizada a consulta ao iterar sobre a coleção
- *IEnumerable<T>* e *List<T>* : utilizar a primeira opção para acessar sequencialmente e implementar em diversas coleções, utilizar a segunda opção se for necessário acessar e modificar de forma eficiente uma coleção
- Programação *assíncrona* e *paralela*: execução de várias tarefas ao mesmo tempo sem o bloqueio da thread principal. Execução de várias tarefas ao mesmo tempo aproveitando os recursos do processador
    - Task e Task<T> : memória heap e garbage collector, consumo de memória e desempenho
    - ValueTask e ValueTask<T> : struct armazenado na memória stack, tipo de valor

Task.Run Thread.Run ThreadPool
Reflection
maquina de estado
yield