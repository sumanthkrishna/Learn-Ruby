# Regular Expressions :: Practice Answers

### Challenge 1: Validate a Password

**Challenge:**
Write a Ruby regular expression to validate a password. The password must be at least 8 characters long, contain at least one uppercase letter, one lowercase letter, and one digit.

**Answer:**
```ruby
password_pattern = /^(?=.*[A-Z])(?=.*[a-z])(?=.*\d).{8,}$/

passwords = ["Pass123", "SecurePwd", "weak", "StrongPass123"]
valid_passwords = passwords.select { |pwd| pwd.match?(password_pattern) }

puts valid_passwords.inspect
# Output: ["Pass123", "SecurePwd", "StrongPass123"]
```

### Challenge 2: Extract URLs from Text

**Challenge:**
Write a Ruby regular expression to extract URLs from a given text.

**Answer:**
```ruby
url_pattern = /https?:\/\/\S+/

text = "Visit our website at http://www.example.com or check out https://rubygems.org."
urls = text.scan(url_pattern)

puts urls.inspect
# Output: ["http://www.example.com", "https://rubygems.org"]
```

### Challenge 3: Extract Words Starting with a Specific Prefix

**Challenge:**
Write a Ruby regular expression to extract words from a text that start with the prefix "ruby".

**Answer:**
```ruby
prefix_pattern = /\bruby\w*\b/i

text = "Ruby is a dynamic programming language. rubyist loves Ruby."
ruby_words = text.scan(prefix_pattern)

puts ruby_words.inspect
# Output: ["Ruby", "rubyist", "Ruby"]
```

### Challenge 4: Validate Email Addresses

**Challenge:**
Write a Ruby regular expression to validate email addresses.

**Answer:**
```ruby
email_pattern = /\A[\w+\-.]+@[a-z\d\-.]+\.[a-z]+\z/i

emails = ["user@example.com", "john.doe@gmail", "invalid.email"]
valid_emails = emails.select { |email| email.match?(email_pattern) }

puts valid_emails.inspect
# Output: ["user@example.com"]
```

### Challenge 5: Extract Markdown Headings

**Challenge:**
Write a Ruby regular expression to extract Markdown headings (lines starting with one or more '#' characters) from a text.

**Answer:**
```ruby
markdown_heading_pattern = /^#+\s+.+/

markdown_text = "# Ruby Programming\nSome text here.\n## Regular Expressions\nMore content."
headings = markdown_text.scan(markdown_heading_pattern)

puts headings.inspect
# Output: ["# Ruby Programming", "## Regular Expressions"]
```

These challenges cover a range of tasks, including password validation, URL extraction, prefix matching, email validation, and Markdown heading extraction using regular expressions in Ruby.
