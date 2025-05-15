# guess-number-game
This Python game lets you guess a number chosen by the computer within a user-defined range. After entering the range, the computer picks a random number. You get 7 chances to guess it, with hints if your guess is too high or low. If you guess it right, you win; otherwise, the correct number is revealed after 7 tries.


import random

print("Hi! Welcome to the Number Guessing Game.\nYou have 7 chances to guess the number. Let's start!")

low = int(input("Enter the Lower Bound: "))
high = int(input("Enter the Upper Bound: "))

print(f"\nYou have 7 chances to guess the number between {low} and {high}. Let's start!")

num = random.randint(low, high) 
ch = 7                        # Total allowed chances
gc = 0                        # Guess counter

  while gc < ch:
    gc += 1
    guess = int(input('Enter your guess: '))

    if guess == num:
        print(f'Correct! The number is {num}. You guessed it in {gc} attempts.')
        break

    elif gc >= ch and guess != num:
        print(f'orry! The number was {num}. Better luck next time.')

    elif guess > num:
        print('Too high! Try a lower number.')

    elif guess < num:
        print('Too low! Try a higher number.')
