from __future__ import print_function
import random

playerItems = []
enteredRooms = []
openedDoors = []

def startGame():
    print('Welcome to the Port-a-potty')
    raw_input('Press enter to start the game. ')
    lobby()

def lobby():
    global playerItems
    global enteredRooms
    global openedDoors
    exitRoom = False
    Bank_Items_Manager = ['$2000 in money']
    print('You have entered the lobby.')
    print('There are two doors in this lobby.  One to the north(vault) and one to the right(offices).')
    print('There is also a bank teller with one drawer that has money in the room.')
    userAction = raw_input('What would you like to do? ')
    while exitRoom == False:
        if userAction == 'open office doors' and 'vault code' in playerItems:
            print('You have entered the offices')
            openedDoors += ['offices']
            exitRoom = True
        elif userAction == 'open vault' and 'vault code' in playerItems:
            print('You have now entered the vault, what would you like to do?')
            openedDoors += ['door2']
            exitRoom = True
        elif userAction == 'open dresser':
            print('You picked up', dresserItems)
            money =  money + 2000
            playerItems += dresserItems
            dresserItems = []
            userAction = raw_input('What would you like to do now? ')
        elif userAction == 'open vault' and 'vault code' not in playerItems:
            print('The vault will not open')
            userAction = raw_input('What would you like to do now? ')
       
    
        
def room2():
    global enteredRooms
    print('You entered Room 2')
    if 'room2' in enteredRooms:
        print('This room looks vaguely familiar')
    if 'room2' not in enteredRooms:
        enteredRooms += ['room2']
        
def room3():
    global enteredRooms
    print('You entered Room 3')
    if 'room3' in enteredRooms:
        print('This room looks vaguely familiar')
    if 'room3' not in enteredRooms:
            enteredRooms += ['room3']
