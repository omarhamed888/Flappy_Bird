# Flappy Bird AI with Reinforcement Learning

This project implements an AI agent that learns to play the Flappy Bird game using the Q-learning reinforcement learning algorithm. The AI is trained by interacting with the game environment, receiving rewards for its actions, and updating its knowledge (stored in a Q-table) to make better decisions over time.

## Features

* **Q-Learning Implementation:** Utilizes the Q-learning algorithm to train the AI agent.
* **Epsilon-Greedy Exploration:** Balances exploration of new actions with exploitation of learned knowledge using an epsilon-greedy policy.
* **State Discretization:** Discretizes the continuous game state (bird position, pipe position) into a finite number of bins for effective learning.
* **Action Space:** The AI can choose between two actions: do nothing or jump (flap).
* **Training Mode:** Allows the AI to learn from scratch or continue learning.
* **Playing Mode:** Enables the user to watch a pre-trained AI play the game using its learned policy.
* **Save and Load Q-Tables:** The trained Q-table can be saved to a file and loaded later for continued training or gameplay.
* **Start Screen Options:** Provides a user-friendly interface to choose between training a new AI, watching a trained AI play, or loading a saved Q-table.
* **Q-Table Selection Screen:** Allows the user to easily select a specific Q-table file to load from a directory.
* **Real-time Game Visualization:** Uses Pygame to display the Flappy Bird game environment and the AI's actions.
* **Learning Rate and Epsilon Decay:** Gradually reduces the learning rate and exploration rate during training to promote convergence to an optimal policy.
* **Score and Generation Tracking:** Displays the current score and the training generation number.
* **Best Score Tracking:** Keeps track of the highest score achieved during training.
* **Training Parameter Display:** Shows the current epsilon and learning rate during training.

## Prerequisites

* **Python 3.x**
* **Pygame** (`pip install pygame`)
* **NumPy** (`pip install numpy`)
* **Pickle** (standard Python library, no installation needed)

## Getting Started

1.  **Clone the repository** (or download the files).
2.  **Ensure you have the required libraries installed** (see Prerequisites).
3.  **Place the game assets** (`base.png`, `pipe.png`, `bg.png`, `bird1.png`) in the same directory as the Python script. You can usually find these assets in standard Flappy Bird game resources online.
4.  **Run the script:** `python your_script_name.py` (replace `your_script_name.py` with the actual name of the Python file).

## Usage

Upon running the script, you will see a start screen with the following options:

* **Train New AI:** Starts the training process from scratch. The AI will explore the game environment and learn through the Q-learning algorithm.
* **Watch AI Play:** Allows you to load a pre-trained Q-table and watch the AI play the game based on its learned policy. You will be presented with a screen to select a `.pkl` file from the `q_tables` directory.
* **Load Q-Table:** Directly opens the Q-table selection screen to load a saved Q-table for either watching the AI play or potentially continuing training (though the current implementation restarts the game after loading in "play" mode).

### Training the AI

* Select "Train New AI" from the start screen.
* The game will begin, and the AI will start playing (and likely crashing initially).
* Observe the score and the generation number. The AI will gradually improve its performance over many generations.
* The Q-table is saved periodically (every `SAVE_INTERVAL` generations) to the `q_tables` directory.
* You can stop the training at any time by pressing the **Escape** key. The current Q-table will be saved upon quitting.

### Watching a Trained AI Play

1.  Select "Watch AI Play" from the start screen.
2.  A screen will appear listing the saved Q-table files in the `q_tables` directory. Use the **Up** and **Down** arrow keys to select a Q-table and press **Enter** to load it. Press **Escape** to cancel and return to the start screen.
3.  Once a Q-table is loaded, the AI will play the game using its learned strategy.
4.  Press the **Escape** key to stop watching.

### Loading a Q-Table

* Selecting "Load Q-Table" from the start screen will take you to the Q-table selection screen, similar to the "Watch AI Play" option. After loading, the script currently proceeds as if you selected "Watch AI Play".

## Configuration

The following parameters can be adjusted within the Python script to influence the AI's learning process and the game environment:

* **Game Constants:**
    * `SW`: Screen width.
    * `SH`: Screen height.
    * `BASEY`: Height of the ground.
    * `FPS`: Frames per second.
* **Learning Parameters:**
    * `INITIAL_LEARNING_RATE`: Initial value for the learning rate ($\alpha$).
    * `LEARNING_RATE_DECAY`: Rate at which the learning rate decreases.
    * `MIN_LEARNING_RATE`: Minimum value for the learning rate.
    * `DISCOUNT_FACTOR`: Discount factor ($\gamma$) for future rewards.
    * `INITIAL_EPSILON`: Initial value for the exploration rate ($\epsilon$).
    * `EPSILON_DECAY`: Rate at which the exploration rate decreases.
    * `MIN_EPSILON`: Minimum value for the exploration rate.
* **State Dimensions:**
    * `X_BINS`: Number of discrete bins for the horizontal distance to the next pipe.
    * `Y_BINS`: Number of discrete bins for the vertical distance to the next bottom pipe.
    * `ACTIONS`: Number of possible actions (should be 2 in this case).
* **Saving Interval:**
    * `SAVE_INTERVAL`: Number of generations after which the Q-table is saved.

Adjusting these parameters can significantly affect the AI's learning speed and the quality of the learned policy.

## File Structure