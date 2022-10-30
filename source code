#This Program can count you GPA

#This line of code is defition of grade value :
def grade(user_grade):
    result = 0
    if user_grade in "Aa":
        result = 4
    elif user_grade in "Bb":
        result = 3
    elif user_grade in "Cc":
        result = 2
    elif user_grade in "Dd":
        result = 1
    elif user_grade in "Ee":
        result = 0

    return result

#this line of code of promt :

print("Welcome to GPA counter")

try:
    total_credits = int(input("Enter your total credit: ")) #user will input total credit
    total_courses = int(input("Enter your total courses : ")) #user will input total courses
except ValueError as err:
    print(err)

#this line for declare variabel

value_grade = 0
total_grade = 0
total_crs = 0
credit_remain = 0

#create for loops to loops total courses and grade

for course in range(total_courses):
    #user will in put the credit each subject :
    try:
        in_credit = int(input("Enter the CREDIT for subject " + str(course+1) + ": "))
    except ValueError as err:
        print(err)
    #user will input grade for each subject :
    in_grade = input("Enter your GRADE for subject " + str(course+1) + ": ")
    #this line to check if user input wrong grade for each subject:
    while in_grade.lower() not in "abcde":
        print("Invalid input, make sure you enter ABCDE : ")
        in_grade = input("Enter your GRADE for subject " + str(course + 1) + ": ")
    #course will increment by 1 to rename subject x to be subject 1 and so on:
    course += 1

    #credit remain will increment by input credit total
    credit_remain += in_credit
    #credit remain will inform user how many credit left from total credit:
    print("credit remain: " + str(total_credits-credit_remain))

    #value grade is credit * grade each subject :
    value_grade = in_credit * grade(in_grade)
    #total value credit by all subject:
    total_grade += value_grade
    #total credit course by all subject:
    total_crs += in_credit

#to check if total credit is not same with total credit user input :
if total_crs != total_credits:
    print("The Total Credit is not match with total credit subject, Please Check again")

#if total credit is match with total credit user input, program with count your GPA
else:
    #formula to count GPA
    GPA = float(total_grade/total_credits)
    print("You're GPA is : ")
    #GPA will use 2 decimal from float
    print("%.2f" %(GPA))
    #just commenting base from GPA result
    if GPA == 4:
        print("Congratulation, You are PERFECT")
    elif GPA < 4 and GPA >= 3 :
        print("Exelent, Keep your Hardwork")
    elif GPA < 3 and GPA >= 2.5 :
        print("Good, little more to be exelent")
    elif GPA < 2.5:
        print("Keep spirit, more hard to work")
