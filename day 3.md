# Logical Operations
#  this is use when we have multiple conditions for instance if an applicant has high income AND good credit . The person is Eligible for loan
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

# if an applicant has high income OR good credit . The person is Eligible for . 
#here since of the condition is available the answer will be eligible for loan
has_high_income = False
has_good_credit = True

if has_high_income or has_good_credit:
    print("Eligible for loan")
![Screenshot from 2024-09-22 21-45-33](https://github.com/user-attachments/assets/a6c7c53e-0010-46bc-8c94-ee77025bbe1a)


