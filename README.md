Dynamic Labyrinths 
 is an interactive 3D asymmetric multiplayer game built with Unity. Developed as a Bachelor of Science in Software Engineering capstone project, this game combines dynamic environment generation with advanced artificial intelligence and pathfinding algorithms.

 Key Features

* Asymmetric Multiplayer: Unique gameplay mechanics where players have different roles and objectives within the maze.
* Dynamic Environments: The labyrinth changes dynamically during gameplay, forcing both players and AI to adapt in real-time.
* Advanced Pathfinding: Custom implementations of multiple heuristic search algorithms to navigate the changing maze efficiently.
* Smart AI Agents: Bots trained using Reinforcement Learning to navigate and react to the dynamic obstacles and player movements.
* 
 Tech Stack

* Game Engine:Unity (C#)
* Machine Learning: Python, Unity ML-Agents Toolkit
* Algorithms: Reinforcement Learning, Proximal Policy Optimization (PPO)

 AI & Pathfinding Algorithms
A core focus of this project is the integration of sophisticated algorithms to handle real-time path recalculation in a dynamic grid. 

 Search Algorithms Implemented (C#)
* A* (A-Star): The baseline heuristic search algorithm.
* LPA* (Lifelong Planning A*): Optimized for dynamic environments, reusing previous search trees when the maze changes.
* Theta*: Used for any-angle path planning, creating smoother and more realistic movement.
* Jump Point Search (JPS): Highly optimized pathfinding for uniform grids.

 Reinforcement Learning (Python)
The game features autonomous bots trained to adapt to the asymmetric gameplay. The training environment was set up using Unity ML-Agents, and the models were trained utilizing Proximal Policy Optimization (PPO) in Python, allowing the bots to learn optimal strategies through continuous interaction with the dynamic maze.

 About the Project
This project was developed as a capstone project for a B.Sc. in Software Engineering. It demonstrates practical applications of graph theory, machine learning, and game development principles in a single, cohesive application.
