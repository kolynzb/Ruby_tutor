# Ruby Cheatsheet

- Ruby was created by Maximoto. He wanted to focus on programmer productivity.
- Utilizes garbage collector.
- Uses `.rb` extention.

## Contents

- [Basics](#hello-world)
- [Ruby on Rails]()

## Resourses

- [Ruby in One Video](https://youtu.be/8wZ2ZD--VTk)
- [code](./main.rb)

<figure align="center">
<img width="300" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/73/Ruby_logo.svg/1024px-Ruby_logo.svg.png" alt="ruby logo"/>
</figure>

## Hello World

- Printing
  `print "Hello "`

- Print with new line

  `puts "World"`

## Comments

- Single line comments are prefixed with `//`
- Multiline comments

```rb
=begin
    Comment goes here
=end
```

## Variables

- Is Dynamically typed

```rb
name = "Mike" # Strings
age = 100 # integer
gpa = 3.5 # float
is_tall = true # Boolean

puts "Yor name is #{name}"
```

## Concatenation

`puts "Your name is " + name `

## Type Casting

```rb
puts 3.14.to_i # to integer
puts 3.to_f # to float
puts "3.14".to_f  # to float
puts 3.to_s # to string
puts 100 + "3.14".to_f # to float
```

## Strings

```rb
greeting = "bonjour"
# indices   0123456

# String Length
puts greeting.length
# get a charater at an index
puts greeting[0]
# Slice
puts greeting[1,3]
# Check if it includes this substring or charater
puts greeting.include? "jou"

```

## Numbers

```rb
 # Basic Arithmetic
puts 2 * 3 # Multiplication
puts 2 ** 3  # Exponent
puts 10 % 3  # Modulus
puts 10 / 3.0  # int's and doubles
# Operations on two integers return an integer whereas operations containing a float return a float.

puts 10 + 8 * 3  # order of operations -> BODMAS

num = 10
num += 100 # increment
# += , -= , /= , *=
puts num

num = -36.8
puts num.abs() # absolute integer
puts num.round

# Math Class has useful numbers
puts Math.sqrt(num) # square root
puts num.log(0)
```

## Getting User Input

```rs
puts "Enter your name"
name = gets
name = gets.chomp # removes newline character added to by pressing enter key
```

## Array

```rb
lucky_nums = [0,"hhey",0x0f]

lucky_nums[0]
lucky_nums[-1]
#  slicing array
lucky_nums[2,3]
lucky_nums[2..4]
puts lucky_nums.length # array length
```

## N Dimensional Array

```rb
# 2D Array
num_grid = [ [3,5],[4,5]]
num_grid[0][0] = 99
```

## Array Methods

```rb
friends = []
friends.push("collo")# append value
friends.pop # removes last element
friends.reverse
friends.sort # sort alhabetically
puts friends.include? "collo" # Check if included
```

## Methods Or Functions

```rb
# Function declaration
def add_nums (num1 , num2=99)
    return num1 + num2
end

# Function call
puts add_nums(4,4)
```

## Conditionals

```rb

is_smart = true and false # and
is_smart = true or false # or
is_smart = !true # not
```

# Control Structures

```rb
# If statement
if is_smart
    puts "Noble Prize"
elsif !is_smart
    puts "Rat race"
else
    puts "right dee"
end
# Conditional operators
# > ,< ,>= ,<= ,!= ,== , String.equals

```

## Switch Statement

```rb
mark = "Z"
case mark
    when  "A"
        puts "hard"
    when  "F"
        puts "????"
    else
        puts "right dee"
end
```

## Dictionaries

```rb
test_grades = {
    "Andy" => "B+",
    :Stanley => "C",
    3 => 95.6
}

test_grades["Andy"] = "B-"
puts test_grades["Andy"]
puts test_grades[:Stanley]
puts test_grades[3]
```

## Loops

### While loop

```rb
index =1
while index <= 1
    puts index
    index += 1
end
```

### For Loop

```rb
# Numbers in a range of zero to 5
for index in 0..5
    puts index
end

#
5.times do |i|
    puts i
end

#
lucky_nums = [1, 2, 3, 4, 5]

for lucky_num in lucky_nums
    puts lucky_num
end

#
lucky_nums.each do |lucky_num|
    puts lucky_num
end
```

# Exception Catching / Error Handling

```rb
# division by zero error
begin
    num = 10/0
rescue  # catchs any error
    puts "Error"
end

# Catch specific error
begin
    puts bad_variable # error
    num = 10/0
rescue ZeroDivisionError
    puts "Error"
rescue
    puts "All Errors"
end

# raise an exception
# raise "Made Up Exception"
```

## OBJECT ORIENTED PROGRAMMING

- Every thing in ruby is an object.

```rb
class Book
    # attributes
    attr_accessor :title, :author

    # method
    def readBooks()
        puts "Reading #{self.title} by #{self.author}"
    end
end

#  new instance
book1 = Book.new()
book1.title = "Atomic Habits"
book1.author = " "

book1.readBook()
puts book1.title

```

### Constructors

```rb
class Animal
    attr_accessor :is_mammal, :gender
    # constructor
    def initialize(is_mammal, gender)
        @title = title # or self.title = title
        @gender = gender
    end

    def make_sound()
        puts "Animal #{self.is_mammal} #{gender}"
    end

    # setter
    def title=(title)
        puts "Set"
        @title = title
    end

    # getter
    def title=(title)
        puts "Get"
        return @title
    end

end

cow = Animal(true,"male")
```

## Inheritance

```rb
class Chef
    def make_chicken()
        puts "Make"
    end
    def make_salad()
        puts "Make"
    end
    def make_special_dish()
        puts "Make"
    end
end

class ItalianChef < Chef
    def make_pasta()
        puts "Make"
    end
    def make_pizza()
        puts "Make"
    end
    # Overide the original make special
    def make_special_dish()
        puts "Overide"
    end
end
```

## Inheritance

```rb
class Teacher
    attr_accessor :name,:age
    def initialize(name, age)
        @name = name
        @age = age
    end

    def teach()
        puts "Teaching"
    end
end

class Lecturer < Teacher
    attr_accessor :uni
    # Overiding the super / parent class constructor
    def initialize(name,age,uni)
        @uni = uni
        super(name,age)
    end

    def course_wrk()
        puts "Course"
    end
end
```
