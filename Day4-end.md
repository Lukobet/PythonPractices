
# While loops
## This is used to execute a block of code multiple times and they are often used in building interactive programs and games.


i = 1 #i.e index = 1
## we write it like this (while condition:)

while i <= 5:
    print(i)
    i = i + 1 ## we increment i by 1 so tha i wont be 1 forever and end up wih infinte loop
    print("Done")

![Screenshot from 2024-09-27 04-47-43](https://github.com/user-attachments/assets/ff8644a4-0b07-41f5-97c3-9adbf099b8bc)



i = 1 

while i <= 5:
    print('*' * i) ## to make it more interesting
    i = i + 1 
    print("Done")
![Screenshot from 2024-09-27 04-52-46](https://github.com/user-attachments/assets/4c1b9d7f-cc2f-4169-a039-1a43792017ba)

# How to use a while loop to build a Guessing Game
## first thing is to define a variable to define a secret number

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
secret_number = 9
guess_count = 0
guess_limit = 3
while guess_count < guess_limit:
    guess = int(input('Guess: '))
    guess_count += 1
    if guess == secret_number:
        print('You won!')
        
![Screenshot from 2024-09-27 05-15-30](https://github.com/user-attachments/assets/f80f2191-43b5-4e22-b668-feebf6f451f0)

## this implementation those not have a message that i failed. 
## i tried using the correct guess first ad wrong answers after 

![Screenshot from 2024-09-27 05-18-24](https://github.com/user-attachments/assets/be589399-507d-42d2-8e47-56967b8af418)

## here it kept running even after the right answer because our while loop needs to be executed 3 times. we need to change the while loop in such a way that when the user gets the right answer it stops. to do this we use the break statement
              ##### break
#### its becomes this
secret_number = 9
guess_count = 0
guess_limit = 3
while guess_count < guess_limit:
    guess = int(input('Guess: '))
    guess_count += 1
    if guess == secret_number:
        print('You won!')
        break
    ![Screenshot from 2024-09-27 05-23-17](https://github.com/user-attachments/assets/871ce854-1fc7-4c9d-ad9a-d4cd769837e9)


### i need to input a failure message in my setup and also change and to do this i need to add an else in the while level
                #### else:
                #### print('Sorry you failed')
## it will now look like this
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
 ![Screenshot from 2024-09-27 05-30-43](https://github.com/user-attachments/assets/ccf0f05c-7932-43f3-8abe-52e05c56180a)
 

