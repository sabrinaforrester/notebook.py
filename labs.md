# Lab 1
## Making Calculations from User Input with Python
### A simple tool to perform temperature conversions from Farenheit to Celsius
#### What you need to know:
- Handling user input the 'input' function.
- Type casting strings to floats. 
- Printing to the screen.

#### Solution:
`# Prompt and store Fahrenheit Value from User` <br \>
`fahrenheit = float(input(What temperature (in Fahrenheit) would you like converted into Celsius?))` <br \>
- The user input is expected to be a number, so it needs to be captured as such for the future conversion.

`# Calculating the Celsius Value` <br \>
`celsius = (fahrenheit - 32) * 5/9` <br \>

`# Print the Calculated Value to the Screen` <br \>
`print(fahrenheit, "F is", celsius, "C")` <br \>