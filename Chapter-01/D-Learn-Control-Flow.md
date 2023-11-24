# Control Flow

Control flow structures in Ruby allow you to dictate the flow of execution in a program, making decisions based on conditions and controlling the repetition of certain code blocks. Here's a detailed overview of control flow operations in Ruby:

### 1. **Conditionals (if, else, elsif):**

- **if Statement:**
  - Executes a block of code if a specified condition is true.

  ```ruby
  # Example
  x = 5
  if x > 0
    puts "x is positive"
  end
  ```

- **else Statement:**
  - Executes a block of code if the condition specified in the if statement is false.

  ```ruby
  # Example
  x = -3
  if x > 0
    puts "x is positive"
  else
    puts "x is non-positive"
  end
  ```

- **elsif Statement:**
  - Allows for the evaluation of additional conditions if the initial `if` condition is false.

  ```ruby
  # Example
  x = 0
  if x > 0
    puts "x is positive"
  elsif x < 0
    puts "x is negative"
  else
    puts "x is zero"
  end
  ```

### 2. **Ternary Operator (? :):**

- A concise way to write simple if-else statements.

  ```ruby
  # Example
  x = 7
  message = x > 5 ? "Greater than 5" : "Not greater than 5"
  puts message
  ```

### 3. **Case Statement:**

- A more concise way to express conditional statements with multiple branches.

  ```ruby
  # Example
  day = "Wednesday"
  case day
  when "Monday", "Tuesday"
    puts "It's a weekday"
  when "Saturday", "Sunday"
    puts "It's the weekend"
  else
    puts "It's another day"
  end
  ```

### 4. **Unless Statement:**

- Executes a block of code unless a specified condition is true.

  ```ruby
  # Example
  x = 10
  unless x < 5
    puts "x is not less than 5"
  end
  ```

### 5. **Logical Operators (&&, ||, !):**

- Used to combine or negate conditions.

  ```ruby
  # Example
  age = 25
  if age >= 18 && age <= 30
    puts "You are between 18 and 30 years old"
  end
  ```

### Conventions:

- **Indentation:**
  - Use two spaces for indentation to enhance readability.

  ```ruby
  # Example
  if condition
    # indented block
  else
    # indented block
  end
  ```

- **Parentheses:**
  - Parentheses around the condition are optional but can be used for clarity.

  ```ruby
  # Example
  if (x > 0)
    # code block
  end
  ```

### Conclusion:

Understanding control flow is crucial for writing effective and expressive Ruby programs. These structures allow us to create dynamic, decision-based logic, making our code responsive to different scenarios. As we work with more complex programs, mastering control flow will empower us to create versatile and robust applications in Ruby.
