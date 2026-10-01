# Python Assignment 3: While Loop, For loop and Function

## While loop & Control Statements :
### (else, break, continue, pass)

## Number Guessing Game

### Problem Statement:
Create a Python program that implements a simple number
guessing game using a while loop. The program should make use of control
statements such as else, break, and continue.

### Instructions:

**1. Set Up the Game:**

Generate a random number between 1 and 10 that the user has to guess.
Import random and use randint function.

**Answer:**

    import random

    # Generate random number between 1 and 10
    secret_number = random.randint(1, 10)

**2. Prompt the User:**

Ask the user to guess the number.
Set a variable attempts to 3, which represents the maximum number of guesses allowed.

**Answer:**

    attempts = 3

**3. Implement the Guessing Logic:**

Use a while loop to allow the user to keep guessing until they get the correct number or run out of attempts.

Provide feedback to the user for each guess:
- If the guess is out of the valid range (1 to 10), inform the user.
- If the guess is greater than the secret number.
- If the guess is lower than the secret number.
- If the guess is correct, congratulate the user and end the game.

**4. Control Statements:**

Use continue to skip the rest of the loop after informing the user if the guess is out of range.

Use break to exit the loop when the guess is correct.

Use else with the while loop to provide a message like "Better luck next time!" if the user runs out of attempts without guessing the correct number.

### Complete Python Code:

    import random

    # Generate random number between 1 and 10
    secret_number = random.randint(1, 10)

    attempts = 3

    while attempts > 0:
        guess = int(input("Guess the number (between 1 and 10): "))

        if guess < 1 or guess > 10:
            print("Your guess is out of range. Please guess a number between 1 and 10.")
            continue

        if guess > secret_number:
            print("Too high. Try again.")
        elif guess < secret_number:
            print("Too low. Try again.")
        else:
            print("Congratulations! You guessed the correct number.")
            break

        attempts -= 1
    else:
        print("Better luck next time!")

### Output:

    Guess the number (between 1 and 10): 15
    Your guess is out of range. Please guess a number between 1 and 10.
    Guess the number (between 1 and 10): 10
    Too high. Try again.
    Guess the number (between 1 and 10): 20
    Your guess is out of range. Please guess a number between 1 and 10.
    Guess the number (between 1 and 10): 8
    Too high. Try again.
    Guess the number (between 1 and 10): 2
    Too low. Try again.
    Better luck next time!

---

## For Loop:

## Multiplication Table Generator

### Problem Statement:
Create a Python program that generates and prints a multiplication table (from 1 to 10) for a given number using a for loop and the range function.

### Step wise Instructions:

**1. Prompt user for Input.**

Ask the user to enter a number for which they want to generate a multiplication table.

**2. Generate the Multiplication Table:**

Use a for loop to iterate through the numbers 1 to 10. In each iteration, calculate the product of the user's number and the current number from the loop.

**3. Display the Multiplication Table:**

Print each line of the multiplication table in the format: "number x i = result".

### Python Code:

    number = int(input("Enter the number for which you want the multiplication table: "))

    for i in range(1, 11):
        result = number * i
        print(number, "x", i, "=", result)

### Output:

    Enter the number for which you want the multiplication table: 10
    10 x 1 = 10
    10 x 2 = 20
    10 x 3 = 30
    10 x 4 = 40
    10 x 5 = 50
    10 x 6 = 60
    10 x 7 = 70
    10 x 8 = 80
    10 x 9 = 90
    10 x 10 = 100

---

## Function:

## BMI Calculator

### Problem Statement:
Create a Python program that calculates the Body Mass Index (BMI).

### Hint:
BMI = weight (kg) / [height (m)]²

### Instructions:

**1. Define a function calculate_bmi(weight, height) that returns the BMI.**

**2. Prompt the user for their weight (in kg) and height (in meters).**

**3. Use the function to calculate and display the BMI.**

### Python Code:

    def calculate_bmi(weight, height):
        return weight / (height ** 2)

    weight = float(input("Enter your weight in kg: "))
    height = float(input("Enter your height in meters: "))

    bmi = calculate_bmi(weight, height)

    print("Your BMI is:", format(bmi, ".2f"))

### Output:

    Enter your weight in kg: 58
    Enter your height in meters: 1.62
    Your BMI is: 22.10

---

# Conclusion

This assignment demonstrates the use of While Loop, For Loop, Control Statements, and Functions in Python.

The Number Guessing Game uses a while loop with else, break, and continue. The Multiplication Table Generator uses a for loop and range function. The BMI Calculator uses a function to calculate and display the Body Mass Index.
