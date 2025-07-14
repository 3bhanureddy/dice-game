# Guessing Dice Game 🎲

A simple command-line game where you try to guess the outcome of a rolled dice. Perfect for practicing basic programming and having some fun!

## How to Play

1. The computer rolls a six-sided dice (numbers 1–6).
2. You guess what number the dice will show.
3. If your guess is correct, you win!
4. If not, you can try again or quit.

## Features

- Random dice roll simulation
- User input for guesses
- Tracks attempts
- Simple, beginner-friendly code

## Example Code (Python)

```python
import random

def guessing_dice_game():
    print("Welcome to the Guessing Dice Game!")
    attempts = 0
    while True:
        dice = random.randint(1, 6)
        guess = input("Guess the dice roll (1-6) or 'q' to quit: ")
        if guess.lower() == 'q':
            print("Thanks for playing!")
            break
        attempts += 1
        if int(guess) == dice:
            print(f"Congratulations! You guessed correctly in {attempts} tries.")
            break
        else:
            print(f"Wrong! The dice showed {dice}. Try again.")

if __name__ == "__main__":
    guessing_dice_game()
```

## Getting Started

1. Copy the Python code above into a file (e.g., `dice_game.py`).
2. Run the game with `python dice_game.py`.
3. Follow the on-screen instructions.

## Contributing

Feel free to fork the repo and submit pull requests for improvements or alternative versions in other languages!

## License

This project is open source under the MIT License.
