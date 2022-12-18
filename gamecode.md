# IT111

#Rock Sessors Paper game


import random

input('Welcome to our game of Rock, Paper, Scissors!! Please Press Enter to start.')
print()
user_wins = 0
computer_wins = 0

choices = ["rock", "paper", "scissors"]

while True:
  random_index = random.randint(0,2)
  comp_choice = choices[random_index]

  user_choice = input("Choose your Warrior! Rock, Paper, or Scissors? ").lower()
  while user_choice not in choices:
    user_choice = input("That is not a valid choice. Please choose Rock, Paper or Scissors: ").lower()
  
  print()
  print("Your Warrior:", user_choice)
  print("Computer's Warrior:", comp_choice)
  print()

  if user_choice == 'rock':
    if comp_choice == 'rock':
      print("It's a tie!")
    elif comp_choice == 'scissors':
      print("Congrats! You win!")
      user_wins+=1
    elif comp_choice == 'paper':
      print("Oh no, You lost!")
      computer_wins+=1
  elif user_choice == 'paper':
    if comp_choice == 'paper':
      print("It's a tie!")
    elif comp_choice == 'rock':
      print("Congrats! You win!")
      user_wins+=1
    elif comp_choice == 'scissors':
      print("Oh no, You lose!")
      computer_wins+=1
  elif user_choice == 'scissors':
    if comp_choice == 'scissors':
      print("It's a tie!")
    elif comp_choice == 'paper':
      print("Congrats! You win!")
      user_wins+=1
    elif comp_choice == 'rock':
      print("Oh no, You lose!")
      computer_wins+=1

  print()
  print("Your Victories "+str(user_wins)+" !")
  print("The computer's Victories "+str(computer_wins)+" !")
  print()

  repeat = input("Would you like to play again? Yes or No? (Y/N) ").lower()
  while repeat not in ['y', 'n']:
    repeat = input("Please try again with Y or N: ").lower()
  
  if repeat == 'n':
     print('Thank you for playing!')
     break
  
