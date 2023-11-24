# Variables and Data Types in Ruby

In Ruby, variables are used to store and manipulate data. The language is dynamically typed, meaning you don't have to explicitly declare the data type of a variable; it is determined at runtime. Here's a detailed overview of variables and the supported data types in Ruby:

### Variables:

1. **Variable Naming Conventions:**
   - Variable names begin with a lowercase letter or underscore.
   - Conventionally, multi-word variable names use underscores (`snake_case`).

   ```ruby
   # Valid variable names
   age = 25
   user_name = "John"
   ```

   ```ruby
   # Invalid variable name (starts with uppercase letter)
   InvalidName = "Invalid"
   ```

2. **Variable Assignment:**
   - Assign values using the `=` operator.

   ```ruby
   x = 10
   message = "Hello, Ruby!"
   ```

3. **Dynamic Typing:**
   - You don't need to declare the data type explicitly; Ruby determines it at runtime.

   ```ruby
   my_variable = 42      # Integer
   my_variable = "Ruby"  # String
   ```

### Data Types:

1. **Integer:**
   - Whole numbers without decimal points.

   ```ruby
   age = 25
   ```

2. **Float:**
   - Numbers with decimal points.

   ```ruby
   price = 19.99
   ```

3. **String:**
   - Sequences of characters enclosed in single or double quotes.

   ```ruby
   name = "Alice"
   greeting = 'Hello'
   ```

4. **Boolean:**
   - Represents true or false.

   ```ruby
   is_ruby_fun = true
   ```

5. **Array:**
   - Ordered collections of items.

   ```ruby
   numbers = [1, 2, 3, 4, 5]
   ```

6. **Hash:**
   - Unordered collections of key-value pairs.

   ```ruby
   person = { "name" => "John", "age" => 30, "city" => "New York" }
   ```

7. **Symbol:**
   - Lightweight, immutable identifiers.

   ```ruby
   status = :success
   ```

8. **Nil:**
   - Represents the absence of a value.

   ```ruby
   result = nil
   ```

### Example Code Snippets:

```ruby
# Variable assignment and data types
age = 25
price = 19.99
name = "Alice"
is_ruby_fun = true

# Array and Hash
numbers = [1, 2, 3, 4, 5]
person = { "name" => "John", "age" => 30, "city" => "New York" }

# Symbol and Nil
status = :success
result = nil
```

In the example above, we've used various variable names and assignments to different data types. The dynamic typing nature of Ruby allows the same variable to hold different types of values during the program's execution.

Understanding variables and data types is fundamental to writing effective Ruby code. As you explore more complex scenarios and build applications, you'll frequently work with these concepts to store and manipulate data.
