# `display.py` - Game Rendering and UI

This file handles the graphical display of the game using Pygame. It defines the methods to render the game environment and user interface elements.

## `static(window)`
- **Purpose**: Displays the starting screen with buttons for starting the game, viewing team members, and checking game info.
- **UI Elements**:
  - **Background**: A static background image is displayed.
  - **Bird**: The bird image is centered on the screen.
  - **Base**: The base (ground) is drawn and moves horizontally.
  - **Buttons**:
    - **Start Game**: Starts the game when clicked.
    - **Team Members**: Displays team member information.
    - **Game Info**: Displays game information.

## `render(window, env, generation, reward=None)`
- **Purpose**: Renders the game environment during the game loop.
- **Draws**:
  - **Background**: Draws two instances of the background for continuous scrolling.
  - **Pipes**: Draws the pipes at their respective positions.
  - **Base**: Draws the base (ground).
  - **Bird**: Draws the bird.
  - **Score and Generation**: Displays the current score and generation count.
  - **Reward (Optional)**: Displays the current reward if provided.

## `show_team_members(window)`
- **Purpose**: Displays team member names in a popup window with a back button.
- **UI**:
  - Shows the names of the team members.
  - The back button allows users to return to the main screen.

## `show_game_info(window)`
- **Purpose**: Displays game-related information in a popup window with a back button.
- **UI**:
  - Provides information about the game, such as the Q-learning setup, how the agent learns, and how rewards impact performance.

---