# Modules :: Examples

### 1. Math Operations Module:

```ruby
module MathOperations
  def add(x, y)
    x + y
  end

  def subtract(x, y)
    x - y
  end
end

class Calculator
  include MathOperations
end

calculator = Calculator.new
puts calculator.add(5, 3)      # Output: 8
puts calculator.subtract(10, 4) # Output: 6
```

In this example, the `MathOperations` module provides basic mathematical operations that are included in the `Calculator` class.

### 2. Auditable Module for Logging:

```ruby
module Auditable
  def log(message)
    puts "[Audit] #{message}"
  end
end

class Order
  include Auditable
end

order = Order.new
order.log("Order placed.")
# Output: [Audit] Order placed.
```

Here, the `Auditable` module provides a logging method that is included in the `Order` class for auditing actions.

### 3. Enumerable Module:

```ruby
class MyCollection
  include Enumerable

  def initialize(data)
    @data = data
  end

  def each(&block)
    @data.each(&block)
  end
end

collection = MyCollection.new([1, 2, 3, 4, 5])
puts collection.select { |num| num.even? } # Output: [2, 4]
```

The `Enumerable` module provides a collection of methods such as `select`, and by including it in a class, those methods become available for instances of that class.

### 4. Mixin for String Formatting:

```ruby
module StringFormatter
  def format_uppercase(str)
    str.upcase
  end

  def format_lowercase(str)
    str.downcase
  end
end

class TextProcessor
  include StringFormatter
end

text_processor = TextProcessor.new
puts text_processor.format_uppercase("Hello")  # Output: HELLO
puts text_processor.format_lowercase("WORLD")  # Output: world
```

Here, the `StringFormatter` module provides methods for formatting strings, and the `TextProcessor` class includes these methods.

### 5. Comparable Module:

```ruby
class Student
  include Comparable

  attr_reader :name, :grade

  def initialize(name, grade)
    @name = name
    @grade = grade
  end

  def <=>(other)
    grade <=> other.grade
  end
end

student1 = Student.new("Alice", 85)
student2 = Student.new("Bob", 92)

puts student1 < student2  # Output: true
```

The `Comparable` module provides comparison methods such as `<`, `>`, and `==`, and by including it, the class gains the ability to compare instances.

These examples illustrate different use cases for modules in Ruby, showcasing their versatility in providing reusable and organized functionality.
