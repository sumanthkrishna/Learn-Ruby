# Variables, Scope

In Ruby, variables are used to store and manipulate data. Ruby has different types of variables, each serving a specific purpose. Here are details about different types of variables in Ruby:

### Local Variables:
Definition: Local variables are variables that are defined within a method or a block and are only accessible within that specific scope.

Naming Convention: Local variables begin with a lowercase letter or an underscore (_).

Example:

```ruby

def example_method
  local_variable = "I am a local variable"
  puts local_variable
end
```

### Instance Variables:
Definition: Instance variables are associated with a particular instance of a class. They start with the @ symbol.

Naming Convention: Instance variables begin with @.

Example:

```ruby

class Example
  def set_value(value)
    @instance_variable = value
  end
end
```

### Class Variables:
Definition: Class variables are shared among all instances of a class. They start with @@.

Naming Convention: Class variables begin with @@.

Example:

```ruby

class Example
  @@class_variable = 0

  def increment_class_variable
    @@class_variable += 1
  end
end
```

### Global Variables:
Definition: Global variables are accessible throughout the entire program. They start with $.

Naming Convention: Global variables begin with $.

Example:

```ruby

$global_variable = "I am a global variable"
puts $global_variable
```

### Constants:
Definition: Constants are variables whose values should not be reassigned. They start with an uppercase letter.

Naming Convention: Constants begin with an uppercase letter.

Example:

```ruby

MY_CONSTANT = "I am a constant"
```

### Block Variables:
Definition: Block variables are used in blocks (e.g., within each or do...end constructs). They have local scope within the block.

Naming Convention: Block variables are typically single-letter variables or short names.

Example:

```ruby

array = [1, 2, 3]
array.each do |element|
  puts element
end
```
These are the main types of variables in Ruby, each with its own scope and use. Understanding these variables is fundamental to writing effective and readable Ruby code. Remember to choose variable names that convey the purpose of the data they hold and adhere to the naming conventions for each variable type.
