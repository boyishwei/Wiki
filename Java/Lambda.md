### Lambda Expression in java

>  Lambda introduced since Java 8 (in java.util.function and java .util.stream)

 > Lambda can be used to replace anonymous inner class

* Common Lambda Functional Interfaces
  * Predicate - takes one argument, return a Bolean
  ```Java
  Predicate<String> varifyStringLength = (str) -> str.length() > 11;
  System.out.println(varifyStringLength.test("videos"));
  ```

  * Consumer - accepts single argument without return value
  ```Java
  Consumer<String> consumer = (str) -> System.out.println(str);
  consumer.accept("welcome to lambda expression introduction");
  ```

  * Function - accepts one argument and produces a result
  ```Java
  Function<Integer, String> converter = (num) -> String.valueOf(num + 5);
  System.out.println(converter.apply(25));
  ```

  * Supplier - takes no argument and return results
  ```Java
  Function<Integer, String> converter = (num) -> String.valueOf(num + 5);
  System.out.println(converter.apply(25));
  ```

  * Unary Operator - takes single argument with a return value
  ```Java
  UnaryOperator<String> ryanGreeting1 = (name) -> new String("Ryan said, hello ").concat(name);
  UnaryOperator<String> ryanGreeting2 = "Ryan said, hello "::concat;
  ```

  * BinaryOperator - takes two arguments and return one value
  * Or you can define your own lambda functional Interfaces
    ```Java
    @FunctionalInterface
    public interface GreetingFounction<T, R>{
        R convert(T t);
    }

    GreetingFounction<Integer, BigDecimal> greetingFounction = (index) -> new BigDecimal(index).setScale(5);
    System.out.println(greetingFounction.convert(100).scale());
    ```

  * Methods can be used as lambda
   feature of java 8, it can converts any methods into lambda expression including static method, instance method and even constructors.

#### Knowledge Assess
1. What is the definition of Functional Interface?
  * An interface with only one abstract method.
2. There are only 4 types of functional interfaces.
  * False. There are more interfaces available in ‘java.util.function’ package.
3. The Predicate interface takes in an input and what does it return?
  * A boolean. It contains a Boolean valued function that takes in one argument, use a test method to evaluate it and returns a Boolean.
4. The Consumer Interface doesn't return value.
  * Correct!  As the name says, it consumes the argument, meaning that it accepts a single argument and does not return a result.
5. Lambda expressions have to take at least one argument.
  * Lambda functions can take no parameter, one or more as arguments.
6. What functional interface does the forEach loop take as argument?
  *  The forEach is contained in a class that implements the Consumer Interface.
7. You can create generic lambda expressions.
  * False. Functional interface can be defined to generic, but the lambda expression can't
