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
    './(.py file)
```

## Comments
- [#] Comment
    - ignored by compiler
- ["""] Multiline string
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
    - ''' triple quoted multiline string - each new line is represented with: \n

#### Boolean
Determine if True or False (if or not to do something)

### Numbers:
    - Int: integer - 0 ->
    - Float: rational numbers (decimals) - <- 0 ->
        - Float operations evaluate to a float

#### Number Systems
There is more than one way to represent a number
    - Decimal:
        - base is 10
            - 0-9
    - Binary: 1111
        - base is 2
            - 0-1
        - in Python: Prefix- 0b
            - 0b1001
    - Octal:
        - base is 8
            - 0-7
        - in Python- 0o
            - 0o7242
    - Hexadecimal
        - base is 16
            - 0-F (0-9 + A-F)
        - in Python- 0x
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

#### Operators:
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

#### Methods:

>Objects are used to encapsulate the state and behavior (funcationality)
>Methods define the behavior with a period and method name


`"This string".find('r') = 7`
- 7 is the index, 'r' is positioned at the 7 index
- index starts at 0

`"LOWERCASE THE STRING".lower() = 'lowercase the string'`

Escape Sequence:

- Tab: Tab\
- New Line: \n
- Escape: \

Quotes inside quotes:
- "'Single' inside Double"
- '"Double" inside single'
- "\"Double\" escaped by Double"










































































# Syntax Errors:

"Starts with a double, ends with a single'
Syntax Error: EOL whie scanning string literal
    EOL: End of Line
Fix: quote marks must be the same on both sides of the string
