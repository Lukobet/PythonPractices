 # variables
price = 10
rating = 4.9
name = 'Mosh'
is_published = False
print(price)

# Example 1 : we checkin a patient named John Smith. He is 20 years old and is a new patient.

full_name = "John Smith"
age = 20
is_new = True

# Getting input from the user
name = input("what is your name? ") #the space after the ? is so that i can answer it on the terminal
print ("Hi " + name)

# Example 2 : Ask two questions: person's name and favourite color. Then, print a message like "Mosh likes blue"
name = input("what is your name? ")
favourite_color = input("what is your favourite colour? ")
print (name + " likes " + favourite_color) 



# Type conversion
birth_year = input('Birth year: ')
print(type(birth_year))
age = 2019 - int(birth_year)
print(type(age))
print(age)

# example 3: ask a user their weight (in pounds), convert it to kilograms and print on the terminal
weight_lbs = input('Weight (lbs): ')
weight_kg = int(weight_lbs) * 0.45
print(weight_kg)

