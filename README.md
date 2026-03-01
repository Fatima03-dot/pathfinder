Gemini said
This is a comprehensive README.md file tailored for your GitHub repository. You can copy and paste this content directly into your project's README file.

AI Pathfinding Visualizer
This project is an interactive Python application built with Pygame that allows users to visualize and compare two common search algorithms: A Search* and Greedy Best-First Search (GBFS). Users can interact with a grid to set start/goal nodes, generate random mazes, toggle dynamic obstacles, and observe how these algorithms navigate a grid world in real-time.

Features
Interactive Grid: Click to place walls, start, and goal positions.

Dual Algorithm Support: Compare the efficiency of A* and GBFS.

Heuristic Options: Switch between Manhattan and Euclidean distance heuristics.

Dynamic Environments: Toggle "Dynamic Mode" to introduce new obstacles randomly while the search is in progress.

Performance Metrics: Real-time feedback on Nodes Visited, Path Cost, and Execution Time.

Maze Generation: Automatically generate complex obstacle layouts with customizable density.

Prerequisites
You need Python installed on your machine. This project relies on the pygame library.

Install dependencies using pip:

Bash
pip install pygame
How to Run
Clone this repository.

Run the script:

Bash
python main.py
Use the Control Panel on the right side to select algorithms, heuristics, and interact with the grid.

Implementation Logic
The visualizer processes pathfinding using a Priority Queue mechanism, which ensures that the algorithm always expands the most promising node next.

*A Search:** This algorithm finds the shortest path by utilizing the function f(n)=g(n)+h(n).

g(n) represents the exact cost from the start node to current node n.

h(n) is the heuristic estimation to the goal.

The implementation constantly updates node scores if a cheaper path is discovered, ensuring the path found is optimal.

Greedy Best-First Search (GBFS): This algorithm simplifies the priority to f(n)=h(n).

It ignores the actual cost traveled (g(n)) and prioritizes nodes based solely on physical closeness to the goal.

This makes the search much faster and "greedy" but often fails to find the most efficient path.

Maze & Dynamic Generation: The maze generator fills the grid using a probability density check. The dynamic mode injects randomness during the search loop, creating an unstable environment that tests the algorithm's ability to adapt.


License
This project is open-source. Feel free to modify, expand, or use this for educational purposes.
