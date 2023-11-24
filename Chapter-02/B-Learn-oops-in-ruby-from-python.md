
# Object Orinted Programming :: Python vs Ruby

Let's create a table comparing the implementation of Object-Oriented Programming (OOP) concepts in Python and Ruby using the example of a zoo and animals:

| OOP Concept                  | Python                                    | Ruby                                       |
| ---------------------------- | ----------------------------------------- | ------------------------------------------- |
| **Class Definition**         | ```python class Animal: pass ```          | ```ruby class Animal; end ```               |
| **Instantiation**            | ```python lion = Animal() ```             | ```ruby lion = Animal.new ```               |
| **Constructor**              | ```python def __init__(self, name):```     | ```ruby def initialize(name); end ```      |
| **Attributes**               | ```python self.name = name ```            | ```ruby attr_accessor :name ```             |
| **Methods**                  | ```python def make_sound(self):```        | ```ruby def make_sound; end ```             |
| **Inheritance**              | ```python class Lion(Animal): pass```     | ```ruby class Lion < Animal; end ```       |
| **Encapsulation**            | ```python self._age = age```             | ```ruby private attr_reader :age ```       |
| **Polymorphism**             | ```python def make_sound(self):```        | ```ruby def make_sound; end ```             |
| **Abstract Class/Module**    | ```python from abc import ABC, abstractmethod; class Animal(ABC):``` | ```ruby module Animal; end ```             |
| **Interface/Mixin**          | ```python class Swimmer: pass; class Dolphin(Animal, Swimmer): pass``` | ```ruby module Swimmer; end ```            |
| **Static Methods**           | ```python @staticmethod; def sleep():``` | ```ruby def self.sleep; end ```            |
| **Object Instantiation**     | ```python lion = Animal()```              | ```ruby lion = Animal.new ```               |
| **Method Overloading**       | ```python def eat(self, food):```         | ```ruby def eat(food); end ```             |

#### Key Points:

1. **Syntax Differences:**
   - Python uses indentation for block structure.
   - Ruby uses `end` to denote the end of a block.

2. **Access Modifiers:**
   - Python has a convention of using a single leading underscore for protected attributes.
   - Ruby uses `attr_accessor`, `attr_reader`, `attr_writer` to control access.

3. **Inheritance:**
   - Both Python and Ruby use the `class` keyword for class inheritance.
   - Ruby uses `<` symbol for class inheritance.

4. **Encapsulation:**
   - Python uses a single leading underscore (`_`) for protected attributes and a double leading underscore (`__`) for name mangling.
   - Ruby uses `attr_accessor`, `attr_reader`, `attr_writer` to control access.

5. **Polymorphism:**
   - Both Python and Ruby support polymorphism, allowing objects of different types to respond to the same method call.

6. **Abstract Classes/Modules:**
   - Python uses the `ABC` module for abstract classes.
   - Ruby uses modules for similar functionality.

7. **Interfaces/Mixins:**
   - Python uses multiple inheritance and abstract classes for interfaces.
   - Ruby uses modules for mixins.

8. **Static Methods:**
   - Both Python and Ruby support static methods.

Understanding these similarities and differences can help learners transition between Python and Ruby, providing insights into how OOP concepts are implemented in each language.
