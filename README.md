# Rock-Papers-Scissors
Rosey Li's Girls Who Code Project

import random
#random.randint(a,b) returns a random integer 

#Returns True if gesture is one of the strings 'rock', 'paper', or 'scissors', and False otherwise.
def isValidGesture(gesture):
    return gesture== 'rock' or gesture== 'paper' or gesture== 'scissors' 
       
#Randomly returns one of 'rock', 'paper', or 'scissors', with equal probability.
def randomGesture():
    """Randomly returns one of 'rock', 'paper', or 'scissors',
       with equal probability."""
    gesture= ['rock', 'paper', 'scissors']
    return gesture[rand.randint(1,3)]
        
#Returns True if the first gesture beats the second gesture. Returns False otherwise.
def beats(gesture1, gesture2):
    if gesture1== 'rock':
        if gesture2== 'scissors':
            return True 
        else:
            return False     
    elif gesture1== 'scissors': 
        if gesture2== 'paper':
            return True
        else:
             return False           
    elif gesture1== 'paper':
        if gesture2== 'rock':
            return True
        else:
            return False
            
#Plays rock/paper/scissors game with your gesture vs. opponent's gesture. 
def play(you, opponent):
    if isValidGesture(you) == False:
        print 'Your gesture ' + '(' + you + ') ' + 'is invalid'
    elif isValidGesture(opponent)== False:
        print 'Opponent\'s gesture ' + '(' + opponent + ') ' + 'is invalid'
    else: 
        if beats(you, opponent):
            print 'You win!'     
        elif you == opponent:
            print 'Game is a tie!'
        else:
            print 'Opponent wins!'
            
#Plays rock/paper/scissors with your gesture against a computer opponent that randomly chooses a gesture. First displays the #choice of the computer, and then displays the result of the game.          
def playComputer(you):
    compresult= randomGesture()
    print 'Computer chooses ' + compresult
    return play(you, compresult)
    
