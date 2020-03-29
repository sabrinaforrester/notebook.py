# Lab 1
## Making Calculations from User Input with Python
### A simple tool to perform temperature conversions from Farenheit to Celsius
#### What you need to know:
- Handling user input the 'input' function.
- Type casting strings to floats. 
- Printing to the screen.

#### Solution:
`# Prompt and store Fahrenheit Value from User`
`fahrenheit = float(input(What temperature (in Fahrenheit) would you like converted into Celsius?))`
- The user input is expected to be a number, so it needs to be captured as such for the future conversion.

`# Calculating the Celsius Value`
`celsius = (fahrenheit - 32) * 5/9

`# Print the Calculated Value to the Screen`
`print(fahrenheit, "F is", celsius, "C")`