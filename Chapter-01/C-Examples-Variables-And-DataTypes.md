# Practice Variables and Data Types

Here are five practice code snippets on "Variables and Data Types" in Ruby for you to practice:

1. **Concatenate Strings:**
   ```ruby
   # Practice Code
   # Prompt user to enter first and last names
   print "Enter your first name: "
   first_name = gets.chomp

   print "Enter your last name: "
   last_name = gets.chomp

   # Concatenate strings for greeting
   full_name = "#{first_name} #{last_name}"
   puts "Hello, #{full_name}!"
   ```

2. **Temperature Conversion:**
   ```ruby
   # Practice Code
   # Prompt user to enter temperature in Fahrenheit
   print "Enter temperature in Fahrenheit: "
   fahrenheit = gets.chomp.to_f

   # Convert Fahrenheit to Celsius
   celsius = (fahrenheit - 32) * (5.0/9.0)
   puts "Temperature in Celsius: #{celsius.round(2)}"
   ```

3. **Array Operations:**
   ```ruby
   # Practice Code
   # Create an array of numbers
   numbers = [3, 7, 1, 5, 9]

   # Print sum of all elements
   sum = numbers.sum
   puts "Sum of array elements: #{sum}"

   # Print largest and smallest elements
   largest = numbers.max
   smallest = numbers.min
   puts "Largest Element: #{largest}, Smallest Element: #{smallest}"

   # Append a new element to the array
   numbers << 4
   puts "Array after appending: #{numbers}"
   ```

4. **Hash Manipulation:**
   ```ruby
   # Practice Code
   # Create a hash representing a person
   person = { "name" => "John", "age" => 30, "city" => "New York" }

   # Print person's name
   name = person["name"]
   puts "Person's Name: #{name}"

   # Add new key-value pair for "occupation"
   person["occupation"] = "Engineer"
   puts "Updated Person Hash: #{person}"

   # Print all keys in the hash
   keys = person.keys
   puts "Keys in Person Hash: #{keys}"
   ```

5. **Boolean Operations:**
   ```ruby
   # Practice Code
   # Prompt user to enter a number
   print "Enter a number: "
   user_input = gets.chomp.to_i

   # Check if the number is even or odd
   is_even = user_input.even?
   puts "The number #{user_input} is #{is_even ? 'even' : 'odd'}."
   ```

Feel free to run and modify these code snippets to experiment and reinforce your understanding of variables and data types in Ruby.
