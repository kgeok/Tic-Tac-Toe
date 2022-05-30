# Tic-Tac-Toe
A simple HTML/JS Tic-Tac-Toe game that can be played standalone or with a visual "scoreboard"

Using a Raspberry Pi hosting this alongside a circuit that contains a series of D-Latches, Demultiplexers and LEDs can help visualize the current game in real life.

### Part A:

![Circuit Part 1](https://github.com/kgeok/Tic-Tac-Toe/blob/master/circuitp1.png)

### Part B:

![Circuit Part 2](https://github.com/kgeok/Tic-Tac-Toe/blob/master/circuitp2.png)

The Raspberry Pi will act as a host that will serve both the Python program as well as web hosting for the HTML/JS game.
Using PHP the game will execute the Python program while passing the following arguments:

```console
foo@bar:~$ py TicTacToe.py COLOR_POSITION
```
Green/Red_Top,Center,Bottom + Left,Middle,Right

From there, the Python program will call the GPIO on the Raspberry Pi to set HIGH outputs that will activate the Demultiplexers to configure the appropriate D-Latches that power corresponding LEDs that match the postition that was called in the game.
