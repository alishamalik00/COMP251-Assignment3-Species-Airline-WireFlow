# COMP 251 – Assignment 3

This repository contains my solutions to **Assignment 3** of COMP 251.  
The assignment includes four algorithmic problems implemented in Java using the provided templates.  
The solutions focus on correctness and efficiency to pass both open and hidden test cases.

---

## Q1 – Species Protection

**Description:**  
You are given a grid where:  
- `.` → food that frogs eat  
- space `" "` → empty space  
- `X` → barriers  
- `A–W` → entrances where frogs start  

Frogs start from entrances on the border and can move in four directions, but cannot cross barriers.  
Your task is to:  
1. Calculate the minimum number of frogs needed to eat all reachable food.  
2. Count how many food spots remain unreachable.  

**Example:**  
XDRVX
X.X.X
XXXXX

Output:  2 0

Two frogs are required, and no food spots are inaccessible.

---

## Q2 – Airline Routing

**Description:**  
Given a list of direct flights (`itinerary`) and a list of target cities (`cities`), determine for each city if it is possible to travel indefinitely without being trapped in an airport.  
If a city is part of a reachable cycle, return `"succeed"`. Otherwise, return `"failed"`.

**Example:**  
Flights connecting `San_Antonio → Baltimore → New_York → Dallas → San_Antonio` mean each city in the loop is `"succeed"`.  
Cities leading to airports with no departures are `"failed"`.

---

## Q3 – Optimal Wire Length

**Description:**  
Given coordinates of `n` points in a 2D plane, find the minimum total wire length to connect all points using straight lines.  
The algorithm applies **Minimum Spanning Tree (MST)** techniques to minimize total length.

**Example:**  
Points: `(1,1)`, `(2,2)`, `(2,4)`  
- `(1,1) → (2,2)` = √2 ≈ 1.41  
- `(2,2) → (2,4)` = 2  
Total = `3.41`

---

## Q4 – Flow Network

**Description:**  
Implement the **Ford–Fulkerson** algorithm to compute the maximum flow from a given source to sink in a directed weighted graph.  

Includes:
- `pathDFS` – Finds augmenting paths using depth-first search.
- `fordfulkerson` – Augments flows until no paths remain.

**Example:**  
For two parallel paths with capacities 10 and 5, the max flow will be 15 once all augmenting paths are used.
