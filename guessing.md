# Random Guessing Game Flowchart

This file contains the flowchart and a detailed textual description of the random guessing game. The game allows the user to guess a randomly generated number, with feedback provided for each guess.

## Flowchart
Below is the flowchart that describes the logical flow of the game using Mermaid syntax:

```mermaid
flowchart TD
    Start([Start]) --> GenerateRandomNumber[Generate a random number within the range]
    GenerateRandomNumber --> GetUserInput[Prompt user for a guess]
    GetUserInput --> ValidateInput{Is the input a valid number?}
    ValidateInput -->|No| InvalidInputMessage[Display "Invalid input. Try again."]
    InvalidInputMessage --> GetUserInput
    ValidateInput -->|Yes| CheckGuess{Is the guess correct?}
    CheckGuess -->|Correct| DisplayWinMessage[Display "You guessed it!"]
    CheckGuess -->|Too High| DisplayHighMessage[Display "Too high! Try again."]
    CheckGuess -->|Too Low| DisplayLowMessage[Display "Too low! Try again."]
    DisplayWinMessage --> End([End])
    DisplayHighMessage --> GetUserInput
    DisplayLowMessage --> GetUserInput
