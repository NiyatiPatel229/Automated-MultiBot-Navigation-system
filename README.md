# Automated Warehouse Bots Solution
(2nd RunnerUp in DoesHack'24)

## Problem Statement
This project solves the Warehouse Autobots Dilemma provided by Dosepacker Inc. In this challenge, autobots (robots) move products across a grid-based warehouse. The autobots face challenges such as traffic jams and collisions, slowing down operations. Our task is to design a system that ensures efficient, collision-free navigation of the autobots from their start points to their destinations while avoiding obstacles.

### Key Objectives:
* Guide multiple autobots across a grid from their start positions (A) to their destinations (B).
* Avoid collisions between autobots and obstacles.
* Ensure all autobots reach their goals without blocking each other.

### Key features of our solution:
* Collision Avoidance: No two bots can occupy the same space at the same time.
* Dynamic Movement: Each bot follows movement commands like Forward, Left, Right, and Wait to safely navigate the grid.
* Real-Time Coordination: Bots operate in parallel and avoid deadlocks.
For more details, please refer to the full problem statement document.

## Solution Overview
We used a Q-learning approach to enable intelligent, dynamic navigation for the autobots. The system is designed to minimize collisions and efficiently guide each bot to its destination.

## How to Run the Code
### Prerequisites
Ensure you have the following installed:
* Python 3.x
* Tkinter (Python's standard GUI package, included with Python)
* Numpy
You can install the required dependencies by running:

### bash
     pip install numpy

## Running the Code
1. Clone the repository or download the project files.
2. Navigate to the project directory.
3. Run the Python script:

### bash
     python your_script_name.py
   The Tkinter GUI window will open, allowing you to set up and simulate the warehouse grid with autobots.

## GUI Instructions:
### 1. Input Fields:
   * Enter the number of rows, columns, bots, and obstacles.
   * After entering the values, click on Set Grid.
### 2. Set Bot and Obstacle Positions:
   * After clicking Set Grid, the system will ask for the positions of each bot and its destination, as well as the positions of the obstacles.
   * Enter the positions as row-column pairs for both bots and obstacles.
### 3. Start Training:
   * Once all positions are set, click Start Training to initiate the Q-learning process.
   * Bots will learn and navigate the grid, avoiding obstacles and collisions.
### 4. Step through Simulation:
   * After training, click on Step to step through each bot’s movements and view their progress across the grid.
    
## Sample Grid Layout

### bash
      A . . X B
      . X . . .
      . . X . .
      . . . . .
      A X . . B

* A: Starting points for autobots
* B: Destination points for autobots
* X: Obstacles
* .: Free spaces where bots can move

  
### Main Script Components
* Bot Class: Represents each bot with its position, goal, and path.
* Environment Class: Manages the grid, updates bot positions, and prevents collisions.
* QLearningAgent Class: Implements Q-learning for dynamic decision-making.
* BotNavigationApp Class: Provides the GUI using Tkinter for setting up and simulating the grid.
  
## Dependencies
* Python 3.x
* Numpy (for handling matrix operations)
* Tkinter (for GUI interface)
  
## Commands and Movements
* Forward: Moves the bot one step forward.
* Left / Right: Rotates the bot 90 degrees.
* Wait: Pauses the bot for a step.
* Bots will avoid collisions by dynamically choosing their actions based on their learned policy from Q-learning.
  
## Notes:
* All autobots start facing upward.
* The Wait() command is used to avoid collisions and deadlocks.
* COOKIES_FINAL.ipynb is the final file which you can execute , rest other files were static approach and withoud GUI uploaded during project for reference.
  
## Future Enhancements
* Extend Q-learning with more advanced reinforcement learning techniques.
* Implement more complex obstacle configurations.
  
## License
This project is for educational purposes as part of the DoseHack'24 Hackathon.
