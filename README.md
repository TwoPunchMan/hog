# CS61A - The Hog Project - Spring 2022
The Hog Project is courtesy of UC Berkeley - CS61A.<br>
The objective of the game is to score 100 points shooting dice before your opponent does.

## Disclaimer:
To whomever is reading this: good luck with this project.<br>
I am not a Berkeley student.<br>
I did not attend Berkeley as an undergrad.<br>
The purpose of this repo is to help myself learn good CS theory, as per [teachyourselfcs.com](https://www.teachyourselfcs.com)<br>
If this code helped anyone out there, great. If not, that's okay too.<br>
That's about it.
<br>
<br>
Now on to the fun stuff:

## Rules:
In Hog, two players alternate turns trying to be the first to end a turn with at least 100 total points. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes. However, if a die shows 1, that player's score for the turn is 1.

## Special Rules:
**Hefty Hogs**:
- If the opponent's score is 0 and the player chooses to roll zero dice, the player will get 1 point. However, if the opponent's score is not 0, a player who chooses to roll zero dice will gain points according to the following:

The opponent's score will be mapped to a series of functions to be applied to the player's score, starting from the rightmost digit (the one's place) and ending on the leftmost digit.
Each digit from 0 to 9 corresponds to a pre-defined function, f0 through f9.
The result of this series of calls modulo 30 is the amount of points the player receives for the turn.

**Hog Pile**
- After points for the turn are dealt with, if the last digit of the player's score is = to the opponent's, the player gets a boost to his score by the last digit (e.g. Turn outcome: player 123 vs. opp 453 -> player score becomes 126 (123 + 3) vs 453)

### Issues/Bugs?
- couldn't pass the fuzz test on problem 5 suite 5 case 87. Kinda gave up on that one.
- problem 10 suite 1 case 4. Test not passing
