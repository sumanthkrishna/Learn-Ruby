# Mixins : Examples

Here are five different examples of mixins in Ruby:

#### **1. Mixin for Logging:**
```ruby
module Logging
  def log(message)
    puts "[LOG] #{message}"
  end
end

class Calculator
  include Logging

  def add(a, b)
    result = a + b
    log("Added #{a} and #{b} to get #{result}")
    result
  end
end

calculator = Calculator.new
calculator.add(3, 5) # Outputs: [LOG] Added 3 and 5 to get 8
```

#### **2. Mixin for Authentication:**
```ruby
module Authentication
  def authenticate(username, password)
    if username == 'admin' && password == 'secret'
      puts 'Authentication successful'
    else
      puts 'Authentication failed'
    end
  end
end

class AdminTool
  include Authentication

  def access_admin_panel(username, password)
    authenticate(username, password)
    puts 'Accessing admin panel...'
  end
end

admin_tool = AdminTool.new
admin_tool.access_admin_panel('admin', 'secret') # Outputs: Authentication successful, Accessing admin panel...
```

#### **3. Mixin for Enumerable Operations:**
```ruby
module CustomEnumerable
  def custom_map
    result = []
    each { |item| result << yield(item) }
    result
  end
end

class CustomList
  include Enumerable
  include CustomEnumerable

  def initialize(items)
    @items = items
  end

  def each(&block)
    @items.each(&block)
  end
end

list = CustomList.new([1, 2, 3, 4])
mapped_list = list.custom_map { |item| item * 2 }
puts mapped_list.inspect # Outputs: [2, 4, 6, 8]
```

#### **4. Mixin for Comparable Behavior:**
```ruby
class Book
  include Comparable

  attr_accessor :title, :pages

  def initialize(title, pages)
    @title = title
    @pages = pages
  end

  def <=>(other)
    pages <=> other.pages
  end
end

book1 = Book.new('Ruby Programming', 300)
book2 = Book.new('Python Basics', 250)

puts book1 > book2 # Outputs: true
```

#### **5. Mixin for Observable Pattern:**
```ruby
module Observable
  def add_observer(observer)
    @observers ||= []
    @observers << observer
  end

  def notify_observers(data)
    @observers.each { |observer| observer.update(data) }
  end
end

class NewsAgency
  include Observable

  def publish_news(news)
    puts "Publishing news: #{news}"
    notify_observers(news)
  end
end

class NewsSubscriber
  def update(news)
    puts "Received news: #{news}"
  end
end

agency = NewsAgency.new
subscriber1 = NewsSubscriber.new
subscriber2 = NewsSubscriber.new

agency.add_observer(subscriber1)
agency.add_observer(subscriber2)

agency.publish_news('Ruby 3.0 Released')
# Outputs:
# Publishing news: Ruby 3.0 Released
# Received news: Ruby 3.0 Released
# Received news: Ruby 3.0 Released
```

These examples demonstrate the versatility of mixins in Ruby, showcasing how they can be used for various purposes such as logging, authentication, custom enumerable operations, providing comparable behavior, and implementing the observable pattern.
