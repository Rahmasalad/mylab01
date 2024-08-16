import random

def main():
    print("Welcome to the Guessing Game!")
    
    # Generate a random number between 1 and 25
    number_to_guess = random.randint(1, 25)
    guessed_correctly = False
    
    while not guessed_correctly:
        try:
            # Prompt the user to guess the number
            user_guess = int(input("Guess a number between 1 and 25: "))
            
            if user_guess < number_to_guess:
                print("Higher!")
            elif user_guess > number_to_guess:
                print("Lower!")
            else:
                print("Congratulations! You've guessed the number!")
                guessed_correctly = True
        
        except ValueError:
            print("Please enter a valid integer.")
    
if __name__ == '__main__':
    main()
