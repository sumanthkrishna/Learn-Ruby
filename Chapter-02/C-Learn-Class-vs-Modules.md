# Class vs Module in Ruby:

#### **1. Classes:**
- **Definition:** Classes are a blueprint for creating objects. They encapsulate attributes (variables) and behaviors (methods) that define the objects created from them.

- **Usage:**
  - Use classes when you want to create instances of objects that share common attributes and behaviors.
  - Classes support inheritance, allowing you to create a hierarchy of related objects.

- **Example:**
  ```ruby
  class Animal
    attr_accessor :name

    def initialize(name)
      @name = name
    end

    def speak
      puts "#{name} makes a sound."
    end
  end

  class Dog < Animal
    def speak
      puts "#{name} barks loudly!"
    end
  end

  dog = Dog.new("Buddy")
  dog.speak
  ```

- **When to Use:**
  - Use classes when you want to model objects with shared characteristics and behaviors.
  - Utilize classes for creating instances with unique state and behavior.

#### **2. Modules:**
- **Definition:** Modules are collections of methods and constants. They provide a way to group related functionalities without creating instances.

- **Usage:**
  - Use modules when you want to share methods across multiple classes.
  - Modules are often employed for code organization, mixins, and as namespaces.

- **Example:**
  ```ruby
  module Swimmer
    def swim
      puts "#{name} is swimming."
    end
  end

  class Fish
    include Swimmer

    attr_accessor :name

    def initialize(name)
      @name = name
    end
  end

  fish = Fish.new("Nemo")
  fish.swim
  ```

- **When to Use:**
  - Use modules when you want to share methods among multiple classes without creating a common parent class.
  - Modules are suitable for adding functionalities to multiple classes without using inheritance.

#### **Similarities:**
1. **Namespacing:**
   - Both classes and modules act as namespaces, encapsulating methods and constants to prevent naming conflicts.

2. **Encapsulation:**
   - Both classes and modules encapsulate methods and attributes, providing a way to organize and structure code.

3. **Reusability:**
   - Both can be reused in various parts of the program, promoting code modularity and reuse.

#### **Differences:**
1. **Instance vs Static:**
   - Classes create instances with state (variables) and behavior (methods).
   - Modules do not create instances; instead, they are included in classes to provide additional methods.

2. **Inheritance:**
   - Classes support inheritance, allowing a class to inherit attributes and behaviors from another class.
   - Modules do not support direct inheritance. Instead, they are included in classes to share methods.

3. **Multiple Inclusion:**
   - A class can only inherit from one class, but it can include multiple modules.
   - Modules can be mixed into multiple classes, allowing for more flexible code organization.

#### **Example Demonstrating Both:**
```ruby
module Eater
  def eat
    puts "#{name} is eating."
  end
end

class Animal
  attr_accessor :name

  def initialize(name)
    @name = name
  end
end

class Cat < Animal
  include Eater
end

class Dog < Animal
  include Eater
end

cat = Cat.new("Whiskers")
dog = Dog.new("Buddy")

cat.eat
dog.eat
```

In this example, the `Eater` module is included in both the `Cat` and `Dog` classes, demonstrating the reuse of the `eat` method across different classes. Classes are used to represent distinct objects (cats and dogs), while modules are employed to share common behavior (eating).
