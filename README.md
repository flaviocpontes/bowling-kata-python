# Bowling Game

Write a function that, receiving a complete list of rolls, calculates the score of the game.

## Definition

The game is composed of 10 frames. Frames 1 through 9 are composed of at most 2 rolls and frame 10 is composed at most of 3 rolls.

The player can knock up to 10 pins per frame. A roll is called a **strike** if the 10 pins are knocked in the first roll of a frame. It is called a **spare** if the the 10 pins are knocked in the second roll of the frame.

The score of a frame is the sum of the pins knocked by the player in its 2 rolls. Whenever the player rolls a spare, the next roll is added to the frame score; if the player rolls a strike the following 2 rolls are added to that frames score.

The game score is the sum of the 10 frames' scores.

A Frame's maximum score is 30 and a game's maximum score is 300.

## Examples

- Normal frame score: [3|2] = 5
- Spare frame: [4|6] [3|2] = 13 + 5
- Strike frame: [10|-] [3|2] = 15 + 5

## Full Game Score examples

- [1|1] [1|1] [1|1] [1|1] [1|1] [1|1] [1|1] [1|1] [1|1] [1|1] =  2 + 2 + 2 + 2 + 2 + 2 + 2 + 2 + 2 + 2 = 20
- [10|-] [10|-] [10|-] [10|-] [10|-] [10|-] [10|-] [10|-] [10|-] [10|10|10] = 30 + 30 + 30 + 30 + 30 = 30 + 30 + 30 + 30 + 30 = 300
- [3|4] [5|5] [3|7] [4|5] [2|7] [8|2] [10|-] [0|10] [0|4] [8|1] = 7 + 13 + 14 + 9 + 9 + 20 + 20 + 10 + 4 + 9 = 115

## Pytest

You can do this Kata without any dependencies whatsoever, but in cas you'd like a more Pythonic way of testing, just run `pip install pytest`