# `algorithm.py` - Q-learning Agent

This file defines the `QLAgent` class that implements a Q-learning agent for training in the Flappy Bird environment.

## `QLAgent` Class

### `__init__(self, learning_rate=0.1, decay_factor=0.9, gamma=0.95)`
- **Purpose**: Initializes the Q-learning agent.
- **Parameters**:
  - `learning_rate`: The rate at which the agent updates its Q-values (default is 0.1).
  - `decay_factor`: Factor by which the agent's Q-value is updated (default is 0.9).
  - `gamma`: Discount factor for future rewards (default is 0.95).

### `choose_action(self, x, y)`
- **Purpose**: Chooses the next action based on the current state `(x, y)` of the environment.
- **Returns**: 
  - `0`: Action to do nothing.
  - `1`: Action to jump.

### `update(self, x_prev, y_prev, action, reward, x_next, y_next)`
- **Purpose**: Updates the Q-table based on the agent's actions and the received reward.
- **Parameters**:
  - `x_prev, y_prev`: The previous state of the environment.
  - `action`: The action taken by the agent.
  - `reward`: The reward received for taking the action.
  - `x_next, y_next`: The new state after taking the action.
- **Functionality**: The Q-value for the previous state-action pair is updated using the Q-learning update formula.

---

