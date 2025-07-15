# number-guessing-game
A mini Python project where the user guesses a randomly generated number. It includes attempt counter, scoring logic, and quit option.



import random
print("Welcome to the Number Guessing Game!")

target = random.randint(1, 100)
attempts = 0
score = 100
while True:
    userChoice = input("Guess the number between 1 to 100 or Quit(Q): ")

    if userChoice == "Q":
        break 

    attempts += 1
    score = max(100 - (attempts - 1) * 10, 0)
    userChoice = int(userChoice)

    if userChoice == target:
        print(f" Congratulations! Correct Guess... in {attempts} attempts.")
        print(f"Your Score : {score}")
        break  
    elif userChoice < target:
        print("Your number is too small. Take a bigger choice...")
    else:
        print("Your number is too big. Take a smaller choice...")

print("____Game Over____")
