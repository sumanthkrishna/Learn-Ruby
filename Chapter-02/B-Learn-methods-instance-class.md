# Methods:: Instance vs Class

In Ruby, class methods and instance methods are two types of methods associated with classes, and they serve different purposes.

Instance Methods:
Definition: Instance methods are methods that are called on instances (objects) of a class. They operate on the attributes (instance variables) of an object.

Access to Data: Instance methods have access to and can modify the state (instance variables) of the object on which they are called.

Declaration: Instance methods are defined using the def keyword within the class definition.

Example:

```ruby
class MyClass
  def instance_method
    puts "This is an instance method"
  end
end

obj = MyClass.new
obj.instance_method
```

Class Methods:
Definition: Class methods are methods that are called on the class itself, rather than on instances of the class. They are prefixed with the self keyword within the class definition.

Access to Data: Class methods have access to class-level data but not to instance-specific data (instance variables). They cannot modify the state of a particular instance.

Declaration: Class methods are defined using the def self.method_name syntax or def ClassName.method_name syntax.

Example:

```ruby
class MyClass
  def self.class_method
    puts "This is a class method"
  end
end

MyClass.class_method
```

When to Use Each:
Instance Methods:

Used when the method needs to interact with or modify the state of a particular instance.
Access to instance variables and instance-specific data.
Often involved in encapsulation and exposing behavior associated with an object.
Class Methods:

Used when the method is related to the class itself and doesn't depend on the state of a particular instance.
Access to class-level data and methods.
Often used for factory methods, utility methods, or methods that perform operations at the class level.
Practical Example:
```ruby
class MathOperations
  # Instance method
  def square(number)
    number * number
  end

  # Class method
  def self.average(numbers)
    sum = numbers.reduce(0, :+)
    sum / numbers.length.to_f
  end
end

# Using instance method
obj = MathOperations.new
puts obj.square(5)

# Using class method
numbers = [1, 2, 3, 4, 5]
puts MathOperations.average(numbers)
```
In this example, the square method is an instance method, as it operates on a specific number. The average method is a class method, as it performs an operation related to the entire class (calculating the average of an array of numbers).
