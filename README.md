# number-guesssing

import random

print(
  "Welcome to the Number Guessing Game!"   
  "   I'm thinking of a number bw 1 and 100")
EASY_LIFE=10
HARD_LIFE=5
def check_answer(user_guess,choice_random,turns):
  if user_guess==choice_random:
    print(f"your answer is crct: {choice_random}")
    return turns-1
  elif user_guess>choice_random:
    print("Too high")
    return turns-1
   
    
  elif user_guess<choice_random:
      print("too low")
  
      
def level():
  level=input("Choose difficulty level.Type 'easy' or 'hard'").lower()
  
  if level=="easy":
     turns=(EASY_LIFE)
     return turns
  elif  level =="hard":
     turns=int(HARD_LIFE)
     return turns


def game():
 print("WELcome")
 turns=level()

 
 choice_random=random.randint(1,100)

 
 user_guess=0
 while user_guess!=choice_random:
        print(f"You have  {turns}attempts remaining")
        user_guess=int(input("Make a guess: "))
        turn=check_answer(user_guess,choice_random,turns)
        if turns==0:
            print("you lose,max attempts exceed")
            return
        
game()   

