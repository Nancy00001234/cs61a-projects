# The Gaame of Hog
Develop a simulator, game rules, and multiple strategies for the dice game Hog using higher-order functions, controls, and mutations in Python.  
Implement functions to calculate the average win rate of various Hog strategies, and determine the number of rolls (1 - 10) that gives the maximum average score for a turn.

![image](https://user-images.githubusercontent.com/104662491/207876132-b8be1fc3-0c88-4e8e-9a88-4d8e4bc7683c.png)

## Usage Guide  
To play with yourself, run the GUI from the terminal:
```
$ python3 hog_gui.py   
```
To play against the final strategy created in hog.py (function final_strategy):
```
$ python3 hog_gui.py -f
```
The project can also calculate the average win rate of different strategies by calling run_experiments using the -r option. The orginal code calculates the avergare win rate of the final strategy against the baseline strategy of always_roll(4). You should find that it wins slightly more often than it loses, giving a win rate around 0.58.
```
$ python3 hog.py -r
final_strategy win rate: 0.5974999999999999
```
You can also modify run_experiments and baseline in average_win_rate to see the other strategies' average win rates. For example, change the second if False: to if True: in run_experiments, to evaluate always_roll(8) against the baseline strategy of always_roll(4).
```
$ python3 hog.py -r
always_roll(8) win rate: 0.544
```
To calculate the number of rolls (1 to 10) that gives the highest average turn score, change the first if False: to if True: in run_experiments.
```
$ python hog.py -r
Max scoring num rolls for six-sided dice: 6
```

## Directory
```
│  calc.py
│  dice.py
│  hog.py
│  hog_gui.py
│  proj01.ok
│  ucb.py
│  
├─images
│      die1.gif
│      die2.gif
│      die3.gif
│      die4.gif
│      die5.gif
│      die6.gif
│      
├─tests
│      00.py
│      01.py
│      02.py
│      03.py
│      04.py
│      05.py
│      06.py
│      07.py
│      08.py
│      09.py
│      10.py
│      11.py
│      12.py
│      check_strategy.py
│      play.sol
│      play_utils.py
│      __init__.py
│      
└─__pycache__
        dice.cpython-310.pyc
        hog.cpython-310.pyc
        ucb.cpython-310.pyc
```        

> Game Rules
> - Pig Out. If any of the dice outcomes is a 1, the current player's score for the turn is 1.
>   - Example 1: The current player rolls 7 dice, 5 of which are 1's. They score 1 point for the turn.
>   - Example 2: The current player rolls 4 dice, all of which are 3's. Since Pig Out did not occur, they score 12 points for the turn.
> - Free Bacon. A player who chooses to roll zero dice scores 2 more than the absolute difference between the digits in the opponent's total score.
>   - Example 1: If the opponent has 42 points, the current player gains 2 + abs(4 - 2) = 4 points by rolling zero dice.
>   - Example 2: If the opponent has 48 points, the current player gains 2 + abs(4 - 8) = 6 points by rolling zero dice.
>   - Example 3: If the opponent has 7 points, the current player gains 2 + abs(0 - 7) = 9 points by rolling zero dice.
> - Swine Swap. After points for the turn are added to the current player's score, if both scores are larger than 1 and either one of the scores is a positive integer multiple of the other, then the two scores are swapped.
>   - Example 1: The current player has a total score of 37 and the opponent has 92. The current player rolls two dice that total 9. The opponent's score (92) is exactly twice the player's new total score (46). These scores are swapped! The current player now has 92 points and the opponent has 46. The turn ends.
>   - Example 2: The current player has 91 and the opponent has 37. The current player rolls five dice that total 20. The current player has 111, which is 3 times 37, so the scores are swapped. The opponent ends the turn with 111 and wins the game.
