# Collections

In Ruby, collections are objects that hold multiple values. These values can be of various data types and can be manipulated using a variety of methods. Here are the main types of collections supported in Ruby:

### 1. **Arrays:**

- **Definition:**
  - An ordered collection of elements. Each element has an index starting from 0.

- **Example:**
  ```ruby
  # Creating an array
  numbers = [1, 2, 3, 4, 5]

  # Accessing elements
  puts numbers[2]  # Output: 3

  # Modifying the array
  numbers.push(6)
  ```

### 2. **Hashes:**

- **Definition:**
  - An unordered collection of key-value pairs. Keys and values can be of any data type.

- **Example:**
  ```ruby
  # Creating a hash
  person = { "name" => "Alice", "age" => 30, "city" => "Wonderland" }

  # Accessing values
  puts person["name"]  # Output: Alice

  # Modifying the hash
  person["occupation"] = "Engineer"
  ```

### 3. **Sets:**

- **Definition:**
  - An unordered collection of unique elements. Sets don't allow duplicate values.

- **Example:**
  ```ruby
  # Creating a set
  colors = Set.new(["red", "green", "blue"])

  # Adding elements
  colors.add("yellow")

  # Checking for existence
  puts colors.include?("red")  # Output: true
  ```

### 4. **Ranges:**

- **Definition:**
  - Represents a range of values. Ranges can be used in various scenarios, such as iterating over a sequence of numbers.

- **Example:**
  ```ruby
  # Creating a range
  num_range = 1..5

  # Iterating over the range
  num_range.each { |num| puts num }
  # Output: 1, 2, 3, 4, 5
  ```

### 5. **Enumerables:**

- **Definition:**
  - Modules providing collection classes with traversal and searching methods.

- **Example:**
  ```ruby
  # Using enumerable methods
  numbers = [1, 2, 3, 4, 5]

  # Map (transform)
  squared_numbers = numbers.map { |num| num**2 }
  # Output: [1, 4, 9, 16, 25]

  # Select (filter)
  even_numbers = numbers.select { |num| num.even? }
  # Output: [2, 4]

  # Reduce (accumulate)
  sum = numbers.reduce(0) { |acc, num| acc + num }
  # Output: 15
  ```

### 6. **Strings:**

- **Definition:**
  - Although not traditionally considered a collection, strings in Ruby behave as a collection of characters.

- **Example:**
  ```ruby
  # Using string methods
  greeting = "Hello, Ruby!"

  # Iterating over characters
  greeting.each_char { |char| puts char }
  # Output: H, e, l, l, o, ,,  , R, u, b, y, !

  # String manipulation
  uppercase_greeting = greeting.upcase
  # Output: HELLO, RUBY!
  ```

### Conclusion:

Collections in Ruby provide versatile ways to organize and manipulate data. Arrays and hashes are fundamental for storing and accessing multiple values, while sets ensure uniqueness. Ranges and enumerables enhance the capabilities of iteration and manipulation, making Ruby a powerful language for working with collections. Understanding these collections is essential for effective Ruby programming.
