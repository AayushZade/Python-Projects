---
# Blackjack Game in Python 🃏

## Overview

This is a simple console-based implementation of the popular card game **Blackjack**. In this game, you will play against the computer, with both participants trying to reach a score as close as possible to 21 without going over. The game follows the basic rules of Blackjack, including handling Aces and the computer's strategy to draw cards until a certain score.

## Rules of the Game

1. The player and the computer are each dealt two cards.
   - The player can see both of their cards and one of the computer's cards.
2. The player can choose to "hit" (draw another card) or "stand" (keep their current hand).
   - The player can keep drawing cards until they choose to stand or until their score exceeds 21, resulting in an automatic loss (bust).
3. The computer will draw cards until its score is at least 17.
   - If the computer's score exceeds 21, the player wins by default.
4. Aces are worth either 11 or 1, depending on which keeps the score below or equal to 21.

## Scoring

- Number cards (2-10) are worth their face value.
- Face cards (Jack, Queen, King) are worth 10.
- Aces can be worth either 1 or 11, depending on the player's total score.

## How to Play

1. Run the script, and you'll be prompted whether you want to play the game or not.
2. If you choose to play, you will receive your first two cards, and the computer will receive one card.
3. After seeing your initial cards, you can choose to draw more cards or stand.
4. The game will automatically compare scores once you stand or bust, and the winner will be announced.

## Game Flow

- **Initial Setup**: You and the computer are each dealt two cards (the computer's second card is hidden).
- **Player's Turn**: You decide whether to draw more cards ("hit") or keep your current hand ("stand").
- **Computer's Turn**: The computer will keep drawing cards until its score is 17 or higher.
- **Winner Announcement**: The winner is determined based on who has the highest score without exceeding 21.

## Example

```text
Do you want to play the game of Blackjack? Type 'y' or 'n': y
Your cards: [8, 10], current score: 18
Computer's first card: 6
Type 'y' to get another card, type 'n' to pass: n
Your Final Hand: [8, 10], final score: 18
Computer's Final Hand: [6, 9, 2], final score: 17
You Win 😎
```

## How to Run

1. Clone or download this repository.
2. Ensure you have Python installed.
3. Run the `blackjack.py` script:

```bash
python blackjack.py
```
