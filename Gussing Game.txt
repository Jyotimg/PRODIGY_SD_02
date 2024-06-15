import random

def guessing_game():
    # Generate a random number between 1 and 100
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guess = None

    print("Welcome to the Guessing Game!")
    print("I have generated a random number between 1 and 100.")
    print("Try to guess the number!")

    # Loop until the user guesses the correct number
    while guess != number_to_guess:
        try:
            # Prompt the user for their guess
            guess = int(input("Enter your guess: "))
            attempts += 1

            # Provide feedback on the guess
            if guess < number_to_guess:
                print("Too low! Try again.")
            elif guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed the correct number {number_to_guess} in {attempts} attempts.")
        except ValueError:
            # Handle the case where the input is not a valid integer
            print("Invalid input! Please enter a valid number.")

# Run the guessing game
if __name__ == "__main__":
    guessing_game()
