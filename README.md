# Connect Four AI player
We made a connect 4 game which utilizes python's built in turtle objects to draw
the board and various pieces on the board. Additionally, we created an ai which
utilizes a mini-max algorithm optimized with alpha beta pruning to find the
best possible move based on a scoring system that evaluates a given new piece.

<p align="center">
<img src="./AI_player.gif" alt="AI playing" width="500" />
</p>
<p align="center">
AI playing yellow pieces exploring 5 moves in advance
</p>

## To Run
Double click on our run.py, or run in the terminal directory

```
python3 run.py
```

To change the AI strength, edit the two lines below in the playon.py \_\_init__ section:

```python
#playerX = [name, AI or Human, smart or random AI, recursive depth]
self.playerA = ['A', None, 'smart', 5]
self.playerB = ['B', None, 'smart', 5]
```

To increase recursive depth (or "piles") to 7:
```python
#playerX = [name, AI or Human, smart or random AI, recursive depth]
self.playerA = ['A', None, 'smart', 7]
self.playerB = ['B', None, 'smart', 7]
```

To use random AI and not minimax AI:
```python
#playerX = [name, AI or Human, smart or random AI, recursive depth]
self.playerA = ['A', None, 'random', 7]
self.playerB = ['B', None, 'random', 7]
```

## Classes
We made classes for each type of object that we use in our code. This includes
a class for the board, graphics, ai, playon (a class which controls
various aspects of the game) and run (a class which connect all the other
classes together). We made these classes to easily access data in
the whole program, and we made sure that our classes cover a more general case.
These will enable us to make variations on things to use in other classes
(e.g. created a new board in the ai class to test various moves on).

## Testing
We have two files that are not used within the program: check_winning_algorithm.py and
check_ai_algorithm.py. While not utilized in the program itself, these files were used
to test our endgame function and test that our ai evaluates the correct
score in certain situations.

## Suggestions
For graphics, we could have made the game a little more flashy, or added
additional features, but all of the necessities are there. When initialized, the
board gives the user 3 options: (human vs. human, human vs. ai, and ai vs. ai).
While the 'ai vs. ai' option was mostly designed for testing our ai and
checking for bugs, it is still interesting to see the computer play against
itself. After the user has made their choice, our program displays all the
pieces and the board. The user can click the desired spot to place a piece. They
must click the actual space and not above or where another piece already is. If
a player clicks an invalid spot a message will be put in the terminal, and the
program will wait for a valid move. 

# Issues
Currently, our program does not have any known bugs, and the only issue that
can occur is long waiting times when the ai is set to search more than 5 moves
in advance. Therefore we will set the depth of the mini-max algorithm fairly
low to 5 maintain a reasonable computation time.


