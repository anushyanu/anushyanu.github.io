#  TIC-TAC-TOE game development in Python

Developed a simple Tic-tac-toe game in python

## Brief description of the module
  tbd 

## Pseudocode
tbd

## Code 

```
import random

def init_tic_tac_toe():
    myl0=[0,0,0]
    myl1=[0,0,0]
    myl2=[0,0,0]
    #mylol=[myl,myl,myl]
    mylol=[myl0,myl1,myl2]
    print_tic_tac_toe(mylol)
    return mylol

def print_tic_tac_toe(mylol):
    #print(mylol)
    for i in range(len(mylol)):
        print (mylol[i])

def get_user_input(who):
    user_input=input(who+" Enter the location to block ")
    return user_input

def manipulate_tic_tac_toe(user_input, mylol):
    if(user_input == "00"):
        mylol[0][0] = "U"
    elif(user_input == "01"):
        mylol[0][1] = "U"
    elif(user_input == "02"):
        mylol[0][2] = "U"
    elif(user_input == "10"):
        mylol[1][0] = "U"
    elif(user_input == "11"):
        mylol[1][1] = "U"
    elif(user_input == "12"):
        mylol[1][2] = "U"
    elif(user_input == "20"):
        mylol[2][0] = "U"
    elif(user_input == "21"):
        mylol[2][1] = "U"
    elif(user_input == "22"):
        mylol[2][2] = "U"
    else:
        print("Input not acceptable. Try again !!")
    print_tic_tac_toe(mylol)    

def computer_manipulate_tic_tac_toe(user_input, mylol):
    if(user_input == 0):
        mylol[0][0] = "C"
    elif(user_input == 1):
        mylol[0][1] = "C"
    elif(user_input == 2):
        mylol[0][2] = "C"
    elif(user_input == 3):
        mylol[1][0] = "C"
    elif(user_input == 4):
        mylol[1][1] = "C"
    elif(user_input == 5):
        mylol[1][2] = "C"
    elif(user_input == 6):
        mylol[2][0] = "C"
    elif(user_input == 7):
        mylol[2][1] = "C"
    elif(user_input == 8):
        mylol[2][2] = "C"
    else:
        print("Input not acceptable. Try again !!")
    print_tic_tac_toe(mylol)    

def check_game_status(mylol):
    zero_blocks = 0
    for i in range(len(mylol)):
        for j in range(len(mylol[i])):
            if (mylol[i][j] == 0):
                zero_blocks = zero_blocks + 1
    if (zero_blocks > 0):
        print ("Game not finished, please continue .. ")
        game_finished = 0
    else:
        print ("Game finished, Need to check the winner or is it tie !!!")
        find_winner(mylol)
        game_finished = 1
    return game_finished

#def find_winner(mylol):
     #for i in range(len(mylol)):
     #   if 
    
anuttt=init_tic_tac_toe()
while(True):
    game_status = check_game_status(anuttt)
    if (game_status==0):
        user_input=get_user_input("user")
        manipulate_tic_tac_toe(user_input,anuttt)
        computer_input=random.randint(0,8)
        print("computer pressed", computer_input)
        computer_manipulate_tic_tac_toe(computer_input,anuttt)
    else:
        print("game_finished")
```
## What I Learned

While doing the problem I understood the concepts relating immutable and mutable objects. 
Improved my understanding on lists and breaking a problem using divide and conquer approach. 
