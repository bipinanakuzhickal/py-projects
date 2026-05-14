# Blackjack Game

A simple command-line Blackjack game implemented in Python. This script deals cards to the user and computer, calculates scores, and determines the game outcome using Blackjack rules.

## Files

- `solution.py` - Main game script for playing Blackjack.

## Requirements

- Python 3.6+
- `art.py` 


## Usage

Run the game from the command line:

```bash
python solution.py
```

The script will prompt you to start a new game. Type `y` to play or `n` to exit.

During the game, you can choose whether to draw another card or pass:

- Type `y` to get another card
- Type `n` to pass

## Gameplay

- The user and the computer each start with two cards.
- The score is calculated as the sum of card values.
- A Blackjack (an Ace and a ten-value card) is treated as a special score.
- The computer draws cards until its score is 17 or higher.
- The script prints the final hands and the game result.

## Notes

- Aces are worth `11` or `1`, depending on whether the hand would bust.
- Tens, Jacks, Queens, and Kings are represented as `10`.
- The script uses `input()` for user interaction, so it should be run in a terminal.
