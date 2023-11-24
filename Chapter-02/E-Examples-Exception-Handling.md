# Exception Handling

Here are five different examples of exception handling in Ruby:

#### 1. **Handling Specific Exception:**
   ```ruby
   begin
     # Code that may raise an exception
     result = 10 / 0
   rescue ZeroDivisionError => e
     puts "Error: #{e.message}"
   end
   ```

#### 2. **Handling Multiple Exceptions:**
   ```ruby
   begin
     # Code that may raise an exception
     file = File.open("nonexistent_file.txt", "r")
   rescue Errno::ENOENT, Errno::EACCES => e
     puts "Error: #{e.message}"
   end
   ```

#### 3. **Using `else` with Exception Handling:**
   ```ruby
   begin
     # Code that may raise an exception
     result = 10 / 2
   rescue ZeroDivisionError => e
     puts "Error: #{e.message}"
   else
     puts "No exception occurred. Result: #{result}"
   end
   ```

#### 4. **Using `ensure` for Cleanup:**
   ```ruby
   begin
     # Code that may raise an exception
     file = File.open("example.txt", "w")
     file.write("Hello, world!")
   rescue IOError => e
     puts "Error writing to file: #{e.message}"
   ensure
     file.close if file
   end
   ```

#### 5. **Handling Custom Exceptions:**
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

These examples cover a range of scenarios, including handling specific exceptions, multiple exceptions, using `else` for no-exception cases, using `ensure` for cleanup, and creating and handling custom exceptions. Understanding and using these patterns will help you write more robust and resilient Ruby code.
