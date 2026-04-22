# Password-Strength-Checker
simple Python program that checks the strength of a user’s password based on length, uppercase, lowercase, digit, and special characters.


import os
os.system("cls")
password=input("Enter Your Password :")
import time
time.sleep(1)
print("loading .",end="\r")
time.sleep(1)
print("loading ..",end="\r")
time.sleep(1)
print("loading ...",end="\r")
time.sleep(1)
for char in password:
    upper=False
    if char.isupper():
        upper=True
        break
for char in password:
    lower=False
    if char.islower():
        lower=True
        break
for char in password:
    digit=False
    if char.isdigit():
        digit=True
        break
for char in password:
    spl=False
    if char in '!@#$%^&*()_-=+':
        spl=True
        break
length=False
if len(password)>=8:
    length=True
if upper and lower and digit and spl and length:
    print("Your Password is Strong")
elif(upper+lower+digit+spl>=2):
    print("Password Is Decent")
else:
    print("Password Is Weak You Must Strengthen Your Password")
