# A* Algorithm Visualizer

An interactive, browser-based visualizer for the **A\* (A-Star) pathfinding algorithm**, hosted on GitHub Pages.

## 🔗 Live Demo

[View the visualizer](https://andrewfoxatu.github.io/A-Star-Algorithm-Project/)

## 🧭 How to Use

1. **Click** a cell to place the **Start** node (red).
2. **Click** another cell to place the **End** node (orange).
3. **Click and drag** to draw **wall** cells that block the path.
4. Press **▶ Visualize** to run the A\* algorithm and watch it find the shortest path.
5. Use **Generate Maze** to auto-generate a random maze.
6. Use **Clear Grid** to reset the grid.
7. Toggle **Speed** to change the animation speed.

## 🔍 How A* Works

A\* is a best-first search algorithm that finds the shortest path between two nodes on a grid. It maintains two sets:

- **Open set** — candidate nodes to be explored next, prioritised by `f(n) = g(n) + h(n)`.
- **Closed set** — nodes already fully explored.

Where:
- `g(n)` = cost from the start node to node `n`.
- `h(n)` = heuristic estimate from `n` to the end (Manhattan distance in this visualizer).

At each step, the node with the lowest `f` score is expanded. Once the end node is reached, the path is reconstructed by following parent pointers back to the start.

## 🛠️ Tech Stack

- Plain HTML, CSS, and vanilla JavaScript — no dependencies.
- GitHub Actions for automated GitHub Pages deployment.