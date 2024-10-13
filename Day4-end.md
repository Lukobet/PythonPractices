
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

## NESTED LOOPS
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
```
