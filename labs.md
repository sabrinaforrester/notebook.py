# Lab 1
## Python Syntax
### Create Purchasing Information and Receipts for Lovely Loveseats
#### Solution

`#Create description and price variable for lovely loveseat` <br />
`lovely_loveseat_description = '''Lovely Loveseat. Tufted polyester blend on wood. 32 inches high x 40 inches wide x 30 inches deep. Red or white.'''` <br />
`lovely_loveseat_price = 254.00` <br />

`#Create description and price variable for stylish settee` <br />
`stylish_settee_description = '''Stylish Settee. Faux leather on birch. 29.50 inches high x 54.75 inches wide x 28 inches deep. Black.'''` <br />
`stylish_settee_price = 180.50` <br />

`#Create description and price variable for luxorious lamp` <br />
`luxurious_lamp_description = '''Luxurious Lamp. Glass and iron. 36 inches tall. Brown with cream shade.'''` <br />
`luxurious_lamp_price = 52.15` <br />

`#Create and set sales tax variable` <br />
`sales_tax = .088` <br />

`#Create and set customers total and items, should start at zero since they have not added anythinf to their cart yet.` <br />
`customer_one_total = 0` <br />
`customer_one_itemization = ''` <br />

`#Add prices and items to the customers total and list` <br />
`customer_one_total += lovely_loveseat_price` <br />
`customer_one_itemization += lovely_loveseat_description` <br />
`customer_one_total += luxurious_lamp_price` <br />
`customer_one_itemization += luxurious_lamp_description` <br />

`#Compute and add the sales tax to the cutomers total` <br />
`customer_one_tax = customer_one_total * sales_tax` <br />
`customer_one_total += customer_one_tax` <br />

`#Print the customers receipt` <br />
`print('Customer One Items: ', customer_one_itemization)` <br />
`print('Customer one Total: ', customer_one_total)` <br />

# Lab 2
## Getting Ready for Physics Class
### You are a physics teacher preparing for the upcoming semester. You want to provide your students with some functions that will help them calculate some fundamental physical properties.
#### Solution:
`#Turn up the Temperature` <br />

`def f_to_c(f_temp):` <br />
  `c_temp = (f_temp - 32)* 5/9` <br />
  `return c_temp` <br />
`f100_in_celsius = f_to_c(100)` <br />

`def c_to_f(c_temp):` <br />
  `f_temp = c_temp*(9/5) +32` <br />
  `return f_temp` <br />
`c0_in_fahrenheit = c_to_f(0)` <br />

`#Use the Force` <br />

```
train_mass = 22680
train_acceleration = 10
train_distance = 100
bomb_mass = 1
```

`def get_force(mass, acceleration):` <br />
  `return mass*acceleration` <br />
`train_force = get_force(train_mass, train_acceleration)` <br />
`print(train_force)` <br />
`print('The GE train supplies ' + str(train_force) + " Netwons of force.")` <br />

`def get_energy(mass, c = 3*10**8):` <br />
  `return mass*c**2` <br />
`bomb_energy = get_energy(bomb_mass)` <br />
`print('A 1kg bomb supplies ' + str(bomb_energy) + " Joules")` <br />

`#Do the work` <br />

`def get_work(mass, acceleration, distance):` <br />
  `force = get_force(mass, acceleration)` <br />
  `return force*distance` <br />
`train_work = get_work(train_mass, train_acceleration, train_distance)` <br />
`print('The GE train does ' + str(train_work) + ' of work over ' + str(train_distance) + ' meters.')` <br />


# Lab 2
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

# Lab 3
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


