# Rock Paper Scissors Game

In this project I have created a program to play Rock, Paper, Scissors against a bot. It's program that picks at random will usually win 50% of the time. We play matches against four different bots and to win player needs to win at least 60% of the games in each match.

In the file `RPS.py` we write a function called `player`. The function takes an argument that is a string describing the last move of the opponent ("R", "P", or "S"). The function returns a string representing the next move for it to play ("R", "P", or "S").

A `player` function will receive an empty string as an argument for the first game in a match since there is no previous play.

The `player` function is defined with two arguments (`player(prev_play, opponent_history = [])`). The function is never called with a second argument so that one is completely optional. The reason why the `player` function contains a second argument (`opponent_history = []`) is because that is the only way to save state between consecutive calls of the `player` function. You only need the `opponent_history` argument if you want to keep track of the opponent_history.

### Development

The `RPS.py` file contains the logic to beat the bots.
The logic for bots is written in `RPS_game.py`. 
`main.py` imports the game function and bots from `RPS_game.py`.

To test the code, we play a game with the `play` function. The `play` function takes four arguments:
- two players to play against each other (the players are actually functions)
- the number of games to play in the match
- an optional argument to see a log of each game. Set it to `True` to see these messages.

```py
play(player1, player2, num_games[, verbose])
```
For example, here is how you would call the function if you want `player` and `quincy` to play 1000 games against each other and you want to see the results of each game:
```py
play(player, quincy, 1000, verbose=True)
```

Click the "run" button and `main.py` will run.

### Testing

The unit tests for this project are in `test_module.py`. We imported the tests from `test_module.py` to `main.py`. If we uncomment the last line in `main.py`, the tests will run automatically whenever we run the `main.py` file.