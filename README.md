# Math Quiz Game

This project is a simple console-based math quiz game implemented in C++. It allows the user to select the difficulty level and type of mathematical operations for the quiz. The game supports addition, subtraction, multiplication, and division, as well as mixed operations.

## Features

- Selectable difficulty levels: Easy, Medium, Hard, and Mixed.
- Multiple operations: Addition, Subtraction, Multiplication, Division, and Mixed.
- Randomized questions based on the chosen level and operation.
- Immediate feedback on the user's answers with the correct answer displayed.
- Option to play multiple rounds.

## How to Run

1. **Compile the Program:**
   Use a C++ compiler like `g++` to compile the code.
   ```sh
   g++ -o math_quiz_game math_quiz_game.cpp
   ```

2. **Run the Program:**
   Execute the compiled program.
   ```sh
   ./math_quiz_game
   ```

## Game Structure

### Enums

- `enQuizLevel`: Represents the quiz difficulty levels.
  - `Easy` = 1
  - `Mid`
  - `Hard`
  - `LvLMix` (Mixed levels)

- `enQuizOperations`: Represents the types of operations.
  - `Add` = 1
  - `Sub`
  - `Mul`
  - `Div`
  - `OpMix` (Mixed operations)

### Structs

- `stMathGame`: Stores information about the current game state.
  - `Level`: Quiz difficulty level.
  - `Operation`: Type of operation.
  - `chOperation`: Character representation of the operation.
  - `FirstNumber`: First number in the question.
  - `LastNumber`: Second number in the question.
  - `PlayerAnswer`: Answer provided by the player.
  - `TheAnswer`: Correct answer.
  - `RightAnswersTimes`: Count of right answers.
  - `WrongAnswersTimes`: Count of wrong answers.
  - `QuizLength`: Number of questions in the quiz.
  - `RoundNumber`: Current round number.

- `stPlayer`: Stores information about the player.
  - `Name`: Player's name.
  - `Choice`: Player's choice.
  - `WinCount`: Number of wins.
  - `DrawCount`: Number of draws.
  - `LoseCount`: Number of losses.
  - `RoundsPlayed`: Number of rounds played.
  - `IsRoundWinner`: Whether the player won the round.

## Game Flow

1. **StartGame**: Initiates the game and loops to allow multiple rounds.
2. **StartQuiz**: Handles the main quiz logic including reading the quiz level, operation, and processing each question.
3. **Question**: Generates a question based on the selected difficulty and operation.
4. **CheckQuestionResult**: Checks if the player's answer is correct and updates the game state accordingly.
5. **RightAnswer / WrongAnswer**: Functions to handle correct and incorrect answers, providing feedback to the player.

## Helper Functions

- `Tabs`: Creates a string of tab characters.
- `ReadPlayerName`: Reads the player's name from input.
- `ReadPlayerInfo`: Reads player information.
- `ReadNumber`: Reads a floating-point number from input.
- `ReadPositiveNumber`: Reads a positive short number within a specified range.
- `ReadNumberInRange`: Reads a short number within a given range.
- `RandNumberInRange`: Generates a random number within a specified range.
- `ReadChar`: Reads a character from input.
- `RingBell`: Rings the system bell.
- `ResetScreen`: Clears the screen and resets the console color.
- `DisplayQuestionsLevel`: Returns a string representation of the question levels.
- `DisplayQuizOperations`: Returns a string representation of the quiz operations.
- `ReadQuizLength`: Reads the desired length of the quiz from input.
- `IsContinuePlay`: Asks the player if they want to continue playing.
- `GetMixOperation`: Randomly selects a mixed operation.
- `CalculateTheRightAnswer`: Calculates the correct answer based on the operation and operands.
- `EasyLevel / MidLevel / HardLevel / MixLevel`: Functions to set the operands based on the difficulty level.
- `GetQuestionsNumbers`: Sets the question numbers based on the difficulty level.
- `ReadQuizLevel`: Reads the quiz level from input.
- `GetcharOperation`: Gets the character representation of the operation.
- `ReadQuizOperation`: Reads the quiz operation from input.
- `ReadPlayerAnswer`: Reads the player's answer from input.
- `DisplayTheQuestion`: Displays the current question to the player.


