# `main.py` - Main Game Loop

This file contains the main game loop for the Flappy Bird game and interacts with the Q-learning agent defined in `algorithm.py`. It also loads and runs the game environment defined in `environment.py`.

## Main Game Flow

### `main()`
- **Purpose**: The entry point of the game, where the environment and agent are initialized and the game loop is run.
- **Initialization**:
  - Pygame is initialized, and a window is set up.
  - The environment (`FlappyBirdEnv`) and the Q-learning agent (`QLAgent`) are created.
  - If a saved Q-table exists, it is loaded from the file `q_table.npy`.
  
### Game Loop:
- **Game Mechanics**:
  - The game proceeds through multiple generations, where the agent interacts with the environment and learns to improve its performance.
  - The agent chooses actions based on the current state, performs the action in the environment, and updates the Q-table.
  - The game state is rendered after each action.
  
- **Generation Saving**: After each generation, the Q-table is saved to `q_table.npy` for future use.

### Pygame Events:
- Listens for key events like quitting the game or pressing the spacebar to start the game.
- Updates the Q-table after each action and tracks the agent's progress.

---