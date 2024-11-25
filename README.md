# Snake Game 🐍

## Description

This is a classic Snake Game built using Python's turtle graphics module. The goal of the game is to control a snake to eat food, causing it to grow longer while avoiding collisions with the walls or its own body. The game tracks your score and ends when the snake crashes into the wall or itself.

This project demonstrates **object-oriented programming (OOP)** concepts, including creating and managing multiple classes for different components of the game such as the Snake, Food, and Scoreboard.

## Features

- **Snake Movement**: Use the arrow keys to control the snake (Up, Down, Left, Right).
- **Food Collection**: Each time the snake eats food, it grows longer, and your score increases.
- **Collision Detection**: The game ends if the snake hits the wall or itself.
- **Score Tracking**: The game displays the current score at the top of the screen.
- **Game Over**: Displays a "GAME OVER" message when the game ends.

## Requirements

- Python 3.x
- `turtle` graphics module (pre-installed with Python)

## How to Play

1. **Start the Game**:
   - Run the `game.py` script to start playing.

2. **Control the Snake**:
   - Use the arrow keys to move the snake:
     - Up Arrow: Move up
     - Down Arrow: Move down
     - Left Arrow: Move left
     - Right Arrow: Move right

3. **Eat the Food**:
   - The snake will grow longer each time it eats the food, and your score will increase accordingly.

4. **Avoid Collisions**:
   - If the snake hits the wall or itself, the game will end, and the final score will be displayed.

## Code Structure

### Files Breakdown

Here is a breakdown of each file and its purpose in the game:

---

### `game.py`

- **Purpose**: This is the main file that runs the game. It sets up the game window, initializes the game objects (snake, food, scoreboard), and controls the flow of the game.
- **Key Functionality**: It contains the game loop where the snake moves, checks for food collisions, handles score updates, and checks for game-over conditions.

---

### `snake.py`

- **Purpose**: This file defines the `Snake` class, which creates and manages the snake. It controls the snake’s movement, growth, and direction.
- **Key Functions**:
  - `create_snake()`: Initializes the snake with three segments.
  - `add_segment(position)`: Adds a new segment to the snake.
  - `extend()`: Adds an additional segment to the snake when it eats food.
  - `move()`: Moves the snake forward by updating the position of its segments.
  - `up()`, `down()`, `left()`, `right()`: Methods for changing the direction of the snake.

---

### `food.py`

- **Purpose**: This file defines the `Food` class that generates food at random positions for the snake to eat.
- **Key Functions**:
  - `refresh()`: Moves the food to a random position within the screen boundaries.

---

### `scoreboard.py`

- **Purpose**: This file defines the `Scoreboard` class that manages the score display. It updates the score and displays the "GAME OVER" message when the game ends.
- **Key Functions**:
  - `update_scoreboard()`: Displays the current score.
  - `increase_score()`: Increases the score by 1 and updates the displayed score.
  - `game_over()`: Displays the "GAME OVER" message when the game ends.

---

## How to Run

1. Clone or download the project files.
2. Make sure Python 3.x is installed on your computer.
3. Open a terminal or command prompt and navigate to the project directory.
4. Run the following command to start the game:

```bash
python game.py
```
## Future Improvements

- **Sound Effects**: Add sounds when the snake eats food or when the game ends.
- **Increasing Difficulty**: Gradually increase the speed of the game as the snake grows longer.
- **Graphical User Interface (GUI)**: Implement a graphical interface with more advanced features, such as a menu or settings screen.
- **Leaderboard**: Save and display high scores for multiple players. ( DONE )

## Credits

This project was created as an exercise to demonstrate object-oriented programming (OOP) principles and basic game development using Python's `turtle` graphics module.

## Change Log - Version 1.2.1

### 1. **High Score Tracking** 🏆
 - The game now saves the High Score to a data.txt file.

## Change Log - Version 1.2.0

### 1. **High Score Tracking** 🏆
   - The game now tracks the **high score** across multiple sessions. Each time the game is reset, the current score is compared to the high score, and if the current score is higher, the high score is updated.
   - The score and high score are displayed at the top of the screen, providing players with a continuous challenge to beat their best score.

### 2. **Indefinite Gameplay** 🎮
   - The game no longer displays a "GAME OVER" message when the snake collides with the wall or its own body. Instead, the snake resets, and gameplay continues indefinitely.
   - The game only ends when manually closed by the user, offering an ongoing challenge to see how long players can keep the snake alive.

### 3. **Improved Snake Reset Mechanism** 🔄
   - When the snake collides with itself or the walls, it is reset to its starting position, and the score is reset to 0. This allows players to quickly continue without interruption.
   - The game logic has been streamlined to ensure a smooth reset process.

### 4. **Optimized Game Loop**
   - The game loop has been further optimized to ensure smoother performance, with a slight delay (`time.sleep(0.1)`) between each movement of the snake, allowing for more fluid controls and gameplay.
   
## Bug Fixes
- Fixed minor display issues with the score updating during gameplay.
  
## Known Issues
- The game currently has no visual indication when it’s over (besides the player manually closing the game window).
