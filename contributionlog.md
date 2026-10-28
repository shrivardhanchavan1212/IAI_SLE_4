AI Contribution Log
SLE-4: Final Viva & Architecture Decision Record (ADR)
Student Details
Name: Shrivardhan Chavan
PRN: 24UAM014
Division: A
Course: 02AML204 – Introduction to Artificial Intelligence
Class: SY B.Tech. CSE (AI & ML)
College: DKTE
Date: 12 October 2026
1. Purpose of This Log

This document records how AI tools were used during the development, testing, performance analysis, architecture design, and documentation of the maze-solving project across SLE-1, SLE-2, SLE-3, and SLE-4.

The purpose is to maintain transparency about AI assistance and distinguish suggested ideas from implementation, testing, analysis, and final decisions.

2. AI Tool Usage

AI tool used: ChatGPT

AI assistance was used for understanding concepts, organizing documentation, explaining algorithmic trade-offs, and preparing the Architecture Decision Record (ADR).

3. Contribution Log by SLE
SLE-1: Maze Solver Implementation

Objective: Implement BFS and DFS algorithms to find a path from the Start cell to the Goal cell in a grid maze.

AI assistance:

Helped explain the working principles of BFS and DFS.
Assisted in understanding stacks, queues, visited sets, and parent maps.
Helped organize project documentation and the README structure.
Supported the explanation of algorithmic complexity and path reconstruction.

Student contribution:

Worked on the maze-solving implementation.
Reviewed the algorithms and their behaviour.
Examined the generated paths and project output.
Organized the source code and project documentation.
SLE-2: Performance Profiling and Comparison

Objective: Compare BFS and DFS across three maze sizes and analyze their performance using a flame graph.

AI assistance:

Helped interpret execution-time comparisons.
Explained how flame graphs represent time spent in functions.
Assisted in organizing benchmark results into tables.
Helped explain why BFS may expand more nodes than DFS on particular maze layouts.

Student contribution:

Conducted or reviewed the reported benchmark runs.
Compared the measured execution times for 20×20, 40×40, and 70×70 mazes.
Examined the flame graph and recorded the reported performance results.
Used the findings to evaluate the trade-offs between BFS and DFS.

Reported benchmark results:

Maze Size	BFS	DFS
20×20	0.05 ms	0.26 ms
40×40	0.81 ms	0.66 ms
70×70	4.75 ms	0.61 ms

These figures are the reported project measurements and should be verified against the original benchmark output.

SLE-3: C4 Architecture Design

Objective: Document the system architecture using C4 Context, Container, Component, and Code diagrams.

AI assistance:

Helped explain the purpose of the C4 architecture model.
Assisted in describing the responsibilities of the Input, Search, and Output components.
Helped explain modular design and the use of a common solver interface.
Supported the organization of architecture documentation.

Student contribution:

Prepared or reviewed the C4 architecture diagrams.
Identified the responsibilities of the main system components.
Documented how BFS and DFS can be selected through the Search component.
Reviewed the relationship between architecture and algorithm profiling.
SLE-4: Final Viva and Architecture Decision Record

Objective: Document and justify the selection of DFS as the primary maze solver.

AI assistance:

Helped structure the ADR into context, decision, alternatives, rationale, and consequences.
Assisted in explaining the performance and memory trade-offs between BFS and DFS.
Helped organize the final README and project summary.
Supported the preparation of clear technical explanations for the viva.

Student contribution:

Reviewed the benchmark results and profiling evidence.
Selected DFS as the default solver based on the reported results.
Retained BFS as a comparison baseline because it guarantees a shortest path in an unweighted maze.
Documented the limitations and conditions under which BFS or A* might be preferred.
4. Architecture Decision Summary

The final architecture decision was to use Depth-First Search (DFS) with an explicit stack, visited set, and parent map as the default solver, while retaining BFS behind the same solve(maze, start, goal) interface.

The decision was based on the reported benchmark results, particularly the 70×70 maze, where DFS took 0.61 ms compared with 4.75 ms for BFS.

The trade-off is that DFS does not guarantee the shortest path. BFS remains available when shortest-path optimality is required.

5. Verification and Responsibility
AI-generated explanations and documentation were reviewed for relevance to
