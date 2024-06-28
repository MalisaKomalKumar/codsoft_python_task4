# codsoft_python_task4
#This is my Task 4 as an intern at codsoft ,  This is a program written in the Python language. 
import random

def play_rock_paper_scissors():
  """Plays a round of Rock-Paper-Scissors with the user."""

  # User input
  while True:
    user_choice = input("Enter 'rock', 'paper', or 'scissors': ").lower()
    if user_choice in ['rock', 'paper', 'scissors']:
      break
    else:
      print("Invalid choice. Please try again.")

  # Computer selection (random)
  computer_choice = random.choice(['rock', 'paper', 'scissors'])

  # Determine winner
  win_message = "You Win!"
  lose_message = "You Lose!"
  tie_message = "It's a tie!"

  if user_choice == computer_choice:
    print(tie_message)
  elif user_choice == 'rock':
    if computer_choice == 'scissors':
      print(win_message)
    else:
      print(lose_message)
  elif user_choice == 'paper':
    if computer_choice == 'rock':
      print(win_message)
    else:
      print(lose_message)
  elif user_choice == 'scissors':
    if computer_choice == 'paper':
      print(win_message)
    else:
      print(lose_message)

  # Display choices
  print(f"You chose: {user_choice}")
  print(f"Computer chose: {computer_choice}")

# Play again prompt
play_again = input("Do you want to play again? (y/n): ").lower()

while play_again == 'y':
  play_rock_paper_scissors()
  play_again = input("Do you want to play again? (y/n): ").lower()

print("Thanks for playing!")
