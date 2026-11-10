# Dynamic Labyrinths: Asymmetric Hunter vs. Builder

A 3D asymmetric multiplayer game in Unity where the maze changes during play. It was built to teach and visualize search algorithms: a Builder reshapes the labyrinth while a Hunter (a player or an AI bot) has to keep finding a path.

> B.Sc. Software Engineering capstone project (Braude College), built with one partner.
> **My part:** most of the back end: the pathfinding algorithms, the server-client networking, the core game logic, and training the AI bots.

![Gameplay](docs/gameplay.gif)
<!-- Turn "POC ML & Alg.mov" into a short GIF and save it at docs/gameplay.gif -->

## Features
- **Asymmetric multiplayer:** Hunter and Builder have different goals and controls
- **A maze that changes in real time:** walls move during play, so paths must be recalculated on the fly
- **Algorithm visualizer:** shows how each search algorithm explores the grid
- **AI bots trained with reinforcement learning** to play the Hunter role
- **PC and phone:** builds for desktop and iOS, connected over the network

## Pathfinding algorithms (C#, written from scratch)
| Algorithm | Why it's here |
|---|---|
| A* | The baseline heuristic search |
| LPA* (Lifelong Planning A*) | Reuses earlier search results when the maze changes |
| D* Lite | Replans efficiently as the agent moves through a changing map |
| ARA* (Anytime Repairing A*) | Returns a quick path first, then improves it |

## Reinforcement learning
The Hunter bot is trained with the **Unity ML-Agents** toolkit using **PPO (Proximal Policy Optimization)** in Python. The training configuration is in `DynamicLab/Assets/Scenes/HunterBot.yaml`, and training run results are in `DynamicLab/results/`.

## Tech stack
| Area | Tools |
|---|---|
| Engine | Unity, C# |
| AI | Unity ML-Agents, Python, PPO |
| Platforms | Windows / macOS, iOS |

## Project structure
```
DynamicLab/
  Assets/        Game scripts: pathfinders, GameManager, LevelManager, map generator,
                 HunterAgent (ML agent), NetworkUI, AlgorithmVisualizer
  results/       ML-Agents training runs
docs/            Capstone presentations and project reports
```

## Run it
1. Open the `DynamicLab` folder in Unity Hub (Unity [version]).
2. Open the main scene and press Play.
3. To train the bot:
   ```bash
   pip install mlagents
   mlagents-learn DynamicLab/Assets/Scenes/HunterBot.yaml --run-id=HunterBot_Run_10
   ```
   Then press Play in Unity when it asks you to.
