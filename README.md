# MANDADRI-ROHITH
# Python Math & Time Modules
import math
import time

# Intro
print("Welcome to the Temperature Conventer. Type C for Celsuis, F for Fahreinheit and K for Kelvin")

# Function
def again():
    try_again = print()
    # Letting the user choose the temperature and convert it to another temperature else
    User_Temperature = input("your temperature | C | F | K | ").upper()
    convert_Temperature = input("The temperature you want to convert to | C | F | K | ").upper()
  
    # If the user's intial temperature (C, F, or K) convert it to what the user wants to convert to (C, F, or K) and give him the equation
    if User_Temperature == "C":
        if convert_Temperature == "F":
            degree = float(input("enter the degree: "))
            result = (degree * 9/5) + 32
            print(f"{result}°F \nThe equation: ({degree} × 9/5) + 32 = {result}")
        elif convert_Temperature == "K":
            degree = float(input("enter the degree: "))
            result = degree + 273.15
            print(f"{result}°K \nThe equation: {degree} + 273.15 = {result}")
        elif convert_Temperature == "C":
            print("This is the same type of temperature")
            time.sleep(1)
            again()
        else:
            print("Type a temperature")
            time.sleep(1)
            again()

    elif User_Temperature == "F":
        if convert_Temperature == "C":
            degree = float(input("enter the degree: "))
            result = (degree - 32) * 5/9
            print(f"{result}°F \nThe equation: ({degree} - 32) × 5/9 = {result}")
        elif convert_Temperature == "K":
            degree = float(input("enter the degree: "))
            result = (degree - 32) * 5/9 + 273.15
            print(f"{result}°K \nThe equation: ({degree} - 32) × 5/9 + 273.15 = {result}")
        elif convert_Temperature == "F":
            print("This is the same type of temperature")
            time.sleep(1)
            again()
        else:
            print("Type a temperature")
            time.sleep(1)
            again()

    elif User_Temperature == "K":
        if convert_Temperature == "C":
            degree = float(input("enter the degree: "))
            result = degree - 273.15
            print(f"{result}°F \nThe equation: {degree} - 273.15 = {result}")
        elif convert_Temperature == "F":
            degree = float(input("enter the degree: "))
            result = (degree - 273.15) * 9/5 + 32
            print(f"{result}°K \nThe equation: ({degree} - 273.15) × 9/5 + 32 = {result}")
        elif convert_Temperature == "K":
            print("This is the same type of temperature")
            time.sleep(1)
            again()
        else:
            print("Type a temperature")
            time.sleep(1)
            again()

    else:
        print("Type a temperature")
        time.sleep(1)
        again()

  # Aking if the user wants to convert again
    while try_again != "Yes" and try_again != "No":
        print("\nDo you want to try again?")
        try_again = input("Yes | No | ").lower().capitalize()
        if try_again == "Yes":
            again()
            break
        elif try_again == "No":
            print("Goodbye")
            break

again()
