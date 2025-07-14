import random

def roll_dice(sides=6):
    return random.randint(1, sides)

def main():
    print("Welcome to the Dice Guessing Game!")
    score = 0
    rounds = 0

    while True:
        guess = input("Guess the dice roll (1-6), or 'q' to quit: ").strip()
        if guess.lower() == 'q':
            break

        if not guess.isdigit() or not 1 <= int(guess) <= 6:
            print("Invalid input! Please enter a number between 1 and 6, or 'q' to quit.")
            continue

        guess = int(guess)
        result = roll_dice()
        print(f"The dice rolled: {result}")

        if guess == result:
            print("Congratulations! You guessed correctly.")
            score += 1
        else:
            print("Sorry, that's not correct.")

        rounds += 1
        print(f"Current score: {score}\n")

    print(f"Thanks for playing! You played {rounds} rounds and scored {score} points.")

if __name__ == "__main__":
    main()
