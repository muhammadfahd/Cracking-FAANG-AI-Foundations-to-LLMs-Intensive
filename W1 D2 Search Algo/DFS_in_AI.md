#  Day 2 – Depth First Search (DFS) in Artificial Intelligence

##  Overview
On Day 2 of the **Advanced AI & Deep Learning Course**, we explored one of the most fundamental concepts in Artificial Intelligence — **Depth First Search (DFS)**.  
DFS is a **search algorithm** used for traversing or searching through data structures like trees and graphs. It forms the backbone of many AI applications that involve **problem-solving, pathfinding, and state-space exploration**.

---
**Table of Content** 
- [Day 2 – Depth First Search (DFS) in Artificial Intelligence](#day-2--depth-first-search-dfs-in-artificial-intelligence)
  - [Overview](#overview)
  - [What is Depth First Search (DFS)?](#what-is-depth-first-search-dfs)
    - [Key Characteristics:](#key-characteristics)
  - [How DFS Works](#how-dfs-works)
    - [Example (Pseudocode):](#example-pseudocode)
    - [Importance of DFS in Artificial Intelligence](#importance-of-dfs-in-artificial-intelligence)
    - [Real Life Example](#real-life-example)
    - [Reflection](#reflection)




##  What is Depth First Search (DFS)?
**Depth First Search (DFS)** is a graph traversal algorithm that explores as far as possible along each branch before backtracking.  
It uses the **LIFO (Last In, First Out)** principle, typically implemented with a **stack (or recursion)**.

### Key Characteristics:
- Explores depth before breadth  
- Can be implemented using recursion or an explicit stack  
- Does not guarantee the shortest path (unlike BFS)  
- Space-efficient for problems with deep but narrow search trees  

---

## How DFS Works
1. Start from the initial node (root).
2. Visit the node and mark it as visited.
3. Move to one of its unvisited child nodes.
4. Repeat the process until you reach a node with no unvisited children.
5. Backtrack and continue exploring other unvisited branches.

### Example (Pseudocode):
```python
def DFS(graph, start, visited=None):
    if visited is None:
        visited = set()
    visited.add(start)
    print(start)
    for neighbor in graph[start]:
        if neighbor not in visited:
            DFS(graph, neighbor, visited)
```

### Importance of DFS in Artificial Intelligence

DFS plays a crucial role in search-based problem-solving in AI.
It helps explore possible states in a structured way and is used in:

* Game trees (e.g., decision-making in chess or tic-tac-toe)
* Pathfinding algorithms
* Constraint satisfaction problems
* Solving puzzles like the 8-Queens or Maze traversal

DFS allows AI systems to search deeply into possible actions or states before making a final decision.

### Real Life Example

1. Route finding in maps: Exploring all possible paths before choosing one.
2. Web crawlers: DFS can be used to crawl web pages deeply before moving to another branch.
3. File system exploration: When you open folders within folders, your operating system uses a DFS-like approach.
4. AI planning problems: Robots exploring possible action sequences to achieve a goal.


### Reflection
Learning DFS helped me understand how AI systems explore and reason through search spaces.
It’s fascinating how such a simple recursive idea becomes the foundation for complex reasoning tasks — from robot navigation to strategic decision-making in games.

