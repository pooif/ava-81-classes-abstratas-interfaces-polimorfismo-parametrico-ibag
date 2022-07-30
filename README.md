# 8.1 // Classes abstratas, Interfaces e Polimorfismo Paramétrico // IBag

Use este link do GitHub Classroom para ter sua cópia alterável deste repositório: <>

Implementar respeitando os fundamentos de Orientação a Objetos.

**Tópicos desta atividade:** classes abstratas, interfaces, classes concretas, parametrização de tipos, generics.

---

Refatorar a interface `IBag` e a classe `Bag` para aceitarem a parametrização do tipo. Há uma classe [Bag](src/util/Bag.java) em [util](src/util/). No entanto, ela foi projetada para armazenar `Object`s. O objetivo desta atividade é torná-la genérica, adicionando a parametrização do tipo em ambas a interface `IBag` e a classe concreta `Bag`, conforme os casos de teste a seguir:

```java
IBag textos = new Bag(5);

textos.add("um");
textos.add("texto");
textos.add("de");
textos.add("exemplo");

// Deveria sem restrito apenas a Strings, então ...
textos.add(5); // não deveria compilar.

// Parametrizar o tipo na classe Bag para que as seguintes instrução funcionem:
// IBag<String> nomes = new Bag<>(4);
// nomes.add("Pierre");
// nomes.add("Han");
// nomes.add("Björn");
// nomes.add(5); // esta instrução não deve compilar, mantenha comentada.

// IBag<Integer> idades = new Bag<Integer>(4);
// idades.add(45);
// idades.add(54);
// idades.add(67);


// IBag<IBag<String>> bagDeBags = new Bag<>();

// IBag<String> nomes = new Bag<>(3);
// IBag<String> setores = new Bag<>(3);
// IBag<String> funcoes = new Bag<>(3);

// bagDeBags.add(nomes);
// bagDeBags.add(setores);
// bagDeBags.add(funcoes);

// System.out.println(bagDeBags);
```

