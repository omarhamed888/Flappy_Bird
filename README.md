# Flappy Bird Reinforcement Learning Project

This project implements a **Flappy Bird** game where an AI agent learns to play the game using **Q-learning** (a reinforcement learning algorithm). The agent learns by interacting with the environment and receiving rewards based on its actions, gradually improving its gameplay over generations.

The project consists of several components:

* **Reinforcement Learning Agent**: The agent uses Q-learning to make decisions.
* **Game Environment**: The Flappy Bird game environment where the agent interacts.
* **User Interface**: A graphical user interface for rendering the game and displaying relevant information.

## Features

* **Q-Learning Agent**: The agent learns to play the game through repeated interactions and updates its behavior using a Q-table.
* **Environment Simulation**: Simulates the Flappy Bird game, including movement of pipes, scoring, and collisions.
* **Graphical UI**: Displays the game window with bird movement, pipes, score, and other UI elements.
* **Multiple Generations**: The agent plays multiple generations, improving over time.

## Setup

To run the project, follow these steps:

### Prerequisites:

* Python 3.x
* Pygame library

### Installation:

1. Clone this repository:

   ```bash
   git clone https://github.com/omarhamed888/Flappy_Bird.git
   cd flappy-bird-rl
   ```

2. Install dependencies:

   ```bash
   pip install pygame numpy
   ```

3. Run the game:

   ```bash
   python main.py
   ```

### Saved Q-Table:

The Q-table is saved in the file `q_table.npy` after each generation. This file can be loaded to resume training or to evaluate the agent's learned behavior.

## Documentation

The project's documentation can be found in the `docs` folder. This includes detailed information about each code file and its components. To access the documentation, refer to the following files:

* [**`docs/algorithm.md`**](docs/algorithm.md): Explanation of the Q-learning agent.
* [**`docs/main.md`**](docs/main.md): Overview of the main game loop.
* [**`docs/display.md`**](docs/display.md): Information about the graphical rendering and UI elements.
* [**`docs/environment.md`**](docs/environment.md): Description of the Flappy Bird environment for reinforcement learning.
