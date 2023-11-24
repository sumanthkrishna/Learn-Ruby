# Exception Handling :: Practice and Answers

Here are five challenges related to exception handling in Ruby along with code solutions:

#### Challenge 1: **Handle File Not Found Exception:**
Create a program that reads data from a file. Handle the case where the file does not exist.

```ruby
begin
  file = File.open("nonexistent_file.txt", "r")
  data = file.read
  puts "Data from file: #{data}"
rescue Errno::ENOENT => e
  puts "Error: #{e.message}. File not found."
end
```

#### Challenge 2: **Division by Zero Exception:**
Write a program that takes user input for two numbers and performs division. Handle the case where the user tries to divide by zero.

```ruby
begin
  print "Enter numerator: "
  numerator = gets.chomp.to_i
  print "Enter denominator: "
  denominator = gets.chomp.to_i

  result = numerator / denominator
  puts "Result of division: #{result}"
rescue ZeroDivisionError => e
  puts "Error: #{e.message}. Division by zero is not allowed."
end
```

#### Challenge 3: **Custom Exception Handling:**
Define a custom exception class and use it in a program to handle a specific error scenario.

```ruby
class CustomError < StandardError
  def message
    "This is a custom error!"
  end
end

begin
  # Code that may raise a custom exception
  raise CustomError
rescue CustomError => e
  puts "Custom Error: #{e.message}"
end
```

#### Challenge 4: **Handle Input Validation:**
Create a program that takes user input for age and ensures that the input is a valid positive integer.

```ruby
begin
  print "Enter your age: "
  age = Integer(gets.chomp)

  if age < 0
    raise ArgumentError, "Age must be a positive integer."
  else
    puts "Your age is: #{age}"
  end
rescue ArgumentError => e
  puts "Error: #{e.message}"
rescue StandardError => e
  puts "Unexpected error: #{e.message}"
end
```

#### Challenge 5: **Nested Exception Handling:**
Write a program that performs a series of operations on an array. Handle potential exceptions at different levels.

```ruby
begin
  array = [1, 2, 3]
  
  begin
    # Code that may raise an exception
    result = array[4] + 5
  rescue IndexError => e
    puts "Error accessing array element: #{e.message}"
  end

  # Additional operations that may raise exceptions
  result = array.map { |item| item / 0 }
rescue ZeroDivisionError => e
  puts "Error: #{e.message}. Division by zero."
rescue StandardError => e
  puts "Unexpected error: #{e.message}"
end
```

These challenges cover various aspects of exception handling, including file operations, user input validation, custom exceptions, and nested exception handling. They provide opportunities to practice handling different types of errors in Ruby programs.
