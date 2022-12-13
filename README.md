# Password
Create a program that takes the length of the password as input and generates a random password of the same length. The strength of the password depends equally on the 4 properties mentioned below
def password(number):
    lower=""
    num=""
    sym=""
    for numbers in number:
        if numbers>="a" and numbers<="z":
            lower+=numbers
        elif numbers>="A" and numbers<="Z":
            upper+=numbers 
        elif numbers>="0" and numbers<="9":
            num+=numbers
        elif numbers in symbol:
            sym+=numbers
    return lower,upper,num,sym
symbol=['@','$','&','#','?']

active = True
while active:
    number = input("Enter a Strong Password :")
    lower, upper, num, sym = password(number)
    if len(number) >= 12:
        if len(number) == (len(lower)  + len(upper) + len(num) + len(sym)):
            print("It's a Strong Password")
            active = False
        else:
            print("Password should consists of uppercase letter,number,and symbols[@ ,$, &, #, ?]")
        else:
            print("Password should consists of uppercase letter, lowercase letter, number, and symbols [@, $, &, #, ?]")
        else:
            print("Password should consists of atleast 12 characters")
