# Exemplo de Uso da Interface Comparator em Java

Este projeto demonstra como implementar e utilizar a interface `Comparator` em Java
 ordenando uma lista de objetos personalizados (`Product`) com base em um critério específico — neste caso;
  o nome do produto em ordem alfabética, ignorando diferenças entre maiúsculas e minúsculas.

## 📁 Estrutura do Projeto

```
src/
├── application/
│   └── Program.java
└── entities/
    ├── Product.java
    └── MyComparator.java
```

## 🧠 Conceitos Demonstrados

* Programação orientada a objetos (POO)
* Implementação da interface `Comparator`
* Ordenação de listas com `List.sort()`
* Manipulação de strings e comparação case-insensitive
* Formatação de saída com `String.format`

## 📦 Classes

### `Product.java`

Classe que representa um produto com nome e preço.

```java
public class Product {
    private String name;
    private Double price;
    // Construtor, getters, setters e toString()
}
```

### `MyComparator.java`

Classe que implementa a interface `Comparator<Product>` para ordenar produtos com base no nome, ignorando letras maiúsculas e minúsculas.

```java
public class MyComparator implements Comparator<Product> {
    @Override
    public int compare(Product p1, Product p2) {
        return p1.getName().toUpperCase().compareTo(p2.getName().toUpperCase());
    }
}
```

### `Program.java`

Classe principal que instancia produtos, os adiciona a uma lista e os ordena usando o `MyComparator`.

```java
list.sort(new MyComparator());
```
