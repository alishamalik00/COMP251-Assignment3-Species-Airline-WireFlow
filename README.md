COMP 251 — Assignment 3: Species Protection, Airline Routing, Wire Length, and Flow Network

This assignment covers a range of graph algorithms and optimization problems implemented in Java. It is divided into four main problems:

Q1: Determining frog accessibility and unreachable food in a habitat map.

Q2: Checking if travelers can avoid being trapped in an airport.

Q3: Finding the minimum wire length to connect points in a plane.

Q4: Computing maximum flow in a directed, weighted network using Ford–Fulkerson.

Q1 — Species Protection (BFS Traversal)

Description:
This problem simulates a frog population feeding on scattered food across a terrain map. The map contains:

"." — food for frogs.

" " — empty space.

"X" — barriers.

"A–W" — frog entrance points.

Using Breadth-First Search (BFS) starting from all frog entrances, the program must:

Count the number of frogs required to reach all accessible food dots.

Count the number of food dots that cannot be reached by any frog.

Example:
If frogs can reach two separate food areas but one food dot is blocked by barriers, the output might be:

2 1


meaning two frogs are needed, and one food dot is unreachable.

Q2 — Airline Routing (Cycle & Reachability Check)

Description:
Given a list of flight routes (itinerary) and a set of destination cities (cities), determine for each city whether it’s possible to keep traveling indefinitely without getting trapped in a final destination.
The solution uses graph reachability and cycle detection.

Example:
If a city has outgoing flights forming a cycle, output "succeed". If all paths lead to an airport with no departures, output "failed".

Q3 — Optimal Wire Length (Minimum Spanning Tree)

Description:
Given n points in a 2D plane, find the minimum length of wire required to connect all points. Only straight lines are allowed, so Euclidean distance is used. The problem is solved with a Minimum Spanning Tree (MST) algorithm.

Example:
For points (1,1), (2,2), (2,4), the minimal connections form a path length of:

sqrt(2) + 2 = 3.41

Q4 — Flow Network (Ford–Fulkerson Algorithm)

Description:
Implement the Ford–Fulkerson algorithm to compute the maximum possible flow from a source to a sink in a weighted, directed graph.
Two methods are completed:

pathDFS — Finds augmenting paths using DFS.

fordfulkerson — Iteratively augments flow until no more paths exist.

Example:
In a network with a source capacity of 15 and multiple paths to the sink, the algorithm returns the maximum achievable flow and updates residual capacities accordingly.
