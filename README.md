## A* vs. Dijkstra: Algorithm Comparison

| Feature | Dijkstra's Algorithm | A* (A-Star) Algorithm |
| :--- | :--- | :--- |
| **Search Strategy** | **Uniform Cost (Blind):** Explores outwards from the start node based *only* on the actual cost ($g(n)$) already traveled. | **Heuristic-Guided (Informed):** Uses the actual cost ($g(n)$) *plus* an estimated cost ($h(n)$) to the goal. Prioritizes nodes that *seem* closer. |
| **Speed** | 🐢 **Generally Slower:** Explores in all directions, often visiting many nodes that are not on the optimal path to the specific target. | 🚀 **Generally Faster:** The heuristic guides the search *towards* the goal, significantly reducing the number of nodes explored, especially in large graphs. |
| **Optimality** | ✅ **Guaranteed:** Always finds the shortest path (assuming non-negative edge weights). | ✅ **Guaranteed (if heuristic is admissible):** Finds the shortest path, *provided* the heuristic never overestimates the true cost to the goal. |
| **Memory Usage** | **Often Higher:** Needs to store all nodes in its "visited" set and priority queue, which can grow large as it explores broadly. | **Often Lower:** By exploring fewer nodes, the priority queue (or "open set") tends to be smaller, often leading to less memory consumption in practice. |
