# Mixins :: Practice and Answers

Here are five challenges related to mixins in Ruby along with code solutions:

#### **Challenge 1: Create a Mixin for String Formatting:**
Create a mixin module that adds formatting methods to a class representing text.

```ruby
module StringFormatter
  def capitalize_words
    split.map(&:capitalize).join(' ')
  end

  def reverse_words
    split.reverse.join(' ')
  end
end

class Text
  include StringFormatter

  attr_accessor :content

  def initialize(content)
    @content = content
  end
end

text = Text.new('ruby programming is fun')
puts text.capitalize_words # Outputs: Ruby Programming Is Fun
puts text.reverse_words   # Outputs: fun is programming ruby
```

#### **Challenge 2: Implement Mixins for Mathematical Operations:**
Create mixins for addition, subtraction, and multiplication operations and apply them to a class representing a numeric value.

```ruby
module Addition
  def add(value)
    self + value
  end
end

module Subtraction
  def subtract(value)
    self - value
  end
end

module Multiplication
  def multiply(value)
    self * value
  end
end

class NumericValue
  include Addition
  include Subtraction
  include Multiplication

  attr_accessor :value

  def initialize(value)
    @value = value
  end
end

number = NumericValue.new(5)
puts number.add(3)        # Outputs: 8
puts number.subtract(2)   # Outputs: 3
puts number.multiply(4)   # Outputs: 20
```

#### **Challenge 3: Mixins for Collection Operations:**
Implement mixins for operations like filtering and mapping on a collection class.

```ruby
module Filterable
  def filter(&block)
    select(&block)
  end
end

module Mappable
  def custom_map(&block)
    map(&block)
  end
end

class CustomCollection < Array
  include Filterable
  include Mappable
end

collection = CustomCollection.new([1, 2, 3, 4, 5])
filtered_result = collection.filter { |item| item.even? }
mapped_result = collection.custom_map { |item| item * 2 }

puts filtered_result.inspect  # Outputs: [2, 4]
puts mapped_result.inspect    # Outputs: [2, 4, 6, 8, 10]
```

#### **Challenge 4: Mixins for Observable Pattern:**
Extend the observable pattern example to allow removing observers.

```ruby
module Observable
  def add_observer(observer)
    @observers ||= []
    @observers << observer
  end

  def remove_observer(observer)
    @observers&.delete(observer)
  end

  def notify_observers(data)
    @observers&.each { |observer| observer.update(data) }
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

agency.remove_observer(subscriber1)

agency.publish_news('Python 4.0 Released')
# Outputs:
# Publishing news: Ruby 3.0 Released
# Received news: Ruby 3.0 Released
# Received news: Ruby 3.0 Released
# Publishing news: Python 4.0 Released
# Received news: Python 4.0 Released
```

#### **Challenge 5: Mixins for Logging with Levels:**
Create a logging mixin that supports different logging levels.

```ruby
module Logging
  LOG_LEVELS = %i[info warning error].freeze

  def log(message, level = :info)
    raise ArgumentError, 'Invalid log level' unless LOG_LEVELS.include?(level)

    puts "[#{level.to_s.upcase}] #{message}"
  end
end

class LoggableClass
  include Logging

  def perform_operation
    log('Performing operation...', :info)
    # ... operation logic ...
    log('Operation completed successfully.', :info)
  rescue StandardError => e
    log("Operation failed: #{e.message}", :error)
  end
end

logger = LoggableClass.new
logger.perform_operation
```

These challenges cover various aspects of mixins in Ruby, from creating mixins for specific behaviors to implementing reusable modules for common operations. They showcase the flexibility and modularity that mixins bring to Ruby programming.
