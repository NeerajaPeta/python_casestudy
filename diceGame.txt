import random

def roll_dice():
    min_value = 1
    max_value = 6
    roll_again = True

    while roll_again:
        #Generate a random number from 1 to 6
        dice_roll = random.randint(min_value, max_value)
        print("You rolled:", dice_roll)

        # Ask the user if they want to roll again
        roll_again = input("Do you want to roll again? (yes/no): ").lower()
        
        if roll_again == "no" or roll_again == "n":
            roll_again = False
        elif roll_again == "yes" or roll_again == "y":
            roll_again = True
        else:
            print("Invalid input. Please enter 'yes' or 'no'.")
            roll_again = False

    print("Thank you for playing!")

# Call the roll_dice() function to start the game
roll_dice()
