flowchart TD
    Start([Start]) --> PromptUser[Prompt user to guess a number]
    PromptUser --> ValidateInput[Validate user input]
    ValidateInput -->|Valid| CheckGuess[Check if guess is correct]
    ValidateInput -->|Invalid| InvalidInput[Handle invalid input]
    InvalidInput --> PromptUser
    CheckGuess -->|TooHigh| GuessHigh[Inform user guess is too high]
    CheckGuess -->|TooLow| GuessLow[Inform user guess is too low]
    CheckGuess -->|Correct| CorrectGuess[Inform user guess is correct]
    GuessHigh --> PromptUser
    GuessLow --> PromptUser
    CorrectGuess --> End([End])
Start: The game begins by initializing the process and setting up a random number for the user to guess.

Prompt User to Guess a Number: The system prompts the user to input their guess of the random number.

Validate User Input: The system checks if the user's input is valid, ensuring that it's a number and falls within the allowed range.

Invalid Input: If the user provides invalid input (e.g., a non-number or out-of-range guess), the game will display an error message and prompt the user to try again.
Check if Guess is Correct: If the input is valid, the system checks the guess against the correct number.

Too High: If the user's guess is higher than the correct number, the game informs the user and prompts them to guess again.

Too Low: If the user's guess is lower than the correct number, the game informs the user and prompts them to guess again.

Correct Guess: If the user guesses the correct number, the game congratulates the user and the game ends.

End: The game ends when the user correctly guesses the number.

3. Edge Cases to Consider in Tests:
Invalid input: Ensure that the system handles cases where the user inputs a non-numeric or out-of-range value.
Number Boundary Testing: Test that the system correctly handles edge cases, like the highest and lowest possible guesses.
Repeated Guesses: Ensure the system loops back correctly if the guess is too high or too low.
Exact Match: Validate that the system ends correctly when the user guesses the correct number.
