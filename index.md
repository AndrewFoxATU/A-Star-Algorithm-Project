---
layout: default
title: A* Pathfinding Algorithm
---

<style>
  /* ── Section headings ─────────────────────────────────── */
  h2 {
    border-left: 4px solid #e94560;
    padding-left: 12px;
    margin-top: 2rem;
    color: #0f3460;
  }

  h3 {
    color: #533483;
    margin-top: 1.4rem;
  }

  /* ── Visualizer CTA link ──────────────────────────────── */
  a[href="visualizer.html"] {
    display: inline-block;
    background: #0f3460;
    color: #fff !important;
    padding: 10px 22px;
    border-radius: 6px;
    font-weight: 700;
    font-size: 1rem;
    text-decoration: none;
    letter-spacing: 0.5px;
    transition: background 0.2s, transform 0.15s;
    margin: 0.5rem 0 1rem;
  }

  a[href="visualizer.html"]:hover {
    background: #e94560;
    transform: translateY(-2px);
  }

  /* ── Tables ───────────────────────────────────────────── */
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 1rem 0 1.5rem;
    font-size: 0.92rem;
  }

  thead th {
    background: #0f3460;
    color: #fff;
    padding: 10px 14px;
    text-align: left;
    border: 1px solid #0a2540;
  }

  tbody tr:nth-child(even) {
    background: #f0f4fb;
  }

  tbody tr:hover {
    background: #dde8f8;
  }

  tbody td {
    padding: 8px 14px;
    border: 1px solid #d0d9e8;
    vertical-align: middle;
  }

  /* ── Inline code & code blocks ────────────────────────── */
  code {
    background: #1a1a2e;
    color: #e94560;
    padding: 2px 6px;
    border-radius: 4px;
    font-size: 0.88em;
  }

  pre {
    background: #1a1a2e;
    color: #eee;
    padding: 14px 18px;
    border-radius: 6px;
    overflow-x: auto;
    line-height: 1.6;
  }

  pre code {
    background: none;
    color: inherit;
    padding: 0;
    font-size: 0.9em;
  }

  /* ── Feature / bullet lists ───────────────────────────── */
  ul {
    padding-left: 1.5rem;
    list-style: disc;
  }

  ol {
    padding-left: 1.5rem;
  }

  ul li, ol li {
    margin-bottom: 0.35rem;
    line-height: 1.7;
  }

  /* ── Horizontal rules ─────────────────────────────────── */
  hr {
    border: none;
    border-top: 2px solid #e2e8f0;
    margin: 2rem 0;
  }

</style>

<div style="background:#f0f4fb;border-left:4px solid #0f3460;border-radius:4px;padding:10px 16px;margin-bottom:1.5rem;font-size:0.95rem;">
  <strong>Author:</strong> Andrew Fox &nbsp;|&nbsp;
  <strong>Module:</strong> C++ Programming &nbsp;|&nbsp;
  <strong>Year:</strong> 2026
</div>

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

