# text-based RPG game

Group no.: 148

#### Team members:
- Liu Lihua
- Jiang Xingjian

#### A game description with game rules:
This is an RPG game in which the player acts as an adventurer and tries to defeat monsters throughout the adventure. 
The player will have Hit Points (HP), Mana Points (MP), and Experience (EXP). Before the adventure, the player can choose their skill from a given skill list. During the battle, the player and monster will take turns taking action. In the player’s turn, the player has 3 choices: normal attack (causes a small amount of damage and does not consume MP), rest (recovers some MP), and using skill (consumes MP, will cause lots of damage or recovers some HP). After the battle, the  player will get EXP and choose to recover part of their HP or MP. If the player’s HP becomes less than 0, the adventure will end as a failure. After some battles, the adventure will end as a success.

#### A list of features/functions to implement:

1. Insert player's name
  - Ask for the player's name and initialize the player's HP (500) and MP (0). Then store name, HP, and MP into "player.txt".
- File input/output:
  - Store the player's name in a file of player status. 

2. Display stage status
  - Display the status of the player and the monster in stages and rounds.
- File input/output:
  - Get the Hp and name of the monster, display from a file with monsters' status according to different game stages.
  - Get the Hp and Mp, display from a file with the player's status.
  - Read the player and monster to determine the winner of the battle.
- Data structures for storing game status:
  - Use a string array to store the HP and attack power of every monster temporarily.
- Program codes in multiple files:
  - The display function will be stored in another file to be reused, while the main function will run the battle. 
- Dynamic memory management:
  - Release the storage of the array of monsters data after displayed. Only store the data of the current stage's monster. 

3. Insert player's move
  - Player will choose between normal attack, rest, recover, and skill attack by inputting certain data. 
  - Depending on the player's MP, recover and skill attack may be unavailable.
- Data structures for storing game status:
  - May change the hp of a monster and store it in the array. 
  - May change the mp and hp of the player and store in the array. 

4. Generate the monster's move
- Generation of random game sets or events:
  - The monster will randomly choose a move. It will also choose skills when it has enough MP.
- Data structures for storing game status:
  - Will change the hp of the player and store it in the file after a stage.  
- If the player's Hp drop to 0, the player will lose.
- If the player kills all monsters, the player wins. 
5. Data validation
- The program will require the user input the data again if the previously input data is out of the given range.
- The program will require the user choose the action again if some conditions of the previous choice aren't satisfied.

6. Play again
- After a game, the player can choose to play the whole game again or exit the game.
- Choose 1 to play again and 2 to exit. 

#### non-standard C/C++ libraries: 
No
#### Compilation and execution instructions:
1. Player needs to make a name for his adventurer (less than 20 letters)
2. Every turn the player needs to choose his move by typing 1,2,3 or 4,whose corresponding action is attack,rest, healing and skill attack.
Among them,healing and skill attack require for enough Mp.
3. After the end of the game,you can choose to replay the game.
4. Compile with "make main", clean files (.o and main) with "make clean", and run with "./main" in terminal.
