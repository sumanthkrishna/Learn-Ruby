# Object Oriented Programming :: Practice and Answers

Here are five challenges related to Object-Oriented Programming (OOP) in Ruby, along with their solutions:

### Challenge 1: Create a Class Hierarchy for Shapes

**Challenge:**
Create a class hierarchy for different shapes (circle, square, rectangle) with a common base class `Shape`. Implement methods to calculate the area for each shape.

**Solution:**
```ruby
class Shape
  def area
    raise NotImplementedError, "Subclasses must implement the area method."
  end
end

class Circle < Shape
  attr_accessor :radius

  def initialize(radius)
    @radius = radius
  end

  def area
    Math::PI * @radius**2
  end
end

class Square < Shape
  attr_accessor :side

  def initialize(side)
    @side = side
  end

  def area
    @side**2
  end
end

class Rectangle < Shape
  attr_accessor :length, :width

  def initialize(length, width)
    @length = length
    @width = width
  end

  def area
    @length * @width
  end
end
```

### Challenge 2: Implement a Library System

**Challenge:**
Create a class hierarchy for a library system with classes such as `Library`, `Book`, and `Member`. Implement methods for checking out and returning books.

**Solution:**
```ruby
class Book
  attr_reader :title, :author

  def initialize(title, author)
    @title = title
    @author = author
    @checked_out = false
  end

  def checkout
    return "Book is already checked out." if @checked_out

    @checked_out = true
    "Book checked out successfully."
  end

  def return_book
    return "Book is not checked out." unless @checked_out

    @checked_out = false
    "Book returned successfully."
  end
end

class Member
  attr_reader :name

  def initialize(name)
    @name = name
  end
end

class Library
  attr_reader :books, :members

  def initialize
    @books = []
    @members = []
  end

  def add_book(book)
    @books << book
  end

  def add_member(member)
    @members << member
  end
end
```

### Challenge 3: Create a Banking System

**Challenge:**
Design a banking system with classes like `Account`, `Transaction`, and `Customer`. Implement methods for deposit, withdrawal, and transaction history.

**Solution:**
```ruby
class Account
  attr_reader :balance, :transactions

  def initialize
    @balance = 0
    @transactions = []
  end

  def deposit(amount)
    @balance += amount
    @transactions << "Deposit: +#{amount}"
  end

  def withdraw(amount)
    return "Insufficient funds." if amount > @balance

    @balance -= amount
    @transactions << "Withdrawal: -#{amount}"
  end
end

class Customer
  attr_reader :name, :account

  def initialize(name)
    @name = name
    @account = Account.new
  end
end
```

### Challenge 4: Modeling a School System

**Challenge:**
Create classes for a school system with `Student`, `Teacher`, and `Course`. Implement methods for enrolling students, assigning teachers, and displaying course information.

**Solution:**
```ruby
class Student
  attr_reader :name, :courses

  def initialize(name)
    @name = name
    @courses = []
  end

  def enroll(course)
    @courses << course
    course.add_student(self)
  end
end

class Teacher
  attr_reader :name, :courses_taught

  def initialize(name)
    @name = name
    @courses_taught = []
  end

  def assign_course(course)
    @courses_taught << course
    course.assign_teacher(self)
  end
end

class Course
  attr_reader :name, :students, :teacher

  def initialize(name)
    @name = name
    @students = []
  end

  def add_student(student)
    @students << student
  end

  def assign_teacher(teacher)
    @teacher = teacher
  end

  def display_info
    puts "Course: #{@name}"
    puts "Teacher: #{@teacher.name}" if @teacher
    puts "Students: #{students.map(&:name).join(', ')}"
  end
end
```

### Challenge 5: Implement a Movie Rental System

**Challenge:**
Create classes for a movie rental system with `Movie`, `Customer`, and `Rental`. Implement methods for renting and returning movies, and display customer rental history.

**Solution:**
```ruby
class Movie
  attr_reader :title, :available

  def initialize(title)
    @title = title
    @available = true
  end

  def rent
    return "Movie not available." unless @available

    @available = false
    "Movie rented successfully."
  end

  def return_movie
    return "Movie not rented." if @available

    @available = true
    "Movie returned successfully."
  end
end

class Customer
  attr_reader :name, :rentals

  def initialize(name)
    @name = name
    @rentals = []
  end

  def rent_movie(movie)
    rental_status = movie.rent
    @rentals << "#{movie.title}: #{rental_status}"
  end

  def return_movie(movie)
    return_status = movie.return_movie
    @rentals << "#{movie.title}: #{return_status}"
  end

  def display_rental_history
    puts "#{name}'s Rental History:"
    puts rentals.join("\n")
  end
end
```

These challenges cover various aspects of Object-Oriented Programming in Ruby, including class hierarchy, encapsulation, inheritance, polymorphism, and modeling real-world scenarios.
