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
        if userAction == 'open office doors' and 'Vault code' in playerItems:
            print('You have entered the offices')
            openedDoors += ['offices']
            exitRoom = True
        elif userAction == 'open vault'
            print('You cannot open the vault door without the vault code. Go to the offices to retrieve the code.')
            openedDoors += ['door2']
            exitRoom = True
        elif userAction == 'open dresser':
            print('You picked up', dresserItems)
            playerItems += dresserItems
            dresserItems = []
            userAction = raw_input('What would you like to do now? ')
        elif userAction == 'open door 2' and 'key1' not in playerItems:
            print('The door will not open')
            userAction = raw_input('What would you like to do now? ')
        elif userAction == 'open door 2' and 'flashlight' not in playerItems:
            print('You open the door, but it is so dark inside that you cannot see.  You do not enter and you close the door.')
            userAction = raw_input('What would you like to do now? ')
        else:
            userAction = raw_input('Not a valid action.  Try Again! ')
    if 'door1' in openedDoors:
        room2()
    else:
        room3()
        
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
