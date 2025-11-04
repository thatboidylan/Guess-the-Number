# Guess-the-Number
import random as rd

magic_number = rd.randint(1, 100)
print(magic_number)
 
guess = int(input("Enter a number between 1 and 100: "))
counter = 5

while guess != magic_number and counter > 0:
  counter -=1
  print("You lose!")
  print("%s guesses remain." % (counter))
  print("")
  if counter == 0:
    break

  guess = int(input("Guess a number between 1 and 100"))

else:
  print("You win!")
