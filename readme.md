# Python Entry Level Programmer Certification

## What is a Complier?
Translates code from one type (high level) to another(low level). For example: a compiler translates source code (what I write in Python) to Machine code.

#### 5 Steps of Compilation
1. Lexical Analysis: Breaks up source code into identified tokens (How the language classifies each text[ID, EQUALS, RPAREN, LPAREN, TIMES, NUM, DIV, PLUS])
2. Syntax Analysis (Parsing): Constructs a parse tree using the tokens provided by the lexer. Parsing provides more context about how the code should run.
3. Semantic Analysis: Applies the language rules to the parse tree. This includes raising errors when rules are broken.
4. Optimization: Rewrites source code to be more efficient
5. Code Generation: Generates code onto the machine

## What is an Interpreter?
Executes source code directly or via a compilation process.

#### Interpreter Strategies
1. Parse source code and execute directly
2. Compile to intermediate form (bytecode) and then execute

## Python Keywords
Reserved words that can't be used as identifiers in code.
|          |          |          |          |          |          |          |
|----------|----------|----------|----------|----------|----------|----------|
| Finally | None | break | except | in | raise | True |
| await | class | finally | is | return | and | continue |
| else | for | lambda | try | as | def | from |
| import | nonlocal | while | assert | del | global | not |
| pass | with | async | elif | if | or | yield |

## Bytecode Instructions
Various commands that the Python virtual machine knows how to run. Python is an interpreted programming language, but source code is compiled to bytecode before being run.

## Make Executable File
Code in the .py file:
```
    #!/usr/bin/env python3.7

    print("Hello, World!")
```

In the terminal:
```
    $ chmod u+x ~/(.py file)
    Run script with:    ./(.py file)    from the home directory.
```

## Comments
- [#] Comment
    - ignored by compiler
- [```] Multiline string
    - commonly mistaken as block comment (non-existent in python)
    - compiler runs to create string - takes up space in memory`

## Variables
Format:
- [identifier] [assign] [value]
`x = 1`

> Variables are not statically typed - meaning a variable can be of different data types

## Data Types
#### Strings: 
> Collection of character to store words (textual data)
    - String Literals
        - 'single quoted string'
        - "double quoted string"
    - ``` triple quoted multiline string - each new line is represented with: \n
> Default encoding is unicode UTF 8
    > Unicode Transformation Format, values stored in 8 bits
    - ord('a')
        - returns 97, the code point for the letter a
    - chr(97)
        - returns 'a'
        - hexadecimal value of the code point may also return the original string
            - ord('\hexadecimal')
#### Methods
> Function tied to the item and provides functionality knowing the state of the object
    `my_string = 'Testing'
    - `my_string.lower()`
        - returns 'testing'
    - `my_string.upper()-`
        - returns 'TESTING'
    - `my_string.capitalize()`
        - returns 'Testing'
    - "once upon a time".title()
        - returns 'Once Upon A Time'
> **.is**... methods checks the contents of the string
    - my_string.isascii()
    - my_string.islower()
    - my_string.isupper()
    - my_string.istitle()
    - my_string.isspace()
    - my_string.isdecimal()
        - returns true for integers, returns false for floats
    - my_string.isdigit()
        - returns true for integers, returns false for floats
    - my_string.isnumeric()
        - returns true for integers, returns false for floats
    - my_string.isalpha()
    - my_string.isalnum()
    - my_string.isidentifier()
        - returns true if follows variable naming qualifiers
    - my_string.isprintable()
        - returns false for escape characters
> Strings can be used as tokens
    - phrase = "This is a simple phrase"
    - words = phrase.split()
        - returns ['This', 'is', 'a', 'simple', 'phrase']
    - url = "https://example.com/users/jimmy"
    - user = url.split('/')[-1]
        - returns 'jimmy'
    - url.split('/')
        - returns ['https:', '', 'example.com', 'users', 'jimmy']
    - ", ".join(words)
        - returns 'This, is, a, simple, phrase]
> Format
    - template = "Hello, my name is {}, and I really enjoy {}. Have a nice day!"
    - template.format('Jamie', 'Python')
        - providing more values than available argument spaces, the extra will be ignored
        - providing less values cause an error
    - "Hello, my name is {0}, and I really enjoy {1}. Have a nice day! - {0}".format('Jamie', 'Python')
        - works well for using the same value multiple times

> ASCII
    > Can only handle letters numbers and punctuation
    > Extended can hold 256 code point

#### Boolean
Determine if True or False (if or not to do something)

#### Numbers:
    - Int: integer - 0 ->
    - Float: rational numbers (decimals) - <- 0 ->
        - Float operations evaluate to a float

#### Number Systems
There is more than one way to represent a number
- Decimal:
    - base is 10
        - 0-9
- Binary:
    - base is 2
        - 0-1
    - in Python: Prefix- 0b
            - 0b1001
- Octal:
    - base is 8
        - 0-7
    - in Python: Prefix- 0o
        - 0o7242
- Hexadecimal
    - base is 16
        - 0-F (0-9 + A-F)
    - in Python: Prefix- 0x
        - 0xFF012

Conversion:
```
    Decimal to Binary for 15
        Least Significant   15/2 = 7 with remainder 1
                            7/2 = 3 with remainer 1
                            3/2 = 1 with remainder 1
        Most Significant    1/2 = with remainder 1
```
```
    Binary to Decimal for 0b1111
        [(1 * 2^3) + (1 * 2^2) + (1 * 2^1) + (1 * 2^0)]
            8 + 4 + 2 + 1
                15
```

#### Floating-Point Accuracy
- Stored as binary fractions in memory.
- Not all decimals can be represented as binary fractions.
- Decimal numbers that cannot be represented are approximated

## Operators
```
Addition
+
combine strings
"pass" + "word" = 'password'
```
```
Multiplication
*
repeat string n times
"Do" * 4 = DoDoDoDo
```
```
Division
/
returns a float
```
```
Floor division
//
returns the integer excluding the remainder
```
```
Modulo
%
returns the remainder as an integer
0 means the input evenly divides
```
```
Exponential
**
```
#### Operator Binding
>How to handle order of operations with many operators
1. Parenthesis
    - ()
2. List
    - []
3. Function
4. Exponents
    - **
5. Positive or Negative
    - (+/-)1
6. Bitwise Complement
    - ~
7. Multiplication
    - \*
8. Div
    - /
9. Floor Division
    - //
10. Mod
    - %
11. Add
    - \+
12. Sub
    - \-
13. Bitwise
    1. AND
    2. XOR
    3. OR
14. Shift

#### Bitwise
>Compare each binary digit in the same position
- AND &
    - both must be true
    - 0b1001 & 0b1100 = 0b1000
- OR  |
    - either can be true
    - 0b1001 | 0b1100 = 0b1101
    - if either digit is a one then 1 is printed for that position.
- XOR ^
    - only one true value otherwise false
    - 0b1001 ^ 0b1100 = 0b101
- NOT
    - returns the opposite

#### Shift Operators
>Compares binary numbers with integers. Change binary representation by moving to the right or left direction.
- Right Shift
    - `a = b110`
    - `bin(a >> 2) = 0b1`

- Left Shift
    - `a = 0b110`
    - `bin(a << 2) = 0b11000`

#### Boolean Operators
- NOT
    - returns the opposite
- OR
    - returns true if there at least one true value
- AND
    - returns true only if both values are true

#### Comparison Operators
>Returns True or False for every operator. Comparisons can be  made for different data types
- Less than
    - <
- Greater than
    - \>
- Greater than or equal to
    - \>=
- Less than or equal to
    - <=
- Equivalent
    - ==
- Not Equal
    - !=
- Identity
    - is
        - `1 is 1.0 = False`
        - `[] is [] = False` because empty lists are modifiable
        - id() memory location
- Negate Identity
    - is not
`'A' <= 'a' = True`
`ord('a') = 97 ord('A') = 65`

## Methods:
>Objects are used to encapsulate the state and behavior (funcationality)
>Methods define the behavior with a period and method name


`"This string".find('r') = 7`
- 7 is the index, 'r' is positioned at the 7 index
- index starts at 0

`"LOWERCASE THE STRING".lower() = 'lowercase the string'`

## Escape Sequence:

- Tab: Tab\
- New Line: \n
- Escape: \

## Quotes inside quotes:
- "'Single' inside Double"
- '"Double" inside single'
- "\"Double\" escaped by Double"

## Type Casting
- float()
    - `float(1) = 1.0`
- int()
    - `int(1.3) = 1`
    - `int('1') = 1`
- str()
    - `str(1.0) = '1.0'`
- bool()
    - `bool(1) = True`
    - `bool(0) = False`
    - `bool('') = False`
    >Anything zero or similar to zero is False, such as empty lists.
    ```
    'and' without boolean works differently by not returning True or False. Instead it returns the first value that is False or the last True value if it is all True:
    1 and 0 returns 0
    'This' and 'That' returns 'That'
    ```
    ```
    'or' returns the first True value or the last False value if they are all False:
    1 or 0 returns 1
    0 or "" returns ''
    ```
    ```
    'not' returns the opposite True or False value:
    not "" returns True
    not 1 returns False
    ```

## Input
- input()
    - built-in function to prompt the user for input
    - Function may be used empty 
        - input()
    - Function may be used with a message to the user
        - input(Enter text)

- print()
    - (function) print: (*values, sep: str, end: str, file: Option al[_Writer], flush: bool) -> None
`name = input("What is your name?")`
    `color = input("What is your favorite color?")`
    `age = int(input("How old are you today?"))`

- end is the string that is added to the end of the string being printed
    `print(name, end=" ")`
    `print("is " + str(age) + " years old", end=" ")`
    `print("and loves the color" + color + ".", end=" ")`
    
- sep is the seperater string
    `print(name, 'is, age, 'years old and loves the colr', color + '.', sep=" ")`
    - single space is the default seperator

## Immutability
> It cannot be changed.
- Strings are immutable.
- Lists are mutable
- Not all sequence types are immutable.

## Length
>Returns the length or number of characters.
`len()`
- The last index of any string is `len() - 1`

## Indexing
> Returns the character that is in requested position.
- Always starts at zero
`string_index = "indexing"`
`string_index[5] = 'i'`
`string_index[-5] = 'e'`
- Negative indexing returns the character in the string reading right to left.
    - Always starts at one.

##Slicing
> Specify ranges of indexes to return a specific segment of a string
- string[starting index, ending index, step value]
`string_splice = "splicing"`
- Return from one position to the end of the string.
    - Manually
        - `string_splice[3:7] = 'icing'`
    - Using len()
        - `string_splice[3:len(string_splice)] = 'icing'`
    - Blank
        - `string_splice[3:] = 'icing'`
- Return every other character in the string beginning with index 1
    `string_splice[1:7:2] = 'pii'`
- Return every other character in the string beginning with index 0
    `string_splice[:7:2] = 'slcn'`
- Reverse string order
    `string_splice[::-1] = 'gnicilps'`

## Lists
> Batch up a collection of other items (booleans, integers, floats, strings)
### Create a list
    - `my_list = ["apple", 4.5, 2, True]`
    - items within a list do not all have to be the same
### Index a list
    - `my_list = ["apple", 4.5, 2, True]`
    - `my_list[0]`
        - returns "apple"
    > IN / NOT IN
        - "apple" **in** my_list
            - returns True
        - "banana" **not in** my_list
            - returns True
### Length of list
    - 'len(my_list)'
        - returns 5
### Slice a list
    - slice from one index to another
        - `my_list[0:2]`
    - slice from one index to the end of the list
        - `my_list[1:]`
    - slice from the beginning of the list to one index
        - `my_list[:3]`
    - stepping by one
        - `my_list[0::1]`
### Mutability
    - Change the value of an index
        - `my_list[2] = 'x'`
            - my_list = ['apple', 4.5, 'x', True]
        - `my_list[1:3] = ['elephant', 'donkey']
            - my_list = ['apple', 'elephant', 'donkey', True]
            - the length of the replacement values does not have to be the same, the list will just grow to include all.
    - Concatenate lists
        - `my_list + ["banana", 7.3, 'z', False]`
            - this does not make a change to my_list
        - `my_list += ["banana", 7.3, 'z', False]`
            - this creates a new list then reassigns it
    - Remove items from a list
        - replace list items with an empty value
            - my_list = ['a', 'b', 'c', 'd', 'e', 'f']
                - `my_list[3:] = []`
                - returns ['a', 'b', 'c']
        - use del statement (not a function)
            - my_list = ['a', 'b', 'c', 'd', 'e', 'f']
                - `del my_list[0]`
                - returns ['b', 'c', 'd', 'e', 'f']
            - `del my_list`
                - deletes the variable that stores the list
### Functions
    > Append([value]) takes an item and puts it on the end of a list
        - my_list = [1, 2, 3]
            - `my_list.append(4)`
            - returns [1, 2, 3, 4]
    > Insert([location], [value]) 
        - my_list = [1, 2, 3]
            - `my_list.insert(0,0)`
            - returns [0, 1, 2, 3, 4]
    > Sorted()
        - my_list = [1, 2, 3, 6, 5, 4]
            - `sorted(my_list)`
            - returns [1, 2, 3, 4, 5, 6]
                - it returns a new sorted list
    > Reversed()
        - my_list = [1, 2, 3, 6, 5, 4]
            - `list(reversed(my_list))`
            - returns [4, 5, 6, 3, 2, 1]
                - reversed(my_list) returns a list_reverseiterator object
            - `list(reversed(sorted(my_list)))`
            - returns [6, 5, 4, 3, 2, 1]
### Matrix
        - nested lists to form a 2-dimensional data structure with rows and columns
            - my_matrix = [[1, 2, 3], [4, 5, 6]]
                - row_count = len(my_matrix)
                    - returns 2
                - column_count = len(my_matrix[0])
                    - returns 3
            - index values of the matrix
               ``` | Col 1  | Col 2  | Col 3  |
                   |--------|--------|--------|
                   | [0][0] | [0][1] | [0][2] |
                   | [1][0] | [1][1] | [1][2] | ```
            - Square
                - a matrix with a two rows and two columns
            - Cube
                - a matrix with the same number of rows and columns
## Tuples
    > An immutable sequence type
        - Add one tuple to an existing tuple
            - point = (1.0, 2.0)
            - point_3d = point + (3.0,)
                - one tuples must have comma
                - returns 1.0, 2.0, 3.0
            - x, y, z = point_3d
                - assigns the tuple to x, y, and z respectively
## Dictionaries
    > Access a key and get its values (considered hashes or assorted arrays in other languages)
    - `ages = {'kevin': 59, 'alex': 29, 'bob': 40}`
        - keys are immutable and should be unique
### Subscribing
    - getting the value of the key
        - ages['kevin']
        - returns 59
### Mutability
    - Add a key and value to the dictionary
        - ages['kayla'] = 21
            - returns {'kevin': 59, 'alex': 29, 'bob': 40, 'kayla': 21}
    - Modify the value of a key
        - ages['kevin'] = 60
            - returns {'kevin': 60, 'alex': 29, 'bob': 40, 'kayla': 21}
    - Removal
        - Remove key
            - del ages['kevin']
        - Remove dictionary
            - del ages
    - In / Not In
        - alexa **in** ages
            - returns False
### Creating a dictionary
    - Dict function
        - weight = dict(kevin=160, bob=240, kayla=135)
    - Tuples
        - color = dict([('kevin', 'blue'), ('bob', 'green'), ('kayla', 'red')])
### Methods
    - ages = {'kevin':61, 'bob':79}
    - return keys
        - `ages**.keys()**`
    - return keys as a list
        - `list(ages.keys())`
    - return values
        - `ages**.values()**`
    - return keys and values
        - `ages**.items()**`
        
## Conditionals
> If/else statements
    - if 'a' < 'b':
        print("Condition was true")
      else:
        print("Condition was false")
> Elif
    - if 'b' < 'a':
        print("This is true")
      elif 'c' < 'd':
        print("Second condition was true")
      else:
        print("no condition was true")
> Else defined
    - name = "jamie"
    - if name == "James"
        print("Hello James")
      else:
        pass
            - place holder
## Looping
> Bundle logic and repeat usually based on conditions
### While Loop
> Good for iterating an unknown or infintie number of times
```
while 1<2:
    print("something")
```
- returns an infinite loop
```
count = 1
while count <= 4:
    print("looping")
    count += 1
```
-The while loop print "looping" starting at 1 and restarting after the variable increments, once the variable has reached its limit, the while loop will stop.

### For Loop
> Iterates using a temporary variable(name doesn't matter)
```
colors = ['blue', 'green', 'red', 'purple']
for color in colors:
    print(color)
```
> For loop through a dictionary to print the keys
```
ages = {'kevin': 59, 'bob': 40, 'kayla': 21}
for key in ages:
    print(key)
```
> For loop through a dictionary to print the items
```
ages = {'kevin': 59, 'bob': 40, 'kayla': 21}
for key, value in ages:
    print(key,value)
```
> For loop through a string
```
for letter in 'my_string':
    print(letter)
```
    - returns the each character of the string
### Nesting Conditionals and Loops
> indenting can get crazy
```
counter = 1
while counter <= 25:
   if counter % 4 == 0:
        printer(counter)
    counter += 1
```
    - prints multples of four up to 25
### Stop Looping
> **Continue** pauses the rest of loop until the conditional completes its full iteration
```
count = 0
while count < 10:
    if count % 2 == 0:
        count += 1
        continue
    print(f"We are counting numbers odd numbers: {count}")
    count += 1
```
    - f is a string iterpolation similar to format
    
> **Break** stops the exceution of the loop enitrely
```
count = 1
while count < 10:
    if count % 2 == 0:
        break
    print(f"We're counting odd numbers: {count}")
    count += 1
```
    - This will only return once and will break after reaching two.
### Else
> Define another code context to execute when the loop finshes successfully
```
count = 1
while count <= 4:
    print(count)
    count += 1
else:
    print("While loop completed)
```
```
colors = ['red', 'pink', 'blue', 'orange', 'green']
for color in colors:
    if color == 'orange'
        print('Orange is in the list')
        break
else:
    print('Orange is not in the list')
```
    - only use else with a break

### Range
> Provise the next item when iteratoring, does not calculate the next item until requested
> Increment over a *non-existent* sequential list or a certain number of times
- my_range = range(10)
- list(my_range)
    - returns all integers from 0 to 10 in a list
- range(starting index, stopping index, stepping value)
    
```
for _ in range(4):
    print("looping")
```
   - _ conventional way of saying a variable is not needed     

### Loop Comprehension
> Easy to read and can be used for filtering
```
colors = ['red', 'blue', 'orange', 'green', 'yellow']
uppercase_colors = []

for color in colors:
    uppercase_colors.append(color.upper())
```
    - changes each value of the original list to uppercase then adds it to a new list of the same length
```
colors = ['red', 'blue', 'orange', 'green', 'yellow']
uppercase_colors = [color.upper() for color in colors]
```
    - yields the same result using list comprehension
```
colors = ['red', 'blue', 'orange', 'green', 'yellow']
warm_colors = [color for color in colors if color in ['red', 'orange', 'yellow']]
```

## Functions
> Group chunks of code to reusable blocks that can have defined parameters to pass variables then return a result or action
    - functions that start with an underscore or usually hidden functions
```
def print_name(name):
    print(f"Name is {name}")
```
    - *def* creates a function
    - *name* is the parameter
    - output = print_name("Jamie")
        - does not return a value because there is nothing to return
        
```
def add_two(num)
    **return** num + 2
```
    - result = add_two(2)
        - returns 4
### Parameters vs Arguments
> Parameters: variable defined when defining the function
> Arguments: values passed for the parameters

```
def contact_card(name, age, car_model):
    return f:{name} is {age} and drives a {car_model}"
```
- `contact_card(age=29, car_model="Honda Civic", name="Jamie")
    - returns the arguments in the correct order using assignment
    - order doesn't matter with assignment looking operation
    
> Keyword Arguments are useful when long list of arguments have defaults but only one needs to be modified
> Parameters can have default arguments but once called all parameters being called after need to have default arguments
```
def can_drive(age, driving_age=16):
    return age >= driving_age
```
    - driving_age has a default value for comparison
        - can_drive(29) returns true

### Recursion
> Call a function from within itself
    > There are limits to recursion

> Fibonnaci Sequence
    > 1, 1, 2, 3, 5, 8, 13,...
    > f(n) = f(n - 2) + f(n - 1)
    ```
    f(5) = f(3) + f(4)
    f(5) = f(1) + f(2) + f(2) + f(3)
    f(5) = 1 + f(0) + f(1) + f(0) + f(1) + f(1) + f(2)
    f(5) = 1 + 0 + 1 + 0 + 1 + 1 + f(0) + f(1)
    f(5) = 1 + 0 + 1 + 0 + 1 + 1 + 0 + 1
    f(5) = 5
```
def fib(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
        
    return fib(n-2) + fib(ni1)
calculation = int(input("What Fibonnaci item would you like to calculate? "))
print(fib(calculation))
```

## Generators
> Similar to range but starting with the stopping index
```
def gen_range(stop, start, step = 1)
    num = start
    while num <- stop:
    yield num
    num += step
```
- yield is like a return that pauses until it gets the next item
- next calculates the next number in the generator until the end of the iteration

```
def gen_range(stop, start=1, step = 1)
    num = start
    while num <- stop:
    yield num
    num += step
```
- generator = gen_range(10)
  list(generator)
    - returns [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
   
 > Generators with Fibinnaci Sequence  
```
def gen_fib():
    a, b = 0, 1
    while True:
        a, b = b, a + b
        yield a
```
- fib = gen_fib()
  next(fib)
  list(fib)
    - turning an infinite generator into a list will get killed because the list will never end
    
> Create a list using a generator by limiting restricting the iteration
- fib = gen_fib()
  [next(fib) for _ in range(50)][-1]
    - returns the 50th number in the sequence
        - get the next fibonnaci sequence value for the last value in the range from 0 to 50
        
## Scopes
> Variables and objects are only accessible within certain scopes

```
if 1 < 2:
    x = 5
    
while x< 6:
    print(x)
    x += 1
print(x)
```
- returns 5 then 6
- conditionals and loops do not define their own scopes

> Name hiding: variable names that match parameter names
> Shadowing: 
```
y = 5
def set_x(y):
    print("Inner y:", y)
    x = y
    y = x
    
set_x(10)

print("Outer y:", y)
```
- parameters win out over variables with the same name at a higher context

> Global keyword
- parameters win over global variables
```
y = 5
def set_x(z):
    print("Inner y:", y)
    x = z
    global y
    global a
    y = x
    a = 7
    
print("y before set_x:", y
    
set_x(10)

print("y after set_x:, y)
print("a after set_x:, a)
```






















































# Errors:
```
"Starts with a double, ends with a single'
Syntax Error: EOL whie scanning string literal
    EOL: End of Line
Fix: quote marks must be the same on both sides of the string
```
```
'a' <= 1
TypeError: '<=' not supported between instances of 'str' and 'int'
Fix: cannot compare different data types to one another
```
```
int('1.2')
ValueError: invalid literal for int() with base 10: '1.2'
Fix: 1.2 is not a normal interger in the decimal system so it cannot be converted from a string to an integer
```
```
test_str = 'testing'
test_str[18]
IndexError: string index out of range
Fix: 18 is more than the number of indexes of test_str. Reduce the number to be between 0 and 7
```
```
point = (2.0, 3.0)
point[0] = 1
TypeError: 'tuple' object does not support item assignment
Fix: tuples cannot be modified
```
```
def print_name(name):
    print(f"Name is {name}")\
    
print_name()
TypeError: print_name() missing 1 required positional argument: 'name'
Fix: an argument should be defined in the parenthesis of the called function
```

```
def set_x():
    x = 5
set_x()

while x< 6:
    print(x)
    x += 1
print(x)
NameError: name 'x' is not defined
Fix: functions and classes define their own scope, the variables created inside the function remain inside the function
```
