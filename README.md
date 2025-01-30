


import random
guess= int

def guess_the_number():
    while True:
        secret_number = random.randint(1, 10)
        attempts = 0
        print("I'm thinking of a number between 1 and 10. Can you guess what it is?")
        
        while True:
            guess = input("Enter your guess: ")
            
            if not guess.isdigit():
                print("Invalid input. Please enter a number between 1 and 10.")
                continue
            
            guess = int(guess)
            attempts += 1
            
            if guess < secret_number:
                print("Too low! Try again.")
            elif guess > secret_number:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed the number in {attempts} attempts.")
                break
        
        play_again = input("Do you want to play again? (yes/no): ").strip().lower()
        if play_again != "yes":
            print("Thanks for playing! Goodbye.")
            break

if __name__ == "__main__":
    guess_the_number()
    
PS C:\Users\user> & C:/Users/user/AppData/Local/Programs/Python/Python313/python.exe "c:/Users/user/Downloads/import random.py"
I'm thinking of a number between 1 and 10. Can you guess what it is?
Enter your guess: age
PS C:\Users\user> & C:/Users/user/AppData/Local/Programs/Python/Python313/python.exe "c:/Users/user/game num.py"
I'm thinking of a number between 1 and 10. Can you guess what it is?
Enter your guess: age
Invalid input. Please enter a number between 1 and 10.
Enter your guess: 2
Too low! Try again.
Enter your guess: 8
Too high! Try again.
Enter your guess: 4 
Congratulations! You guessed the number in 3 attempts.
Do you want to play again? (yes/no): yes
I'm thinking of a number between 1 and 10. Can you guess what it is?
Enter your guess: 10
Too high! Try again.
Enter your guess: 7
Too low! Try again.
Enter your guess: 8
Too low! Try again.
Enter your guess: 9
Congratulations! You guessed the number in 4 attempts.
Do you want to play again? (yes/no): no
Thanks for playing! Goodbye.
