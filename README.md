# Rock_Paper_Scissors
Python script to run rock, paper, scissors against the computer while tracking total score with quitting function.
# Import tools
import random
# Insert win counter
user_wins = 0
computer_wins = 0
# Create List with text strings as the elements (Mutable)
options = ["rock", "paper", "scissors"]
# Input game start Print function
while True:
    user_input = input("Type rock/paper/scissors or Q to quit: ").lower()
    if user_input == "q":
        break

    if user_input not in options:
        continue
# Create random number generator for computer
    random_number = random.randint(0, 2)
    # Rock: 0, paper: 1, scissors: 2
    computer_pick = options[random_number]
    print("Computer picked", computer_pick + ".")
#  If statements and adding values to user/computer
    if user_input == "rock" and computer_pick == "scissors":
        print("You Won!")
        user_wins += 1

    elif user_input == "paper" and computer_pick == "rock":
        print("You Won!")
        user_wins += 1

    elif user_input == "scissors" and computer_pick == "paper":
        print("You Won!")
        user_wins += 1
# Input draw/lose conditions
    else:
        print("That's Crazy")
        computer_wins += 1
# Print string when user or computer won
    print("You Won!", user_wins, "times.")
    print("The Computer Won!", computer_wins, "times.")
    print("Goodbye!")