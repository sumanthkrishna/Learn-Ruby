# Object Oriented Programming :: Java vs Ruby

Let's create a table comparing the implementation of Object-Oriented Programming (OOP) concepts in Java and Ruby using the example of a zoo and animals:

| OOP Concept                  | Java                                      | Ruby                                       |
| ---------------------------- | ----------------------------------------- | ------------------------------------------- |
| **Class Definition**         | ```java public class Animal { } ```        | ```ruby class Animal; end ```               |
| **Instantiation**            | ```java Animal lion = new Animal(); ```    | ```ruby lion = Animal.new ```               |
| **Constructor**              | ```java public Animal(String name) { } ``` | ```ruby def initialize(name); end ```      |
| **Attributes**               | ```java private String name; ```           | ```ruby attr_accessor :name ```             |
| **Methods**                  | ```java public void makeSound() { } ```   | ```ruby def make_sound; end ```             |
| **Inheritance**              | ```java class Lion extends Animal { }```   | ```ruby class Lion < Animal; end ```       |
| **Encapsulation**            | ```java private int age; ```               | ```ruby private attr_reader :age ```       |
| **Polymorphism**             | ```java public void makeSound() { } ```   | ```ruby def make_sound; end ```             |
| **Abstract Class/Module**    | ```java public abstract class Animal { }``` | ```ruby module Animal; end ```             |
| **Interface/Mixin**          | ```java interface Swimmer { } ```         | ```ruby module Swimmer; end ```            |
| **Static Methods**           | ```java public static void sleep() { } ``` | ```ruby def self.sleep; end ```            |
| **Object Instantiation**     | ```java Animal lion = new Animal(); ```   | ```ruby lion = Animal.new ```               |
| **Method Overloading**       | ```java public void eat(String food) { }``` | ```ruby def eat(food); end ```             |

#### Key Points:

1. **Syntax Differences:**
   - Java uses a more verbose syntax with explicit type declarations and semicolons.
   - Ruby has a more concise syntax with dynamic typing and no semicolons.

2. **Access Modifiers:**
   - Java uses keywords like `public`, `private`, `protected` for access control.
   - Ruby uses keywords like `attr_accessor`, `attr_reader`, `attr_writer` for similar purposes.

3. **Inheritance:**
   - Java uses the `extends` keyword for class inheritance.
   - Ruby uses `<` symbol for class inheritance.

4. **Encapsulation:**
   - Java uses access modifiers like `private`, `protected`, `public`.
   - Ruby uses `attr_accessor`, `attr_reader`, `attr_writer` to control access.

5. **Polymorphism:**
   - Both Java and Ruby support polymorphism, allowing objects of different types to respond to the same method call.

6. **Abstract Classes/Modules:**
   - Java has abstract classes, while Ruby has modules for achieving similar functionality.

7. **Interfaces/Mixins:**
   - Java uses interfaces to define contracts, and Ruby uses modules for mixins.

8. **Static Methods:**
   - Java uses the `static` keyword for static methods.
   - In Ruby, methods defined with `def self.method_name` are equivalent to static methods.

Understanding these similarities and differences can help learners transition between Java and Ruby, providing insights into how OOP concepts are implemented in each language.
