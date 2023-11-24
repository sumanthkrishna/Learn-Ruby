# Object Oriented Programming (OOP)

Let's use the example of a zoo and animals to explain various object-oriented programming (OOP) concepts in Ruby. We'll cover class definition, instantiation, encapsulation, inheritance, and polymorphism.


### 1. **Class Definition:**

In this example, we'll define a `Zoo` class and an `Animal` class.

```ruby
class Animal
  attr_accessor :name, :sound

  def initialize(name, sound)
    @name = name
    @sound = sound
  end

  def make_sound
    puts "#{name} says #{sound}!"
  end
end

class Zoo
  attr_reader :animals

  def initialize
    @animals = []
  end

  def add_animal(animal)
    @animals << animal
  end

  def perform_concert
    puts "Zoo Concert:"
    @animals.each { |animal| animal.make_sound }
  end
end
```

### 2. **Instantiation:**

Now, let's create instances of the `Animal` class and the `Zoo` class.

```ruby
lion = Animal.new("Lion", "Roar")
elephant = Animal.new("Elephant", "Trumpet")

zoo = Zoo.new
zoo.add_animal(lion)
zoo.add_animal(elephant)
```

### 3. **Encapsulation:**

Encapsulation involves bundling the data (attributes) and methods that operate on the data into a single unit (class).

In the `Animal` class, `name` and `sound` are encapsulated, and methods like `make_sound` operate on this encapsulated data.

### 4. **Inheritance:**

Inheritance allows a class to inherit attributes and methods from another class. Let's create a subclass `Bird` that inherits from `Animal`.

```ruby
class Bird < Animal
  attr_accessor :fly_distance

  def initialize(name, sound, fly_distance)
    super(name, sound)
    @fly_distance = fly_distance
  end

  def fly
    puts "#{name} is flying #{fly_distance} meters."
  end
end

sparrow = Bird.new("Sparrow", "Chirp", 50)
```

### 5. **Polymorphism:**

Polymorphism allows objects of different classes to respond to the same method call. In this case, both `Animal` and `Bird` respond to the `make_sound` method.

```ruby
zoo.add_animal(sparrow)
zoo.perform_concert
```

### Conventions, Tips, and Tricks:

1. **Naming Conventions:**
   - Use CamelCase for class names (`Zoo`, `Animal`) and snake_case for variable and method names (`make_sound`, `fly_distance`).

2. **Instance Variables:**
   - Prefix instance variables with `@` to distinguish them from local variables.

3. **Encapsulation:**
   - Use `attr_accessor` or `attr_reader` to create getters and setters for attributes. Keep data private and provide controlled access.

4. **Inheritance:**
   - Avoid deep hierarchies; favor composition over inheritance when appropriate.

5. **Polymorphism:**
   - Design classes to share common interfaces, allowing them to be used interchangeably.

### Example Usage:

```ruby
# Creating instances
lion = Animal.new("Lion", "Roar")
elephant = Animal.new("Elephant", "Trumpet")
sparrow = Bird.new("Sparrow", "Chirp", 50)

# Adding animals to the zoo
zoo = Zoo.new
zoo.add_animal(lion)
zoo.add_animal(elephant)
zoo.add_animal(sparrow)

# Performing a concert
zoo.perform_concert
```

This example illustrates how to create and use classes in Ruby for a zoo simulation. It covers class definition, instantiation, encapsulation, inheritance, and polymorphism, following Ruby's object-oriented programming principles.
