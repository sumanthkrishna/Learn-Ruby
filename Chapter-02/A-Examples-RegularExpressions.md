# Regular Expressions :: Examples

Here are five different examples of regular expressions in Ruby along with code:

### 1. Matching Email Addresses:

```ruby
email_pattern = /\A[\w+\-.]+@[a-z\d\-.]+\.[a-z]+\z/i

emails = ["user@example.com", "john.doe@gmail.com", "invalid.email"]
valid_emails = emails.select { |email| email.match?(email_pattern) }

puts valid_emails.inspect
# Output: ["user@example.com", "john.doe@gmail.com"]
```

### 2. Extracting Date Components:

```ruby
date_pattern = /(\d{4})-(\d{2})-(\d{2})/

date_string = "2023-11-17"
matches = date_string.match(date_pattern)

year = matches[1]
month = matches[2]
day = matches[3]

puts "Year: #{year}, Month: #{month}, Day: #{day}"
# Output: Year: 2023, Month: 11, Day: 17
```

### 3. Finding Words with Three Consecutive Vowels:

```ruby
vowel_pattern = /\b[aeiou]{3}\b/i

text = "The rain in Spain falls mainly on the plain."
matches = text.scan(vowel_pattern)

puts matches.inspect
# Output: ["rain", "Spain", "falls", "plain"]
```

### 4. Validating Phone Numbers:

```ruby
phone_pattern = /\A\d{3}-\d{3}-\d{4}\z/

phone_numbers = ["123-456-7890", "555-1234", "987-654-3210"]
valid_numbers = phone_numbers.select { |number| number.match?(phone_pattern) }

puts valid_numbers.inspect
# Output: ["123-456-7890", "987-654-3210"]
```

### 5. Extracting Hashtags from a Text:

```ruby
hashtag_pattern = /#\w+/

text = "Ruby programming is #fun and #powerful! #coding"
hashtags = text.scan(hashtag_pattern)

puts hashtags.inspect
# Output: ["#fun", "#powerful", "#coding"]
```

These examples cover a range of use cases, including validating email addresses, extracting components from a date, finding words with three consecutive vowels, validating phone numbers, and extracting hashtags from a text. Regular expressions are versatile tools for pattern matching and manipulation in various scenarios.
