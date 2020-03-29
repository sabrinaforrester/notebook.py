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