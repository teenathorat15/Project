# Rock Paper Scissors using python 
This is my First Github Project.
I developed this portfolio using Python IDLE framework. 
In this game, the user gets the first chance to pick the option between Rock, paper, and scissors. After the computer select from the remaining two choices(randomly), the winner is decided as per the rules.
so this is the main code:

import random
print('Winning rules of the game ROCK PAPER SCISSORS are :\n'
      + "Rock vs paper -> Paper wins \n"
      + "Rock vs Scissors -> Rock wins \n"
      + "Paper vs Scissors -> Scissor wins \n")

while True:
    
    print("Enter your choice \n 1 - Rock \n 2 - paper \n 3 - Scissors \n")
    
    choice=int(input ("Enter your choice :"))
    
    while choice > 3 or choice < 1:
        choice = int(input('Enter a valid choice please'))
    if choice == 1:
        choice_name= 'Rock'
    elif choice == 2:
        choice_name= 'Paper'
    else:
         choice_name= 'Scissors'
            
    print('User choice is \n ', choice_name)
    print('Now its computers turn....')
        
    comp_choice = random.randint(1,3)
        
    while comp_choice == choice:
      comp_choice = random.randint(1,3)

    if comp_choice == 1:
      comp_choice_name = 'Rock'
    elif comp_choice == 2:
      comp_choice_name = 'paper'
    else:
      comp_choice_name= 'Scissor'
    print('Computer choice is \n ', comp_choice_name)
    print(choice_name,'vs',comp_choice_name)
        
    if choice == comp_choice:
         print('Its a draw', end="")
         result= 'Draw'
            
    if(choice==1 and comp_choice==2):
         print('Paper wins =>',end="")
         result='Paper'
    elif (choice==2 and comp_choice==1):
         print('Paper wins =>',end="")
         result='Paper'

    if(choice==1 and comp_choice==3):
         print('Rock wins =>\n',end="")
         result='Rock'
    elif (choice==3 and comp_choice==1):
         print('Rock wins =>\n',end="")
         result='Rock'

    if(choice==2 and comp_choice==3):
         print('Scissors wins =>',end="")
         result='Scissor'
    elif (choice==3 and comp_choice==2):
         print('Scissor wins =>\n',end="")
         result='Rock'

    if result == 'Draw' :
         print("<== its a tie ==>")
    if result == choice_name:
         print("<== User wins ==>")
    else:
         print("<== Computer wins ==>")
    print("Do you want to play again? (Y/N)")
    ans = input().lower()
    if ans =='n':
         break
 print("Thanks for playing")
