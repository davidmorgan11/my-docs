## Quick Hints

### Declarative calculate sum
```java
IntStream.of(1, 2, 3, 4, 5).sum();
IntStream.rangeClose(1, 5).sum()
```
### Declarative find min
```java
List<Integer> numbers = Array.asList(1, 2, 3, 4, 5);
numbers.stream().min(Integer::compareTo);
```

# Java 8
## Lambda Expression
* Anonymous function
* Function without a name
* Does not belong to any class
* No return type, Java 8 compiler infers return type
* -> denotes Lambda expression
* SAM (Single Abstract Method) a functional interface
```java
() -> {}
(input params) -> {body}
```
### Functional Interface
```java
@FunctionalInterface
public interface Runnable {
    public abstract run(); // <- SAM
}
```