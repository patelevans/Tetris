# Tetris

I used pygame to create a Tetris clone as a way to learn more about how game logic flows.
The core logic is as follows:
- At any point in time, there is a list of locked positions that Tetrominos in freefall can not exist in.
- If this list of locked positions contains a position in the top row, then the user loses the game.
- As Tetrominos fall, the positions occupied by the falling Tetromino is checked against the list of locked positions. If there is a collision, then the Tetromino has fallen one position too far, and is translated upwards by one position. Then, all of the positions occupied by that Tetromino are added to the list of locked positions. This process repeats until the player loses the game.
- When any row on the game board fully consists of locked positions, then that row is deleted, a new row is added at the top of the game board, and the locked positions that were previously above that row are adjusted accordingly.

To play the game, make sure you have pygame on your computer. If you do not, you can get it via the command `pip3 install pygame`. Once the pygame dependency is installed, run the command `python3 tetris.py` to play the game.