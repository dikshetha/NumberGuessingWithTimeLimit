# Number-Guessing-With-TimeLimit
## Rules: 
In the Time Limit Guessing Game implemented in the given code, there is one main role for the player:
1. **Player:** The role of the player is to interact with the game through the terminal (command-line interface). The player needs to guess the target number within the time limit of 10 seconds.

The player's actions in the game involve:

- Entering their guesses for the target number when prompted.
- Trying to guess the correct number within the given time frame.
- Reacting to hints provided by the game (e.g., "Try a higher number" or "Try a lower number") based on their guesses.
- Achieving the objective of guessing the correct number or recognizing when the time limit is reached and the game is over.

The game manager (represented by the `time_limit_guessing_game()` function) handles the game's logic and flow, generates the target number, starts the timer, and determines the game's outcome based on the player's input and the time limit.

As the code is designed to be a simple text-based guessing game, it doesn't involve any complex player roles or interactions beyond the player trying to guess the correct number within the time limit. The player's role is to enjoy the challenge of guessing the number while being under the constraint of the time limit.
### About code
Sure! Let's go through each term in the code and explain its purpose:

1. `random.randint(1, 100)`: This function call is used in the `generate_random_number()` function to generate a random integer between 1 and 100 (inclusive). The `random` module provides this functionality.

2. `get_user_guess()`: This function is responsible for getting the player's guess as input. It uses a `while` loop to keep asking for input until the player enters a valid integer between 1 and 100. If the player enters anything other than a valid integer, they will be prompted to enter a valid number.

3. `time.time()`: This function from the `time` module is used to get the current time in seconds since the epoch. It helps to track the elapsed time during the game.

4. `target_number = generate_random_number()`: The game generates the target number that the player needs to guess using the `generate_random_number()` function. This will be the number that the player has to guess within the time limit.

5. `start_time = time.time()`: The `time.time()` function is used to get the current time at the start of the game, which helps to track the elapsed time during the game.

6. `while time.time() - start_time <= 10:`: This is the main game loop, which runs as long as the difference between the current time and `start_time` is less than or equal to 10 seconds. This ensures that the game lasts for 10 seconds.

7. `user_guess = get_user_guess()`: During each iteration of the loop, the game prompts the player to enter their guess using the `get_user_guess()` function.

8. `if user_guess == target_number:`: The player's guess is then compared with the `target_number`. If the guess is correct, the game congratulates the player, prints "Congratulations! You guessed the correct number," and returns from the function, ending the game.

9. `elif user_guess < target_number:`: If the guess is not correct, the game provides a hint by printing "Try a higher number" if the guess is smaller than the target number.

10. `else:`: If the guess is not correct and greater than the target number, the game prints "Try a lower number."

11. If the time limit (10 seconds) is reached and the player hasn't guessed the correct number, the game prints "Time's up!" along with the correct `target_number`.

12. The `if __name__ == "__main__":` block is used to ensure that the `time_limit_guessing_game()` function is called only when the script is run directly and not when it's imported as a module.

Overall, this code creates a simple text-based number guessing game with a time limit of 10 seconds. The player needs to guess the target number within this time frame, and the game provides hints to help them make accurate guesses.
