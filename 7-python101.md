# Python 101

## Today 15 Sep 2020

Today, it is Episode 2 on the [CyberMentor's page](https://www.thecybermentor.com/zero-to-hero-pentesting).

**This tutorial uses Python3.**

### Python Course References

Heath is suggesting a few websites to learn Python.

- Cybrary's [Python for Security Professionals](https://www.cybrary.it/course/python-security-professionals-archive/), but this may not be free. It used to be nice on this site a few years ago when things were free. But no more!
- Codecademy's [Learn Python 3](https://www.codecademy.com/learn/learn-python-3). I think this is still not free.

> I don't think we need his advices on finding resources on learning python. We have done enough in the past in terms of finding resources and experimenting with learning the subject itself. Better follow my own path!

The goal of this episode is not to make us good with python. But we will be able to do what we did on bash in the last episode. And another goal is to be able to read the code and understand.

> Heath says you can make career in pentesting without ever knowing python.

### Let's jump right in!!

```
touch python101.py
chmod +x python101.py
```

Heath covered printing for some time. Not taking much notes here for this part.

#### Inside Vi

```py
#!/bin/python3

# Print String
print("Strings and things:")
print('Hello, world!')
print('''Hello, this is
a multi-line string!''')
print("This is"+"a string")


print('\n') # print a new line
# Math
print("Math time:")
print(50 + 50) # add
print(50 - 50) # subtract
print(50 * 50) # multiply
print(50 / 50) # divide
print(50 + 50 - 50 * 50 / 50) # PENDAS
print(50 ** 2) # exponents/powers
print(50 % 6) # modulo
print(50 // 6) # number without leftovers

print('\n') # print a new line

# Variables & Methods
print("Fun with Variables and Methods:")
quote = "All is fair in love and war!"
print(len(quote)) # Length of the String
print(quote.upper()) # All upper case
print(quote.lower()) # All lower case
print(quote.title()) # Title

name = "Anand"
age = 38 # int
gpa = 3.1 # float

print(int(age))
print(int(29.9)) # Doesn't not round, but skips the decimals
print("My name is " + name + " and I am " + str(age) + " years old.")

print('\n') # print a new line

age += 1 # Will add an year to the age and changes the value of the variable, so age is no longer what we set it to be.
print(age)

birthday = 1
age += birthday
print(age)

print('\n') # print a new line

# Functions
print("Now, some functions:")
def who_am_i():
  name = "Anand"
  age = 38
  print("My name is " + name + " and I am " + str(age) + " years old.")

who_am_i()

# Adding parameters into Functions
def add_one_hundred(num):
  print(num + 100)

add_one_hundred(100) # Output should be 200

# Adding multiple parameters into functions
def add(x,y):
  print( x + y )

add(7,7)
add(305,207)

# Using Return instead of Print
def multiply(x,y):
  return x * y

print(multiply(7,7))

def square_root(x):
  return x ** .5

print(square_root(64))

print('\n') # print a new line

print("Here at this stage, somebody in the audience suggested to write a function for printing a new line.")
print("That is cute! :-)")

# Boolean Expressions (True or False)
print("Boolean Expressions:")
bool1 = True
bool2 = 3 * 3 == 9
bool3 = False
bool4 = 3 * 3 != 9

print(bool1, bool2, bool3, bool4)
print(type(bool1))

bool5 = 'True'
print(type(bool5))

print('\n') # print a new line

# Relational and Boolean Operators
greater_than = 7 > 5
less_than = 5 < 7
greater_than_equal_to = 7 >= 7
less_than_equal_to = 7 <= 7

print(greater_than, less_than, greater_than_equal_to, less_than_equal_to)

test_and = (7 > 5) and (8 < 7)
test_or = (7 > 5) or (5 < 7)
test_not = not True
print(test_and, test_or, test_not) # For this whole part, check out what are called Truth Tables

print('\n') # print a new line

# Conditional Statements
print("Conditional Statements:")
def soda(money):
  if money >= 2:
    return "You've got yourself a soda!"
  else:
    return "No soda for you! :-()"

print(soda(3))
print(soda(1))

print('\n') # print a new line

print("Tipsy stuff below!")

def alcohol(age,money):
  if (age >= 21) and (money >=5):
    return "We're getting tipsy!"
  elif (age >= 21) and (money < 5):
    return "Come back with more money!"
  elif (age < 21) and (money >= 5):
    return "Nice try, kid!"
  else:
    return "You're too poor and too young!"

print(alcohol(21,5))
print(alcohol(21,4))
print(alcohol(18,4))

print('\n') # print a new line

# Lists
print("Lists have brackets:")
movies = ["When Harry Met Sally", "The Hangover", "The Perks of Being a Wallflower", "The Exorcist"]

print(movies[1]) # prints the second item, because lists begin with 0th item.
print(movies[0]) # for the first item in the list

print(movies[0:2]) # prints only the ones before 2nd, but not the 2nd item.
print(movies[0:]) # prints all items till the last one
print(movies[0:1]) # again prints only the first item in the list
print(movies[-1]) # prints the last item in the list
print(len(movies))

movies.append("Jaws") # adding to the list as the item
print(movies)

movies.pop() # removes the last item from the list
print(movies)
movies.pop(1) # removes the second item in the list
print(movies)

movies = ["When Harry Met Sally", "The Hangover", "The Perks of Being a Wallflower", "The Exorcist"]
person = ["Heath", "Jake", "Leah", "Jeff"]
combined = zip(movies, person) # combines two lists and create a list with tuples inside it.
print(list(combined))

print('\n') # print a new line

# Tuples
print("Tuples have parentheses and cannot change - Immutable")
grades = ("A", "B", "C", "D", "F")
print(grades[1])

print('\n') # print a new line

# looping
print("FOR Loops - Start to finish of iterate:")
vegetables = ["cucumber", "spinach", "cabbage"]

for x in vegetables:
  print(x)

print("WHILE Loops - Execute as long as True:")

i=1
while i < 10:
  print(i)
  i += 1
```
