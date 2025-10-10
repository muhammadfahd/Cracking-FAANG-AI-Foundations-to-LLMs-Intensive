# Week 1 – Day 3: Search Algorithms in AI
(BFS, DFS, A*, Rule-Based Systems)

## Overview
On **Day 3** of the **AI Foundations Course**, I learned about several fundamental **search algorithms** — **BFS**, **DFS (revision)**, **A\***, and **Rule-Based AI Systems**.  
These algorithms are crucial for **problem-solving, pathfinding, and reasoning**, forming the **backbone of AI decision-making**.

---

- [Week 1 – Day 3: Search Algorithms in AI](#week-1--day-3-search-algorithms-in-ai)
  - [Overview](#overview)
  - [🔍 What is Search in AI?](#-what-is-search-in-ai)
    - [🧩 Example](#-example)
  - [🧠 Why Search Algorithms Matter in AI](#-why-search-algorithms-matter-in-ai)
  - [⚙️ Types of Search Strategies](#️-types-of-search-strategies)
    - [1️. Uninformed (Blind) Search](#1️-uninformed-blind-search)
      - [**Depth First Search (DFS)** – Revision](#depth-first-search-dfs--revision)
      - [**Breadth First Search (BFS)**](#breadth-first-search-bfs)
        - [🧩 BFS Example](#-bfs-example)
        - [Real-Life Examples of BFS](#real-life-examples-of-bfs)
    - [2. Informed (Heuristic) Search](#2-informed-heuristic-search)
      - [A\* (A-Star) Search Algorithm](#a-a-star-search-algorithm)
        - [Importance of A\*](#importance-of-a)
        - [Real-Life Examples of A\*](#real-life-examples-of-a)
    - [3. Rule-Based AI Systems](#3-rule-based-ai-systems)
      - [**How They Work**](#how-they-work)
  - [Why These Algorithms Are Necessary](#why-these-algorithms-are-necessary)




## 🔍 What is Search in AI?
Search in AI is a **systematic process** used by an intelligent agent to **explore possible states** and **find a path to a goal**.  
In simpler terms — it’s how AI systems **think, plan, and decide what to do next**.

### 🧩 Example
Imagine a **robot in a maze**:
- **Start State** → Robot’s initial position  
- **Actions / Paths** → Possible moves it can take  
- **Goal State** → The maze’s exit  

The AI uses **search algorithms** to find a **valid and efficient path** from start to goal.

---

## 🧠 Why Search Algorithms Matter in AI
Search algorithms are the **foundation of intelligent behavior**.  
They are essential because they:
- Enable **decision-making** and **goal achievement**.  
- Help AI systems **plan actions** and **navigate environments**.  
- Form the **basis for pathfinding**, **game strategies**, and **robot motion planning**.  
- Bridge the gap between **problem definition** and **solution generation**.  

---

## ⚙️ Types of Search Strategies

### 1️. Uninformed (Blind) Search
Uninformed searches **do not have any additional information** about the goal — they explore blindly.

#### **Depth First Search (DFS)** – Revision
- Explores **deep** paths first before backtracking.  
- Uses a **stack (LIFO)** or recursion.  
- **May not find the shortest path**, but requires **less memory**.  
- Ideal for **deep and narrow** problems.

#### **Breadth First Search (BFS)**
- Explores nodes **level by level**, starting from the root.  
- Uses a **queue (FIFO)** data structure.  
- **Guaranteed to find the shortest path**, but **requires more memory**.  
- Works best for **shallow and wide** search spaces.

##### 🧩 BFS Example
```python
from collections import deque

def BFS(graph, start):
    visited = set()
    queue = deque([start])

    while queue:
        node = queue.popleft()
        if node not in visited:
            print(node)
            visited.add(node)
            queue.extend(graph[node])
```
##### Real-Life Examples of BFS

* Shortest route finding (like in Google Maps or GPS systems)
* Social networks (finding the shortest connection between two users)
* Web crawling (exploring all links level-wise)


### 2. Informed (Heuristic) Search
Informed searches use additional knowledge or heuristics to estimate which path leads faster to the goal.

#### A* (A-Star) Search Algorithm

A* combines:
Actual cost so far (g(n))
Estimated cost to goal (h(n))

Formula:
f(n) = g(n) + h(n)

Where:
g(n) = cost from start to current node
h(n) = estimated cost to goal
f(n) = total estimated cost

A* chooses the path with the lowest f(n) value.


##### Importance of A*
* Balances speed (like greedy algorithms) and accuracy (like uniform cost search).
* Ensures the shortest and optimal path if the heuristic is admissible.

##### Real-Life Examples of A*
* Google Maps Navigation → Combines real distance (g) and traffic/estimated time (h) to find the best route.
* Robotics Path Planning → Robots use A* to navigate obstacles efficiently.
* Game AI Movement → NPCs use A* to find optimal paths in game environments.

### 3. Rule-Based AI Systems

Rule-based systems use “IF-THEN” rules for decision-making and reasoning.
They form one of the earliest forms of symbolic AI and are still widely used.

#### **How They Work**

The system has a knowledge base (rules + facts).
An inference engine applies the rules to infer new information or make decisions.

## Why These Algorithms Are Necessary

These concepts form the core reasoning framework of AI:
🔹 **BFS & DFS** → Teach structured exploration.
🔹 **A*** → Adds intelligence with heuristics and optimization.
🔹 **Rule-Based Systems** → Introduce reasoning, logic, and explainability.

Together, they build the foundation for intelligent agents, decision systems, and autonomous machines.