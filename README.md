# Guess-the-Number
import random as rd
import os
wins = 0
attempt = 0
play = True
round1 = 1

while play:
  numbers = []
  magic_number = rd.randint(1, 100)
  # print(magic_number)

  guess = int(input("Enter a number between 1 and 100: "))
  counter = 6
 
  while guess != magic_number and counter > 0:
    counter -=1
    numbers.append(guess)
    if magic_number < guess:
      print("Try lower")
    if magic_number > guess:
      print("Try higher")
    print("%s guesses remain." % (counter))
    print("")
    if counter == 0:
      print("Game Over")
    elif guess != magic_number:
      guess = int(input("Try again"))
  if guess == magic_number: 
     print("You win!")
     wins += 1
  if guess == magic_number or counter == 0:
    attempt += 1
    print("SCOREBOARD")
    print("----------")
    print("You've won %d out of %d rounds" % (wins,attempt))
    
    print("Would you like to play again")
    response=input("y/n")
    
    if response == "y":
      os.system("cls")
      round+=1
      
      print("Okay round" +str(round))
    else:
      play=False
      print("Thanks for playing type shiiiii")
