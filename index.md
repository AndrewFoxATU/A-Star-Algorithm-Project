---
layout: none
---
<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@300;400;500&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap');

:root {
  --ink: #0f0e0d;
  --paper: #f7f4ef;
  --accent: #c94a2a;
  --accent-light: #f0e8e4;
  --muted: #7a7570;
  --rule: #ddd8d0;
  --code-bg: #1a1916;
  --code-fg: #e8e4dc;
  --green: #2d6a4f;
  --amber: #b45309;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--paper);
  color: var(--ink);
  font-size: 16px;
  line-height: 1.7;
  max-width: 860px;
  margin: 0 auto;
  padding: 3rem 2rem 6rem;
}

/* ── Header ─────────────────────────────────────── */
.report-header {
  border-top: 4px solid var(--ink);
  padding-top: 2.5rem;
  margin-bottom: 3.5rem;
  position: relative;
}

.report-header::after {
  content: '';
  display: block;
  height: 1px;
  background: var(--rule);
  margin-top: 2.5rem;
}

.label {
  font-family: 'DM Mono', monospace;
  font-size: 0.7rem;
  font-weight: 500;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 1rem;
  display: block;
}

h1 {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(2.4rem, 5vw, 3.6rem);
  line-height: 1.1;
  letter-spacing: -0.02em;
  color: var(--ink);
  margin-bottom: 1rem;
}

h1 em {
  font-style: italic;
  color: var(--accent);
}

.subtitle {
  font-size: 1.05rem;
  color: var(--muted);
  font-weight: 300;
  max-width: 560px;
  line-height: 1.6;
}

.meta-row {
  display: flex;
  gap: 2rem;
  margin-top: 1.5rem;
  flex-wrap: wrap;
}

.meta-item {
  font-family: 'DM Mono', monospace;
  font-size: 0.72rem;
  color: var(--muted);
  letter-spacing: 0.05em;
}

.meta-item strong {
  color: var(--ink);
  font-weight: 500;
}

/* ── Table of Contents ───────────────────────────── */
.toc {
  background: white;
  border: 1px solid var(--rule);
  border-left: 3px solid var(--accent);
  padding: 1.5rem 2rem;
  margin-bottom: 3rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.3rem 2rem;
}

.toc-title {
  font-family: 'DM Mono', monospace;
  font-size: 0.7rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--muted);
  margin-bottom: 0.8rem;
  grid-column: 1 / -1;
}

.toc a {
  font-size: 0.875rem;
  color: var(--ink);
  text-decoration: none;
  display: flex;
  align-items: baseline;
  gap: 0.4rem;
}

.toc a:hover { color: var(--accent); }

.toc-num {
  font-family: 'DM Mono', monospace;
  font-size: 0.65rem;
  color: var(--accent);
  flex-shrink: 0;
}

/* ── Sections ────────────────────────────────────── */
.section {
  margin-bottom: 3.5rem;
  padding-top: 0.5rem;
}

h2 {
  font-family: 'DM Serif Display', serif;
  font-size: 1.75rem;
  letter-spacing: -0.01em;
  color: var(--ink);
  margin-bottom: 1.25rem;
  display: flex;
  align-items: baseline;
  gap: 0.75rem;
}

h2 .section-num {
  font-family: 'DM Mono', monospace;
  font-size: 0.7rem;
  color: var(--accent);
  letter-spacing: 0.1em;
  font-weight: 500;
  flex-shrink: 0;
  margin-top: 0.15rem;
}

h3 {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.95rem;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--muted);
  margin: 1.75rem 0 0.75rem;
}

p {
  color: #2a2825;
  margin-bottom: 1rem;
}

hr.section-rule {
  border: none;
  border-top: 1px solid var(--rule);
  margin: 3rem 0;
}

/* ── Feature Grid ────────────────────────────────── */
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 1rem;
  margin: 1.25rem 0;
}

.feature-card {
  background: white;
  border: 1px solid var(--rule);
  padding: 1.1rem 1.25rem;
  position: relative;
}

.feature-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 2px;
  background: var(--accent);
  opacity: 0;
  transition: opacity 0.2s;
}

.feature-card:hover::before { opacity: 1; }

.feature-icon {
  font-size: 1.2rem;
  margin-bottom: 0.5rem;
  display: block;
}

.feature-label {
  font-size: 0.875rem;
  font-weight: 500;
  color: var(--ink);
}

.feature-desc {
  font-size: 0.8rem;
  color: var(--muted);
  margin-top: 0.2rem;
  line-height: 1.4;
}

/* ── Tables ──────────────────────────────────────── */
table {
  width: 100%;
  border-collapse: collapse;
  margin: 1.25rem 0;
  font-size: 0.9rem;
}

thead tr {
  border-bottom: 2px solid var(--ink);
}

th {
  font-family: 'DM Mono', monospace;
  font-size: 0.68rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--muted);
  padding: 0.6rem 0.75rem;
  text-align: left;
  font-weight: 500;
}

td {
  padding: 0.7rem 0.75rem;
  border-bottom: 1px solid var(--rule);
  vertical-align: top;
}

tr:last-child td { border-bottom: none; }

code {
  font-family: 'DM Mono', monospace;
  font-size: 0.82em;
  background: #ede9e3;
  padding: 0.1em 0.4em;
  border-radius: 2px;
  color: var(--accent);
}

/* ── Status Badges ───────────────────────────────── */
.badge {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  font-family: 'DM Mono', monospace;
  font-size: 0.68rem;
  letter-spacing: 0.05em;
  padding: 0.2rem 0.5rem;
  border-radius: 2px;
  font-weight: 500;
}

.badge-pending {
  background: #fef3cd;
  color: var(--amber);
  border: 1px solid #fde68a;
}

.badge-done {
  background: #d1fae5;
  color: var(--green);
  border: 1px solid #a7f3d0;
}

/* ── Callout Boxes ───────────────────────────────── */
.callout {
  padding: 1.25rem 1.5rem;
  margin: 1.5rem 0;
  border-left: 3px solid;
  background: white;
}

.callout-info {
  border-color: #3b82f6;
  background: #eff6ff;
}

.callout-warn {
  border-color: var(--amber);
  background: #fffbeb;
}

.callout p { margin: 0; font-size: 0.9rem; }

.callout-label {
  font-family: 'DM Mono', monospace;
  font-size: 0.65rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  font-weight: 500;
  margin-bottom: 0.4rem;
  display: block;
}

.callout-info .callout-label { color: #3b82f6; }
.callout-warn .callout-label { color: var(--amber); }

/* ── Timeline ────────────────────────────────────── */
.timeline {
  position: relative;
  margin: 1.25rem 0;
  padding-left: 1.5rem;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 0; top: 0; bottom: 0;
  width: 1px;
  background: var(--rule);
}

.timeline-item {
  position: relative;
  padding: 0.5rem 0 1rem 1.25rem;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: -4px; top: 0.85rem;
  width: 7px; height: 7px;
  border-radius: 50%;
  background: var(--rule);
  border: 2px solid var(--paper);
}

.timeline-item.active::before {
  background: var(--accent);
}

.timeline-week {
  font-family: 'DM Mono', monospace;
  font-size: 0.68rem;
  letter-spacing: 0.1em;
  color: var(--accent);
  text-transform: uppercase;
  margin-bottom: 0.2rem;
}

.timeline-desc {
  font-size: 0.9rem;
  color: var(--ink);
}

/* ── Grid Legend ─────────────────────────────────── */
.legend {
  display: flex;
  gap: 1.5rem;
  flex-wrap: wrap;
  margin: 1rem 0;
  padding: 1rem 1.25rem;
  background: var(--code-bg);
  border-radius: 3px;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-family: 'DM Mono', monospace;
  font-size: 0.8rem;
}

.legend-sym {
  font-size: 1rem;
  min-width: 1.5rem;
  text-align: center;
}

.legend-lbl { color: #8c8880; }
.sym-s { color: #4ade80; }
.sym-g { color: #facc15; }
.sym-obs { color: #f87171; }
.sym-empty { color: #4b5563; }

/* ── Limitations ─────────────────────────────────── */
.tag-list {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin: 0.75rem 0;
}

.tag {
  font-family: 'DM Mono', monospace;
  font-size: 0.72rem;
  padding: 0.25rem 0.6rem;
  border: 1px solid var(--rule);
  color: var(--muted);
  background: white;
}

.tag-future {
  border-color: var(--accent);
  color: var(--accent);
  background: var(--accent-light);
}

/* ── References ──────────────────────────────────── */
.ref-list {
  list-style: none;
  counter-reset: refs;
  margin: 1rem 0;
}

.ref-list li {
  counter-increment: refs;
  display: flex;
  align-items: baseline;
  gap: 0.75rem;
  padding: 0.6rem 0;
  border-bottom: 1px solid var(--rule);
  font-size: 0.9rem;
}

.ref-list li::before {
  content: counter(refs);
  font-family: 'DM Mono', monospace;
  font-size: 0.65rem;
  color: var(--accent);
  background: var(--accent-light);
  width: 1.4rem;
  height: 1.4rem;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.ref-list a {
  color: var(--ink);
  text-decoration: none;
  border-bottom: 1px solid var(--rule);
}

.ref-list a:hover { border-color: var(--accent); color: var(--accent); }

/* ── Footer ──────────────────────────────────────── */
.report-footer {
  margin-top: 5rem;
  padding-top: 1.5rem;
  border-top: 2px solid var(--ink);
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: gap;
}

.footer-brand {
  font-family: 'DM Serif Display', serif;
  font-size: 1rem;
  color: var(--ink);
}

.footer-note {
  font-family: 'DM Mono', monospace;
  font-size: 0.68rem;
  color: var(--muted);
  letter-spacing: 0.05em;
}

@media (max-width: 600px) {
  .toc { grid-template-columns: 1fr; }
  .feature-grid { grid-template-columns: 1fr 1fr; }
  .meta-row { gap: 1rem; }
}
</style>

<div class="report-header">
  <span class="label">Technical Report · C++14 · Pathfinding</span>
  <h1>A<em>*</em> Pathfinding<br>Algorithm</h1>
  <p class="subtitle">A grid-based shortest-path implementation using the A* search algorithm with Manhattan distance heuristic, written in modern C++14.</p>
  <div class="meta-row">
    <span class="meta-item"><strong>Language</strong> C++14</span>
    <span class="meta-item"><strong>Tool</strong> Visual Studio 2022</span>
    <span class="meta-item"><strong>VCS</strong> GitHub</span>
    <span class="meta-item"><strong>Status</strong> Week 3 — In Progress</span>
  </div>
</div>

<nav class="toc">
  <span class="toc-title">Contents</span>
  <a href="#overview"><span class="toc-num">01</span> Project Overview</a>
  <a href="#design"><span class="toc-num">02</span> Design Choices</a>
  <a href="#data-structures"><span class="toc-num">03</span> Data Structures</a>
  <a href="#heuristic"><span class="toc-num">04</span> Heuristic</a>
  <a href="#visualization"><span class="toc-num">05</span> Grid Visualization</a>
  <a href="#testing"><span class="toc-num">06</span> Testing & Validation</a>
  <a href="#limitations"><span class="toc-num">07</span> Limitations & Future Work</a>
  <a href="#timeline"><span class="toc-num">08</span> Project Timeline</a>
  <a href="#reflection"><span class="toc-num">09</span> Reflection</a>
  <a href="#references"><span class="toc-num">10</span> References</a>
</nav>

---

<div class="section" id="overview">

## <span class="section-num">01</span> Project Overview

This project implements the A\* pathfinding algorithm in modern C++14. The application finds the shortest path between two points on a grid while avoiding obstacles, producing a visual ASCII representation of the result.

<div class="feature-grid">
  <div class="feature-card">
    <span class="feature-icon">⊞</span>
    <div class="feature-label">Grid-based Pathfinding</div>
    <div class="feature-desc">Configurable grid dimensions with flexible start and goal placement</div>
  </div>
  <div class="feature-card">
    <span class="feature-icon">◼</span>
    <div class="feature-label">Obstacle Support</div>
    <div class="feature-desc">Arbitrary obstacle placement to test path routing around barriers</div>
  </div>
  <div class="feature-card">
    <span class="feature-icon">⌖</span>
    <div class="feature-label">Manhattan Heuristic</div>
    <div class="feature-desc">Admissible heuristic guaranteeing optimal shortest paths</div>
  </div>
  <div class="feature-card">
    <span class="feature-icon">⊡</span>
    <div class="feature-label">Visual Grid Output</div>
    <div class="feature-desc">ASCII-rendered grid showing path, obstacles, start, and goal</div>
  </div>
  <div class="feature-card">
    <span class="feature-icon">◈</span>
    <div class="feature-label">OOP Design</div>
    <div class="feature-desc">Modular, object-oriented class structure for clean separation of concerns</div>
  </div>
</div>

</div>

<hr class="section-rule" />

<div class="section" id="design">

## <span class="section-num">02</span> Design Choices

### Why A\*?

A\* was chosen because it combines the completeness of Dijkstra's algorithm with the speed of greedy best-first search. By using an admissible heuristic — one that never overestimates the true cost — A\* is guaranteed to find the optimal (shortest) path while exploring significantly fewer nodes than an exhaustive breadth-first search.

For a grid with no terrain weighting, the Manhattan distance heuristic is both admissible and consistent, making A\* the natural and efficient choice.

<div class="callout callout-info">
  <span class="callout-label">Algorithm Property</span>
  <p>A* is <strong>complete</strong> (always finds a path if one exists) and <strong>optimal</strong> (the path found is guaranteed to be shortest) when the heuristic is admissible.</p>
</div>

</div>

<hr class="section-rule" />

<div class="section" id="data-structures">

## <span class="section-num">03</span> Data Structures

| Structure | Purpose |
|-----------|---------|
| `gridParameters` | Stores grid configuration: dimensions, start position, goal position, and obstacle list |
| `Node` | Represents a single cell with position coordinates, cost values (`g`, `h`, `f`), and a pointer to its parent node |
| `AStarAlgorithm` | Encapsulates all pathfinding logic, including the open/closed list management and path reconstruction |

The `Node` struct tracks three cost values: **g** (actual cost from start), **h** (heuristic estimate to goal), and **f = g + h** (total estimated cost). Nodes in the open list are sorted by `f` to always expand the most promising candidate next.

</div>

<hr class="section-rule" />

<div class="section" id="heuristic">

## <span class="section-num">04</span> Heuristic: Manhattan Distance

For a grid with only horizontal and vertical movement (no diagonals), the Manhattan distance is the canonical admissible heuristic:

```
h(n) = |n.x − goal.x| + |n.y − goal.y|
```

This is **admissible** because no path through adjacent cells can ever be shorter than the Manhattan distance, ensuring A\* will not discard the optimal path. It is also **consistent** (monotone), meaning the estimated cost only ever improves as you move closer to the goal — avoiding redundant node re-expansion.

<div class="callout callout-warn">
  <span class="callout-label">Diagonal Note</span>
  <p>If diagonal movement is added in a future iteration, the heuristic must be updated to Euclidean or Chebyshev distance to preserve admissibility.</p>
</div>

</div>

<hr class="section-rule" />

<div class="section" id="visualization">

## <span class="section-num">05</span> Grid Visualization

The `printGrid()` function renders the grid state to the console after pathfinding completes.

<div class="legend">
  <div class="legend-item"><span class="legend-sym sym-s">S</span><span class="legend-lbl">Start position</span></div>
  <div class="legend-item"><span class="legend-sym sym-g">G</span><span class="legend-lbl">Goal position</span></div>
  <div class="legend-item"><span class="legend-sym sym-obs">#</span><span class="legend-lbl">Obstacle cell</span></div>
  <div class="legend-item"><span class="legend-sym sym-empty">.</span><span class="legend-lbl">Empty / traversable cell</span></div>
</div>

The reconstructed path is overlaid on the grid after a successful search, providing a quick visual confirmation that the algorithm has found a valid route. The visualizer linked in the header provides an interactive version of this output.

</div>

<hr class="section-rule" />

<div class="section" id="testing">

## <span class="section-num">06</span> Testing & Validation

Test cases cover both valid and degenerate inputs to ensure robust error handling across all edge conditions.

| Test Case | Description | Status |
|-----------|-------------|--------|
| Invalid grid dimensions | Grid width or height ≤ 0 | <span class="badge badge-pending">⬜ Pending</span> |
| Start out of bounds | Start position outside grid extents | <span class="badge badge-pending">⬜ Pending</span> |
| Goal out of bounds | Goal position outside grid extents | <span class="badge badge-pending">⬜ Pending</span> |
| Start on obstacle | Start cell is blocked | <span class="badge badge-pending">⬜ Pending</span> |
| Goal on obstacle | Goal cell is blocked | <span class="badge badge-pending">⬜ Pending</span> |
| No path exists | All routes to goal blocked by obstacles | <span class="badge badge-pending">⬜ Pending</span> |
| Start equals goal | Trivial case — zero-length path | <span class="badge badge-pending">⬜ Pending</span> |

</div>

<hr class="section-rule" />

<div class="section" id="limitations">

## <span class="section-num">07</span> Limitations & Future Improvements

### Current Limitations

<div class="tag-list">
  <span class="tag">Compile-time grid dimensions</span>
  <span class="tag">No diagonal movement</span>
  <span class="tag">No weighted terrain</span>
  <span class="tag">No random obstacle generation</span>
</div>

Grid dimensions are currently fixed as compile-time constants, which limits runtime flexibility. Movement is restricted to four cardinal directions, and all traversable cells share a uniform cost of 1.

### Planned Enhancements

<div class="tag-list">
  <span class="tag tag-future">Random obstacle generation</span>
  <span class="tag tag-future">Diagonal movement + Euclidean heuristic</span>
  <span class="tag tag-future">Weighted terrain (grass, mud, road)</span>
  <span class="tag tag-future">Path animation / step-through visualizer</span>
</div>

</div>

<hr class="section-rule" />

<div class="section" id="timeline">

## <span class="section-num">08</span> Development Timeline

<div class="timeline">
  <div class="timeline-item">
    <div class="timeline-week">Week 1</div>
    <div class="timeline-desc">Project setup, header file structure, initial class scaffolding</div>
  </div>
  <div class="timeline-item">
    <div class="timeline-week">Week 2</div>
    <div class="timeline-desc">Grid visualization implemented — <code>printGrid()</code> functional</div>
  </div>
  <div class="timeline-item active">
    <div class="timeline-week">Week 3 · Current</div>
    <div class="timeline-desc">Core A* algorithm implementation in progress</div>
  </div>
</div>

### Tools Used

| Tool | Purpose |
|------|---------|
| Visual Studio 2022 | Primary IDE and debugger |
| C++14 Standard | Language specification |
| GitHub | Version control and backup |

</div>

<hr class="section-rule" />

<div class="section" id="reflection">

## <span class="section-num">09</span> Reflection

### Challenges Encountered

*To be completed as the project progresses.*

### Key Learnings

*To be completed as the project progresses.*

### What I Would Do Differently

*To be completed as the project progresses.*

</div>

<hr class="section-rule" />

<div class="section" id="references">

## <span class="section-num">10</span> References

<ol class="ref-list">
  <li><a href="https://en.wikipedia.org/wiki/A*_search_algorithm">A* Search Algorithm — Wikipedia</a></li>
  <li><a href="https://en.wikipedia.org/wiki/Taxicab_geometry">Manhattan Distance (Taxicab Geometry) — Wikipedia</a></li>
  <li><a href="https://en.cppreference.com/w/cpp/utility/pair">std::pair — cppreference.com</a></li>
</ol>

</div>

<div class="report-footer">
  <span class="footer-brand">A* Pathfinding Report</span>
  <span class="footer-note">C++14 · Visual Studio 2022 · In Progress</span>
</div>
