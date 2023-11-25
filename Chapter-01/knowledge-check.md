##  Data Types:
**Question**: Explain the difference between nil and false in Ruby.

<details>
  <summary>Answer</summary>
In Ruby, nil represents the absence of a value or the absence of an object, while false is a boolean value indicating falseness. nil is an object of class NilClass, and false is an object of class FalseClass.
</details>

**Question**: What is the purpose of the && (logical AND) operator in Ruby, and how does it differ from and?
<details>
  <summary>Answer</summary>
  
**Answer**: Both && and and are logical AND operators. However, && has higher precedence than and. In practice, && is often used in control flow and conditions, while and is used for low-precedence logical operations within expressions.
</details>

## Lists (Arrays):
**Question**: How would you remove all duplicate elements from an array without using any Ruby built-in methods?
<details>
  <summary>Answer</summary>
  
**Answer**: One way to remove duplicates without using built-in methods is by iterating through the array and building a new array with unique elements.
</details>

**Question**: Can you explain the difference between map and each when working with arrays in Ruby?
<details>
  <summary>Answer</summary>
  
**Answer**: Both map and each iterate through each element of an array. However, map creates a new array based on the block's return values, while each is used for iteration without modifying the original array.
</details>

## Loops:
**Question**: Write a single-line Ruby code to print the numbers from 1 to 10 using the times method.

<details>
  <summary>Answer</summary>
  
**Answer**: 10.times { |i| puts i + 1 }
</details>

**Question**: How do you break out of a loop prematurely in Ruby?

<details>
  <summary>Answer</summary>
  
**Answer**: The break keyword is used to exit a loop prematurely in Ruby.
</details>

## Conditions:
**Question**: What is the difference between == and === in Ruby when used for equality comparison?

<details>
  <summary>Answer</summary>
  
**Answer**: While == is used for general equality comparison, === is often used for more specific comparisons, such as in case statements. However, their behavior depends on the context and the classes involved.
</detail>

**Question**: Explain the concept of the ternary operator in Ruby and provide an example.

<details>
  <summary>Answer</summary>
  
**Answer**: The ternary operator (?:) is a concise way to express a conditional. Example: condition ? true_value : false_value.
</details>

## Mixed Concepts:
**Question**: Given an array of integers, how would you find the sum of all even numbers greater than 10?
<details>
  <summary>Answer</summary>
  
**Answer**: array.select { |num| num.even? && num > 10 }.sum
</details>

**Question**: Write a Ruby code snippet to determine if a year is a leap year or not, considering the leap year rule (divisible by 4 but not divisible by 100 unless divisible by 400).
<details>
  <summary>Answer</summary>
  
**Answer**:
```

def leap_year?(year)
  (year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)
end
```
</details>

These **Question**s are designed to assess a candidate's understanding of Ruby's data types, array manipulation, loop constructs, and conditional statements. The **Answer**s provided aim to guide discussions and help evaluate the candidate's problem-solving skills.
