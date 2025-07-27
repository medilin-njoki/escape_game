# Escape Game

A text-based escape game where the player has to find their way out of a mysterious house.

## The Story

You wake up on a couch in a strange house with no windows. You don't remember how you got there, but you know you have to escape. Explore the rooms, find clues, and solve puzzles to find your way out.

## How to Play

The game is played by typing commands into the console. The available commands are:

*   `explore`: To look around the room and see what items are in it.
*   `examine [item]`: To examine an item in the room. This might reveal a hidden key or another clue.
*   `yes`/`no`: To answer yes/no questions.
*   `head`/`tail`: To play heads or tails.

To start the game, run the `quest-room.ipynb` notebook.

## The Code

The game is written in Python and runs in a Jupyter Notebook. It uses the following libraries:

*   `pygame`: For playing background music and sound effects.
*   `rich`: For creating rich text and beautiful formatting in the terminal.
*   `IPython.display`: For playing audio in the notebook.

The game logic is contained in the `quest-room.ipynb` file. The game world is defined by a set of dictionaries that represent rooms, items, and their relationships. The game state is managed in a dictionary that is updated as the player progresses through the game.

### Game Logic

The core of the game is the `play_room` function, which is called recursively as the player moves from room to room. The player's actions are handled by the `explore_room` and `examine_item` functions.

When a player examines an item, the game checks if there is a key associated with that item. If there is, the key is added to the player's inventory.

To move between rooms, the player must first unlock the door with the correct key. After unlocking the door, the player must win a game of heads or tails to enter the next room.

The game ends when the player reaches the "outside" room.