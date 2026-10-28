# IAI_SLE_4
SLE-4: Final Viva & Architecture Decision Record (ADR)

Course: 02AML204 – Introduction to Artificial Intelligence
Class: SY B.Tech. CSE (AI & ML)
College: DKTE
PRN: 24UAM014
Name: Shrivardhan Chavan
Division: A
Date: 12 October 2026

1. Project Overview

This project implements a maze-solving agent that finds a path from a Start cell to a Goal cell in a grid maze while avoiding walls.

Two uninformed search algorithms are implemented and compared:

Breadth-First Search (BFS): Finds the shortest path in an unweighted maze.
Depth-First Search (DFS): Explores one branch deeply before backtracking.

Based on the performance evaluation conducted in SLE-2, DFS with an explicit stack and a visited set was selected as the primary maze-solving algorithm. BFS is retained as a baseline for comparison and profiling.

2. Objectives
Implement BFS and DFS for maze solving.
Compare the execution time and number of expanded nodes.
Profile algorithm performance using a flame graph.
Design the system using the C4 architecture model.
Document the algorithm selection through an Architecture Decision Record (ADR).
Understand the trade-off between execution speed and shortest-path optimality.
3. Algorithms Used
Breadth-First Search (BFS)

BFS explores the maze level by level using a queue.

Advantages:

Guarantees the shortest path in an unweighted maze.
Provides predictable path optimality.

Disadvantages:

Can explore many cells before reaching the goal.
May require more memory to store the queue and discovered cells.
Depth-First Search (DFS)

DFS explores one branch as deeply as possible before backtracking. This implementation uses an explicit stack, a visited set, and a parent map.

Advantages:

Faster than BFS on the larger test mazes used in this project.
Expanded fewer nodes in the 70×70 test case.
Avoids recursion-depth problems by using an explicit stack.

Disadvantages:

Does not guarantee the shortest path.
Performance depends on the order in which neighbours are explored.
4. Performance Evaluation

BFS and DFS were tested on three maze sizes.

| Maze Size | BFS Average Time | DFS Average
