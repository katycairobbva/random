# random
# random work
import random

def secret_number_game(low, high, rounds):
  print('Can you guess my secret number between {low} and {high}. You have {rounds} rounds to try')
  secret_number = random.randint(low, high)

  for _ in range(rounds):
    guess = input('Enter a number: ')

    try:
        integer = int(guess)
        if integer == secret_number:
            print ('Great guessing! You won!')
            return
        elif integer < secret_number: 
            print('Your guess is too low.')
            continue
        elif integer > secret_number: 
            print('Your guess is too high.')
            continue
    except ValueError:
      print('You must enter a valid number')
 
  print('You were unable to guess my secret number in {rounds} rounds. Better luck next time'.format(rounds=rounds))

secret_number_game(1,100,10)
