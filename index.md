---
layout: default
title: A* Pathfinding Algorithm
---

# A* Pathfinding Algorithm
**Author:** Andrew Fox  
**Module:** C++ Programming  
**Year:** 2026

---

## Project Overview

[▶ Open the Interactive A\* Visualizer](visualizer.html)

This project implements the A* pathfinding algorithm in modern C++ (C++14). The application finds the shortest path between two points on a grid while avoiding obstacles.

### Features
- Grid-based pathfinding with configurable dimensions
- Obstacle placement support
- Manhattan distance heuristic
- Visual grid output
- Modular, object-oriented design

---

## Design Choices

### Why A* Algorithm?


### Data Structures

| Structure | Purpose |
|-----------|---------|
| `gridParameters` | Stores grid configuration (size, start, goal, obstacles) |
| `Node` | Represents a cell with position, costs (g, h, f), and parent pointer |
| `AStarAlgorithm` | Encapsulates pathfinding logic |

### Heuristic: Manhattan Distance


### Grid Visualization
The `printGrid()` function renders the grid with:
- `S` = Start position
- `G` = Goal position  
- `#` = Obstacles
- `.` = Empty cells


---

## Testing & Validation

### Test Cases (Planned)
<!-- Update this section as you implement tests -->

| Test | Description | Status |
|------|-------------|--------|
| Invalid grid dimensions | Grid width/height ≤ 0 | ⬜ Pending |
| Start out of bounds | Start position outside grid | ⬜ Pending |
| Goal out of bounds | Goal position outside grid | ⬜ Pending |
| Start on obstacle | Start placed on obstacle cell | ⬜ Pending |
| Goal on obstacle | Goal placed on obstacle cell | ⬜ Pending |
| No path exists | Obstacles block all routes | ⬜ Pending |
| Start equals goal | Trivial case | ⬜ Pending |

---

## Limitations & Future Improvements

### Current Limitations
- Grid dimensions are compile-time constants
- No diagonal movement support
- No weighted terrain support

### Future Enhancements
- Random obstacle generation (`randomObstaclesEnabled`)
- Diagonal movement with Euclidean heuristic
- Different terrain costs (e.g., grass vs mud)
- Path animation/visualization

---

## Project Management

### Development Timeline
<!-- Update with your actual progress -->

| Week | Tasks Completed |
|------|-----------------|
| 1 | Project setup, header file structure |
| 2 | Grid visualization (`printGrid`) |
| 3 | *In progress...* |

### Tools Used
- Visual Studio 2022
- C++14 Standard
- GitHub for version control

---

## Reflection

### Challenges Encountered
<!-- Add your reflections as you progress -->
- *To be completed...*

### Key Learnings
- *To be completed...*

### What I Would Do Differently
- *To be completed...*

---

## References

1. [A* Search Algorithm - Wikipedia](https://en.wikipedia.org/wiki/A*_search_algorithm)
2. [Manhattan Distance - Wikipedia](https://en.wikipedia.org/wiki/Taxicab_geometry)
3. [std::pair - cppreference](https://en.cppreference.com/w/cpp/utility/pair)

