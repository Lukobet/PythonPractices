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

# strings
course = "Python's course for Beginners"
# we had to use double "" here now '' because the python word carries an apostrophe
print(course)
# imagine we want to want the word beginners in a quote we will need the whole words to be in single quote then put the beginners in a double quote just like below
course = 'Pyhton for "Beginners"'
print(course)

# when you want a strings with multiple quotes
course = '''
Hi John 

Here is our first email to you.

THank you,

THe support team

'''

print(course)


# when you want a square brackets to get index of characters in the letters
course = 'Python for Beginners'
# could be 0 to 9 or even -0 to -9. check the oicture for the result
print(course[-5])

# when you want a square brackets syntax to get index of characters in the letters
course = 'Python for Beginners'
print(course[0:3])

# this will give you the letters from 0 to 3 but exclude the next letter check the picture
print(course[0:5])

# if dont specify the end index
print(course[0:])
# if i dont specify the start index but gave an end index
print(course[:5])

## if i dont specify any index
course = 'Python for Beginners'

print(course[:])

# or in did it this way
course = 'Python for Beginners'
another = course[:]

print(another)


# example 
name = 'Jennifer'
print(name[1:-1])

# formatted strings(used for a dynamic text with my variables)

first = 'John'
last = 'Smith'
# with this 2 variables i want to generate a text like this: (John [Smith] is a coder)
message = first + ' [' + last + '] is a coder'
print(message)

# but this above method is not idle to visualize it. the best method is a fromatted strings which is below
first = 'John'
last = 'Smith'
msg = f'{first} [{last}] is a coder'

print(msg)

# strings methods
course = 'Python for Beginners'
# to calculate (count) the total number of characters in the sentence use len
print(len(course))

# to convert characters in the sentence to lower case or upper case use .
print(course.upper())
print(course.lower())

# to find the index of the character in the sentence use find 
print(course.find('P'))
print(course.find('B'))
print(course.find('r'))
print(course.find('Beginners')) #here the result will be to give use the index of the first letter


# to replace character in the sentence use replace
print(course.replace('Beginners', 'Absolute Beginners'))

# or
print(course.replace('P', 'J'))


# to check the existence of a character in the sentence use in
print('Python' in course)

# or

print('python' in course)


# This will give us a  BULLION VALUE I.E True or False


# Arthimetic Operations supported in Python