# Logical Operations
#  AND CONDITION
# this is use when we have multiple conditions for instance if an applicant has high income AND good credit . The person is Eligible for loan
has_high_income = True
has_good_credit = True

if has_high_income and has_good_credit:
    print("Eligible for loan")

![Screenshot from 2024-09-22 21-42-28](https://github.com/user-attachments/assets/981b184b-5a49-46d9-88f0-b60b87a37435)

# if you set one of the statement to false nothing will display
has_high_income = False
has_good_credit = True

if has_high_income and has_good_credit:
    print("Eligible for loan")
![Screenshot from 2024-09-22 21-43-21](https://github.com/user-attachments/assets/858a38fe-beaa-4ba3-ad98-2fee1a483896)

# OR CONDITIONS
# if an applicant has high income OR good credit . The person is Eligible for . 
#here since of the condition is available the answer will be eligible for loan
has_high_income = False
has_good_credit = True

if has_high_income or has_good_credit:
    print("Eligible for loan")
![Screenshot from 2024-09-22 21-45-33](https://github.com/user-attachments/assets/a6c7c53e-0010-46bc-8c94-ee77025bbe1a)


# NOT CONDITIONS
# if an applicant has good credit and doesn't have a criminal record, then the person is Eligible for loan

has_good_credit = True
has_criminal_record = False

if has_good_credit and not has_criminal_record:
    print("Eligible for loan")
![Screenshot from 2024-09-22 21-58-53](https://github.com/user-attachments/assets/432fbbef-6321-469f-a0f0-d89f211c5cdc)

# if change oth to TRUE no message will be printed

# Comparison operators
# this is used when we want to compare a variable with value.
#for instance : if temperature is greater than 30
                     #it's a hot day
                #otherwise if it's less than 10
                    #it's a cold day
                #otherwise 
                    #it's neither hot or cold
temperature = 30

if temperature > 30:
    print("it's a hot day")
else:
    print("it's not a hot day")
![Screenshot from 2024-09-22 22-07-31](https://github.com/user-attachments/assets/464aeefa-789b-4db4-8829-7158a06f28cd)
## it is showing its not a hot day becuase we set it higher than the value of the variable

# changed value to 35
temperature = 35

if temperature > 30:
    print("it's a hot day")
else:
    print("it's not a hot day")

![Screenshot from 2024-09-22 22-09-44](https://github.com/user-attachments/assets/64a8ebf8-cc10-4706-9124-d865f55bfec9)

# self practice my attempt
# this is used when we want to compare a variable with value.
#for instance : if name is less than 3 characters long
                     #name must be at least 3 characters
                #otherise if more than 50 characters long
                    #name can be a maximum of 50 characters
                #otherwise 
                    #name looks good
name = 3

if name < 3:
    print("name must be at least 3 characters")
else:
    print("name can be a maximum of 50 characters")

![Screenshot from 2024-09-22 22-16-52](https://github.com/user-attachments/assets/7c6626c9-aa7d-447b-8545-4baa006107c8)

#Solution
name = "J"


if len(name) < 3:
    print("name must be at least 3 characters")
elif len(name) > 50:
    print("name can be a maximum of 50 characters")
else:
    print("name looks good")
![Screenshot from 2024-09-22 22-20-38](https://github.com/user-attachments/assets/1908ccee-a4bf-4289-b439-f79cde67529a)
## i added more than 50 to the name 
name = "Jcdgfhgbvhtjkmhbjhxvdfgxdfgvxxfsdgfghfhesxdfdfttgfjhbnjgvgdxfazdsfdfcvbfvnecdyhngkjnmlnhn"


if len(name) < 3:
    print("name must be at least 3 characters")
elif len(name) > 50:
    print("name can be a maximum of 50 characters")
else:
    print("name looks good")

![Screenshot from 2024-09-22 22-23-46](https://github.com/user-attachments/assets/542a47c9-a881-4ae6-a6f2-8bccdfce156a)

### now did a proper name between 3 to 50
name = "John Smith"
if len(name) < 3:
    print("name must be at least 3 characters")
elif len(name) > 50:
    print("name can be a maximum of 50 characters")
else:
    print("name looks good")

![Screenshot from 2024-09-22 22-24-20](https://github.com/user-attachments/assets/d567b828-3213-4669-a25d-a1ce2b669f6a)



    



