
# WHILE LOOPS
## This is used to execute a block of code multiple times and they are often used in building interactive programs and games.

```
i = 1
```
#i.e index = 1
## we write it like this (while condition:)
```
while i <= 5:
    print(i)
    i = i + 1 ## we increment i by 1 so tha i wont be 1 forever and end up wih infinte loop
    print("Done")
```
![Screenshot from 2024-09-27 04-47-43](https://github.com/user-attachments/assets/ff8644a4-0b07-41f5-97c3-9adbf099b8bc)


```
i = 1 

while i <= 5:
    print('*' * i) ## to make it more interesting
    i = i + 1 
    print("Done")
```
![Screenshot from 2024-09-27 04-52-46](https://github.com/user-attachments/assets/4c1b9d7f-cc2f-4169-a039-1a43792017ba)

## How to use a while loop to build a Guessing Game
### first thing is to define a variable to define a secret number

            ##### secret_number = 9
## we then need a while loop to ask a user to make  guess
####(while_condition:)
 ### we want to guess our users a maximum of 3 guesses
            ##### i = 0
            ##### while i< 3:
### replace the i with guess_count and also set a variable for the limit 

## after then thenuse the input function to make a guess
            ##### guess = int(input('Guess: '))
## then increment the guess_count
            ##### guess_count += 1
## then check to see if the user make the right guess
            ##### if guess == secret_number:
            #####   print('You won!')
### it will all look like this 
```
secret_number = 9
guess_count = 0
guess_limit = 3
while guess_count < guess_limit:
    guess = int(input('Guess: '))
    guess_count += 1
    if guess == secret_number:
        print('You won!')
        
```
![Screenshot from 2024-09-27 05-15-30](https://github.com/user-attachments/assets/f80f2191-43b5-4e22-b668-feebf6f451f0)

## this implementation those not have a message that i failed. 
## i tried using the correct guess first ad wrong answers after 

![Screenshot from 2024-09-27 05-18-24](https://github.com/user-attachments/assets/be589399-507d-42d2-8e47-56967b8af418)

## here it kept running even after the right answer because our while loop needs to be executed 3 times. we need to change the while loop in such a way that when the user gets the right answer it stops. to do this we use the break statement
              ##### break
#### its becomes this
```
secret_number = 9
guess_count = 0
guess_limit = 3
while guess_count < guess_limit:
    guess = int(input('Guess: '))
    guess_count += 1
    if guess == secret_number:
        print('You won!')
        break
```
![Screenshot from 2024-09-27 05-23-17](https://github.com/user-attachments/assets/871ce854-1fc7-4c9d-ad9a-d4cd769837e9)


### i need to input a failure message in my setup and also change and to do this i need to add an else in the while level
                #### else:
                #### print('Sorry you failed')
## it will now look like this
```
secret_number = 9
guess_count = 0
guess_limit = 3
while guess_count < guess_limit:
    guess = int(input('Guess: '))
    guess_count += 1
    if guess == secret_number:
        print('You won!')
        break
else:
    print('Sorry you failed')
 ```
![Screenshot from 2024-09-27 05-30-43](https://github.com/user-attachments/assets/ccf0f05c-7932-43f3-8abe-52e05c56180a)


 ## BUILDING A CAR GAME using while loops
```
command = "" #an empty string is a sting that has no chaacter in it. it just has the quote

while command.lower() != "quit":
    command = input(">")
    if command.lower() == "start":
        print("Car started...")
    elif command.lower() == "stop":
        print ("Car stopped.")
```

### looking at the above codes we have repeated words and this is bad, to solve this issue turn it to the below

```
command = ""

while command != "quit":
    command = input(">").lower()
    if command == "start":
        print("Car started...")
    elif command == "stop":
        print ("Car stopped.")
    elif command == "help":
        print("""
              start - to start the car
              stop - to stop the car
              quit - to quit
              """)
    else:
        print("Sorry, I don't understand this")

```
![Screenshot from 2024-10-07 05-22-15](https://github.com/user-attachments/assets/b0d74699-3a2c-42f4-a84c-dc963e11a0cc)
### looking at this  there is a lot of spce in the result for help command and also the quit result is not suppose to give any answwer.
```
command = ""
while True: ### remove the (command != "quit") and replace withh (True)
    command = input(">").lower()
    if command == "start":
        print("Car started...")
    elif command == "stop":
        print ("Car stopped.")
    elif command == "help":
        print(""" 
start - to start the car
stop - to stop the car
quit - to quit
              """)
    elif command == "quit": ### added this 
        break
    else:
        print("Sorry, I don't understand this !")

```
![Screenshot from 2024-10-07 05-29-59](https://github.com/user-attachments/assets/fd8ac0ad-6242-48d6-b7a1-5dd616c20bdb)

# to make the programme make sense, just incase the person tries to start or stop the car, there should be message to tell the person the car has been started ealrier or stopped.
```
command = ""
started = False
while True:
    command = input(">").lower()
    if command == "start":
        if started:
            print("Car is already started")
        else:
            started = True
            print("Car started...")
    elif command == "stop":
        if not started:
            print("Car is already stopped")
        else:
            started = False
            print ("Car stopped.")
    elif command == "help":
        print(""" 
start - to start the car
stop - to stop the car
quit - to quit
              """)
    elif command == "quit": 
        break
    else:
        print("Sorry, I don't understand this !")

```
![Screenshot from 2024-10-07 05-37-52](https://github.com/user-attachments/assets/589f4565-dcd1-4248-a4f0-9f0bc495eed9)


# FOR LOOPS
###  This is used to iterate over items of a collecton, such as string( a sequence of character)
### For example

```
for item in "Python":
    print(item)
```
![Screenshot from 2024-10-13 15-55-05](https://github.com/user-attachments/assets/9888ad65-2873-40c7-8719-188167369c4f)

####each character in the string is printed on new line.
### example 2 using square bracket[]

```
for item in ['Mosh', 'Josh', 'Sarah']:
    print(item)
```
![Screenshot from 2024-10-13 15-58-12](https://github.com/user-attachments/assets/56765f68-11e0-449a-ac8a-7b7631d677c0)
### WE can also loop over a list of numbers

```
for item in [1, 2, 3, 4]:
    print(item)
```
![Screenshot from 2024-10-13 16-00-32](https://github.com/user-attachments/assets/93d76f97-9e25-4bce-970e-1a458480a512)
### to interate over a large list of numbers we use the range function.

```
for item in range(10):
    print(item)
```
![Screenshot from 2024-10-13 16-02-42](https://github.com/user-attachments/assets/a1373b18-bbf6-4fe7-9f35-f90d79ff2364)
### we can also do this 
```
for item in range(5, 10):
    print(item)
```
![Screenshot from 2024-10-13 16-04-36](https://github.com/user-attachments/assets/7123f04f-bfc2-4271-802a-a483202e918a)
### it can also pass in steps(like sequences)

```
for item in range(5, 10, 2):
    print(item)
```
![Screenshot from 2024-10-13 16-06-12](https://github.com/user-attachments/assets/1db9842f-1a6a-479e-8fd9-6e6a6040fc55)
#### Exercise : Write a program to calculate the total cost of all the items in a shopping cart
```
prices = [10, 20, 30]

total = 0

for price in prices:
    total += price

print(f"Total: {total}")
```
![Screenshot from 2024-10-13 16-13-01](https://github.com/user-attachments/assets/d2884a33-9e66-46ab-8dec-5cfa30b337fd)

# NESTED LOOPS
## this means adding one loop into another loop. with this we can easily generate a list of cordinates, i.e a combination of x and y value (x, y) (0, 0) (0, 1) (0, 2) (1, 0) (1, 1) (1, 2)

```
for x in range(4):
    for y in range(3):
        print(f'({x}, {y})')
```
![Screenshot from 2024-10-13 16-23-19](https://github.com/user-attachments/assets/be484ce5-304d-4c7f-b763-2081639d55af)
### look at this it did for 0 first before going to 1 and 2 and 3 (all this are value for x)
### exercise: draw f shape 
xxxxx
xx
xxxxx
xx
xx

## to cheat use the below
```
numbers = [5, 2, 5, 2, 2]

for x_count in numbers:
    print('x' * x_count)
```
![Screenshot from 2024-10-13 16-33-34](https://github.com/user-attachments/assets/3f2d9e26-9679-4a67-bc38-5bbc5ccd7725)
### but the right way is 
```
numbers = [5, 2, 5, 2, 2]

for x_count in numbers:
    output = ''
    for count in range(x_count):
        output += 'x'
    
    print(output)
```
![Screenshot from 2024-10-13 16-37-18](https://github.com/user-attachments/assets/65f04cb1-2536-4e51-9f76-bc69d5eedb9e)
#### practice t get l shape

```
numbers = [1, 1, 1, 1, 5]

for x_count in numbers:
    output = ''
    for count in range(x_count):
        output += 'x'
    
    print(output)
```
![Screenshot from 2024-10-13 16-38-53](https://github.com/user-attachments/assets/038537ea-c150-424b-abbf-0682f91fe5d8)

# LISTS
### using index wi=hich can be negative(-)( this starts from the back or end of the list) or positive
```
names = ['Tosin', 'Mosh', 'Sola', 'Titi', 'Femi']

print(names[2])
```
![Screenshot from 2024-10-16 04-10-20](https://github.com/user-attachments/assets/019d0687-01b6-4c58-82a1-d779f6f06764)
![Screenshot from 2024-10-16 04-12-03](https://github.com/user-attachments/assets/cd4998de-f212-499e-9fbe-652631824fc4)
![Screenshot from 2024-10-16 04-12-24](https://github.com/user-attachments/assets/6e66a7e6-824a-468d-af7e-05f6afd35c4a)

#### using a colon((:) to pass range of items( this will pass the list from the index indicated to the end of the strings

```
names = ['Tosin', 'Mosh', 'Sola', 'Titi', 'Femi']

print(names[2:])
```
![Screenshot from 2024-10-16 04-16-19](https://github.com/user-attachments/assets/5d9db48d-26fb-45db-a045-8357c625d87a)

![Screenshot from 2024-10-16 04-17-11](https://github.com/user-attachments/assets/18e6c94d-d03f-449a-8d11-76a40802e322)
### we can also specify the last index but it wont display the item
```
names = ['Tosin', 'Mosh', 'Sola', 'Titi', 'Femi']

print(names[1:4])
```
![Screenshot from 2024-10-16 04-19-07](https://github.com/user-attachments/assets/bd8f05e1-bde4-4c01-bfcb-63e323e58c27)

### we can also modify the list. for instance we made a mistake in the spelling
```
names = ['Tosin', 'Mosh', 'Sola', 'Titi', 'Femi']
names[0] = 'Oluwatosin'
print(names)```
```
![Screenshot from 2024-10-16 04-22-46](https://github.com/user-attachments/assets/a7e2e5c5-ad7b-4590-83c1-8d4cd42f4d40)

### Exercise: Write a program to find the largest number in a list.

```
numbers = [3, 5, 2, 6, 8, 9, 10]
max = numbers[0]
for number in numbers:
    if number > max:
        max = number

print(max)
```
![Screenshot from 2024-10-16 04-28-53](https://github.com/user-attachments/assets/9bcd4f65-822d-4c95-aab3-863783dd3d85)

# 2 Dimensional Lists
## THis is a list in which each item in the list is in another list.
# List methods
```
numbers = [3, 5, 2, 6, 8, 9, 10]
numbers.append(20)

print(numbers)
```
##### number append adds numbers to the end of the list
![Screenshot from 2024-10-26 04-51-29](https://github.com/user-attachments/assets/c19315a7-6961-4d9d-a626-ca50d072d7c3)

##### but to add at the begining or middle use insert
```
numbers = [3, 5, 2, 6, 8, 9, 10]
numbers.insert(0, 10)

print(numbers)
```
## at the beginnijng
![Screenshot from 2024-10-26 04-54-21](https://github.com/user-attachments/assets/5d96b79f-3782-4918-9703-ae39a6727d22)
#### to remove 
```
numbers = [3, 5, 2, 6, 8, 9, 10]
numbers.remove(5)

print(numbers)
```
![Screenshot from 2024-10-26 04-56-17](https://github.com/user-attachments/assets/42ed92a9-69bd-4295-b310-7bcf37b026f3)
### to remove all the items in the list use clear

```
numbers = [3, 5, 2, 6, 8, 9, 10]
numbers.clear()

print(numbers)
```
![Screenshot from 2024-10-26 04-57-55](https://github.com/user-attachments/assets/869b5cef-7eb8-46e6-ac5f-337fbf302032)

#### to remove the last number in the list use pop
```
numbers = [3, 5, 2, 6, 8, 9, 10]
numbers.pop()

print(numbers)
```
![Screenshot from 2024-10-26 04-59-20](https://github.com/user-attachments/assets/2b1486c4-d067-43d7-90c9-6203d967f9e5)
#### to check for the existence of a number in a list use index
```
numbers = [3, 5, 2, 6, 8, 9, 10]


print(numbers.index(5))
```
![Screenshot from 2024-10-26 05-01-37](https://github.com/user-attachments/assets/6fa709de-6dae-4526-a8db-519172554628)
###### you get an error if you pass a wrong index
![Screenshot from 2024-10-26 05-03-03](https://github.com/user-attachments/assets/593f7ccd-cd18-4f15-967a-4bf8e8277f11)

##### checking the existence using an in operator and the response will in in buliion value (i.e True or False)

```
numbers = [3, 5, 2, 6, 8, 9, 10]

print(50 in numbers)
```
![Screenshot from 2024-10-26 05-04-57](https://github.com/user-attachments/assets/d573dc3c-f664-47db-af35-315697ff043e)
### to check how many times a number occurs in a list use count
```
numbers = [3, 5, 2, 5, 8, 9, 10]

print(numbers.count(5))
```
![Screenshot from 2024-10-26 05-07-58](https://github.com/user-attachments/assets/96c2ef97-249d-4a4c-8e11-c1118bb5233f)
#### if you want to sort your lists use sort
#### in ascending order

```
numbers = [3, 5, 2, 5, 8, 9, 10]
numbers.sort()
print(numbers)
```
![Screenshot from 2024-10-26 05-10-55](https://github.com/user-attachments/assets/cded40e8-be0c-41fc-9e4e-53290238c62c)
##### to sort in descending order include reverse.
```
numbers = [3, 5, 2, 5, 8, 9, 10]
numbers.sort()
numbers.reverse()
print(numbers)
```
![Screenshot from 2024-10-26 05-12-49](https://github.com/user-attachments/assets/d53f1cb5-f37d-4888-b31e-2e6ba7892110)

##### to get a copy of the list use copy
```
numbers = [3, 5, 2, 5, 8, 9, 10]
numbers2 = numbers.copy()
numbers.append(10)
print(numbers2)
```
![Screenshot from 2024-10-26 05-18-53](https://github.com/user-attachments/assets/b1fa62b9-3db9-4874-b40f-5e510080fdef)
#### looking at the above evn if we append a new number in the list it wont be displayed in numbers2 because they ar two independent list
#### Exercise: Write a program to remove the duplicates in a list
##### my solution

```
numbers = [3, 5, 2, 5, 8, 9, 10]
numbers.remove(5)

print(numbers)
```
#### this didnt remove the duplicates 
![Screenshot from 2024-10-26 05-22-37](https://github.com/user-attachments/assets/79f5c0ba-7552-4433-ad2c-75e4fd494b5d)```

```
numbers = [3, 5, 2, 5, 8, 2, 3, 9, 10]
uniques = []
for number in numbers:
    if number not in uniques:
        uniques.append(number)

print(uniques)
```
![Screenshot from 2024-10-26 05-26-35](https://github.com/user-attachments/assets/afd9894f-59f9-40f9-8b38-478ac2710b3b)
#### self try bring out just the numbers that has duplicates, couldnt get it
![Screenshot from 2024-10-26 05-33-07](https://github.com/user-attachments/assets/8b6b07b4-1ffd-461a-a4fc-076740070117)


# TUPLES
### These are similar to list, it can be used to store up listeof items like list, but unlike list we cannot modify them, we cannot add new itemms, we cannot remove existing items, it  immutable. we use square brackets[] to define lists and parenthesis() to define tuples. For instance: numbers = (1, 2, 3)
### UNPACKING
### for instances we have coordinates(1,2,3) and want to mulitply them , normally we are to do coordinates [0] * coordinates [1] * coordinates [2] or set them as variables as : x = coordinates [0] y = coordinates [1] z = coordinates [2], then do x * y * z. but in Tuples we do it like this:
```
coordinates = (1, 2, 3)
x, y, z = coordinates

print (y)
```
![Screenshot from 2024-11-11 04-15-28](https://github.com/user-attachments/assets/89fafd3c-658f-4497-888e-669033b3ca99)
* NOTE: this does not only work in Tuples we can also use it in lists. all we have to do is to change the parenthesis to square bracket
```
coordinates = [1, 2, 3]
x, y, z = coordinates

print (y)
```
![Screenshot from 2024-11-11 04-18-35](https://github.com/user-attachments/assets/8857d330-6484-4ce5-8d4a-b5926f629251)
# Dictionaries: These are used when we want to store information that comes as key  value pairs. For instance: Name : Tosin Aluko, Email: John@gmail.com, Phone: 1234. The keys here are name, email and phone while each of this keys has a value.
```
customer = {
    "name": "John Smith",
    "age" : 30,
    "is_verified": True
}
print(customer["name"])
```
![Screenshot from 2024-11-11 04-26-20](https://github.com/user-attachments/assets/2465521b-2eca-40e9-af7b-a60a3d2e6150)
#### normally if we pass a word that is not in the dictionary like burthname or Name the system will bring error but if we add .get and also change the square bracket to parenthesis it wont bring back error but say none

![Screenshot from 2024-11-11 04-29-55](https://github.com/user-attachments/assets/8ba45024-8f9d-4069-9070-1fc5d0e01b12)
```
customer = {
    "name": "John Smith",
    "age" : 30,
    "is_verified": True
}
print(customer.get("Name"))
```
![Screenshot from 2024-11-11 04-32-23](https://github.com/user-attachments/assets/a99f624f-6e3d-4a19-873e-a536b0541812)
##### we can also add a default value to it.
![Screenshot from 2024-11-11 04-36-08](https://github.com/user-attachments/assets/6b1f3ef9-734a-4e0c-8eda-753b2b461544)
##### we can also update the dictionary
```
customer = {
    "name": "John Smith",
    "age" : 30,
    "is_verified": True
}
customer["name"] = "Jack Smith"
print(customer["name"])
```
![Screenshot from 2024-11-11 04-40-22](https://github.com/user-attachments/assets/30cf71fc-383a-45fe-b264-b7c741951e1b)
EXERCISE: write a program the write  out a phone number in words like phone : 1234 ans is one two three four
```
phone = input("Phone: ")
digits_mapping = {
    "1": "One",
    "2": "Two",
    "3": "Three",
    "4": "Four"
}
output = ""
for ch in phone:
    output += digits_mapping.get(ch, "!") + " "

print(output)
```
![Screenshot from 2024-11-11 04-57-21](https://github.com/user-attachments/assets/4edb571f-0bc1-4bcc-a960-e820eb10739f)
# Emoji converter
Using dictionaries
```
message = input(">")
words = message.split(' ')
emojis = {
    ":)": "emoji symbol",
    ":(": "emoji symbol"
}
output = ""
for word in words:
    output += emojis.get(word, word) + " "

print(output)
```
# Functions
This is a container for a few lines of code that perform a specific task. Lets write a simple program for printing a greeting message. 

```
def greet_user():
    print('Hi there!')
    print('Welcome aboard!')


print("Start")
greet_user()
print("Finish")
```
![Screenshot from 2024-11-15 04-34-09](https://github.com/user-attachments/assets/b9c06b7f-e8aa-4efc-840b-f6fdd09839ea)
# parameters
use it to pass information to our functions

```
def greet_user(name):
    print(f'Hi {name}!')
    print('Welcome aboard!')


print("Start")
greet_user("John")
print("Finish")```
```
```
def greet_user(first_name, last_name):
    print(f'Hi {first_name} {last_name}!')
    print('Welcome aboard!')


print("Start")
greet_user("John", "Smith")
print("Finish")
```
![Screenshot from 2024-11-15 04-53-25](https://github.com/user-attachments/assets/add965b4-c9ea-4e33-b104-b856f5462b68)
#### parameters are the placeholder that we define in our function for receiving informations while arguments are the actual pieces of information that we supply for these functons.
## keyword Arguments
whenever we define a parameter for our functions we should always supply values otherwise we will get an error.

```
def greet_user(first_name, last_name):
    print(f'Hi {first_name} {last_name}!')
    print('Welcome aboard!')


print("Start")
greet_user(last_name="Smith", first_name="John")
print("Finish")
```
![Screenshot from 2024-11-15 05-04-32](https://github.com/user-attachments/assets/4e71b2e1-b39e-4ee2-b12c-d0956ed716c8)
Use positional arguments for the most part, but if you are dealing with numerical values use Keyword argument which are best used to improve the readability of your codes. Note always use keyword arguments after a positional arguments.

# Return statements: This involves a function that return values.

```
```
```
```
```
```
```
```
```
```
```
```
```
