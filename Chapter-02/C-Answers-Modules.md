# Modules :: Practice and Answers

Here are five challenges related to modules in Ruby along with their solutions:

### Challenge 1: Create a Logging Module

**Challenge:**
Create a logging module that can be included in different classes to log messages.

**Solution:**
```ruby
module Logging
  def log(message)
    puts "[LOG] #{message}"
  end
end

class Order
  include Logging
end

class Product
  include Logging
end

order = Order.new
order.log("Order placed.")

product = Product.new
product.log("Product added to inventory.")
```

### Challenge 2: Implement a Validation Module

**Challenge:**
Create a validation module that can be included in a class to validate certain properties.

**Solution:**
```ruby
module Validation
  def validate_length(attribute, min_length)
    value = send(attribute)
    unless value.length >= min_length
      puts "#{attribute.capitalize} must be at least #{min_length} characters long."
    end
  end
end

class User
  include Validation

  attr_accessor :username

  def initialize(username)
    @username = username
  end
end

user = User.new("john_doe")
user.validate_length(:username, 8)
```

### Challenge 3: Develop a Math Module

**Challenge:**
Create a math module with methods for basic mathematical operations.

**Solution:**
```ruby
module MathOperations
  def square_root(number)
    Math.sqrt(number)
  end

  def cube(number)
    number ** 3
  end
end

class Calculator
  include MathOperations
end

calculator = Calculator.new
puts calculator.square_root(25)  # Output: 5.0
puts calculator.cube(3)          # Output: 27
```

### Challenge 4: Implement a Persistence Module

**Challenge:**
Create a persistence module that provides methods for saving and loading objects.

**Solution:**
```ruby
module Persistence
  def save(filename)
    File.open(filename, 'w') { |file| file.puts to_json }
    puts "Object saved to #{filename}."
  end

  def load(filename)
    data = File.read(filename)
    from_json(data)
    puts "Object loaded from #{filename}."
  end
end

class Product
  include Persistence

  attr_accessor :name, :price

  def initialize(name, price)
    @name = name
    @price = price
  end

  def to_json
    { name: name, price: price }.to_json
  end

  def from_json(data)
    json_data = JSON.parse(data)
    @name = json_data['name']
    @price = json_data['price']
  end
end

product = Product.new("Laptop", 999)
product.save("product_data.json")
loaded_product = Product.new("Unknown", 0)
loaded_product.load("product_data.json")
puts loaded_product.name    # Output: Laptop
puts loaded_product.price   # Output: 999
```

### Challenge 5: Create a Mixin for String Formatting

**Challenge:**
Develop a mixin module for formatting strings with methods for title case and camel case.

**Solution:**
```ruby
module StringFormatting
  def format_title_case(str)
    str.split.map(&:capitalize).join(' ')
  end

  def format_camel_case(str)
    words = str.split
    camel_case = words.first.downcase + words[1..-1].map(&:capitalize).join
    camel_case
  end
end

class TextProcessor
  include StringFormatting
end

text_processor = TextProcessor.new
puts text_processor.format_title_case("hello world")  # Output: Hello World
puts text_processor.format_camel_case("hello world")  # Output: helloWorld
```

These challenges cover a range of scenarios, from logging and validation to mathematical operations, persistence, and string formatting. They demonstrate how modules can be used to encapsulate and reuse functionality across different classes.
