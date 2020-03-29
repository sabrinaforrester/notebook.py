# Lab 1
## Making Calculations from User Input with Python
### A simple tool to perform temperature conversions from Farenheit to Celsius
#### What you need to know:
- Handling user input the 'input' function.
- Type casting strings to floats. 
- Printing to the screen.

#### Solution:
`# Prompt and store Fahrenheit Value from User` <br />
`fahrenheit = float(input(What temperature (in Fahrenheit) would you like converted into Celsius?))` <br />
- The user input is expected to be a number, so it needs to be captured as such for the future conversion.

`# Calculating the Celsius Value` <br />
`celsius = (fahrenheit - 32) * 5/9` <br />

`# Print the Calculated Value to the Screen` <br />
`print(fahrenheit, "F is", celsius, "C")` <br />

# Lab 2
## Indexing and Slicing Python Strings
### Print different peices of information about a string back to the user.
#### What you need to know:
- Working with string literals
- Indexing and slicing strings
- Printing to the screen

#### Solution
`# Take user input` <br />
`message = input("Enter a message: ")` <br />

`#Print the First, Last, and Middle characters from the user's input` <br />
`print("First Character:", message[0])` <br />
`print("Last Character:", message[-1])` <br />
`print("Middle Character:", message[int( len(message) /2 )])` <br />

`#Print the Even and Odd index characters` <br />
`print("Even Index Character:"), message[0::2])` <br />
`print("Odd Index Character:"), message[1::2])` <br />

`#Print the string in Reverse` <br />
`print("Reversed Message:"), message[::-1])` <br />