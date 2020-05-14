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

# Lab
## Python Syntax
### Create Purchasing Information and Receipts for Lovely Loveseats
#### Solution
```
#Create description and price variable for lovely loveseat
lovely_loveseat_description = '''
Lovely Loveseat. Tufted polyester blend on wood. 32 inches high x 40 inches wide x 30 inches deep. Red or white.
'''
lovely_loveseat_price = 254.00
```
```
#Create description and price variable for stylish settee
stylish_settee_description = '''
Stylish Settee. Faux leather on birch. 29.50 inches high x 54.75 inches wide x 28 inches deep. Black.
'''
stylish_settee_price = 180.50
```
```
#Create description and price variable for luxorious lamp
luxurious_lamp_description = '''
Luxurious Lamp. Glass and iron. 36 inches tall. Brown with cream shade.
'''
luxurious_lamp_price = 52.15
```
```
#Create and set sales tax variable
sales_tax = .088
```
```
#Create and set customers total and items, should start at zero since they have not added anythinf to their cart yet.
customer_one_total = 0

customer_one_itemization = ''
```
```
#Add prices and items to the customers total and list

customer_one_total += lovely_loveseat_price

customer_one_itemization += lovely_loveseat_description

customer_one_total += luxurious_lamp_price

customer_one_itemization += luxurious_lamp_description
```
```
#Compute and add the sales tax to the cutomers total

customer_one_tax = customer_one_total * sales_tax

customer_one_total += customer_one_tax
```
```
#Print the customers receipt

print('Customer One Items: ', customer_one_itemization)

print('Customer one Total: ', customer_one_total)
```
