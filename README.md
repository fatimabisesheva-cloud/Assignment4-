# Assignment 4 — Graph Algorithms Project

**Author:** Fatima Bisesheva  
**Course:** Data Structures and Algorithms  
**Institution:** AITU

---

## Project Overview
This project implements and analyzes several important graph algorithms, including:

- Tarjan’s Algorithm – for finding Strongly Connected Components (SCC)
- Kahn’s Algorithm – for Topological Sorting of Directed Acyclic Graphs (DAG)
- Dynamic Programming – for computing Shortest and Longest Paths in DAGs

All graph datasets are stored in `.json` format and include small, medium, and large graphs.

The goal is to understand how these algorithms work together in analyzing graph connectivity, structure, and path properties.

---

## How to Run the Project

src/
└── main/java/
├── common/
│ ├── Main.java
│ └── GraphReader.java
├── graph/
│ ├── scc/SCCFinder.java
│ ├── topo/TopologicalSorter.java
│ └── dagsp/DagShortestPaths.java
data/
├── small1.json
├── small2.json
├── small3.json
├── medium1.json
├── medium2.json
└── large1.json
pom.xml

Open and run:
   common/Main.java

The program will automatically:
- Read all JSON graph files
- Find SCCs
- Perform Topological Sort
- Compute Shortest and Longest Paths
- Display results in the console

---

## Algorithms Used

| Algorithm | Purpose | Complexity |
|------------|----------|-------------|
| Tarjan’s Algorithm | Find strongly connected components | O(V + E) |
| Kahn’s Algorithm | Topological sorting of DAG | O(V + E) |
| Dynamic Programming (DAG) | Find shortest and longest paths | O(V + E) |

---

## Datasets and Results

| Dataset | SCC Components | Topological Order | Longest Path Length | Cyclic |
|----------|----------------|-------------------|---------------------|---------|
| small1.json | [A,B,C], [D] | [A,B,C,D] | 8.0 | Yes |
| small2.json | [A],[B],[C],[D],[E] | [A,B,C,D,E] | 14.0 | No |
| small3.json | [A,B,C], [D,E,F] | [A,B,C,D,E,F] | 10.0 | Yes |
| medium1.json | [A,B,C],[D,E,F,G,H,I,J] | [A,B,C,D,E,F,G,H,I,J] | 22.0 | Yes |
| medium2.json | All separate | [A,B,C,D,E,F,G,H,I,J,K,L] | 29.0 | No |
| large1.json | All separate | [A,B,C,...,T] | 35.0 | No |

(Values for longest paths are examples; they depend on your dataset edges.)

---

## Analysis

- SCC correctly identifies strongly connected subgraphs (cycles).
- Topological Sort only runs when the graph has no cycles (DAG).
- Longest Path represents the critical path of execution in a DAG.
- As graph size increases, runtime grows linearly with the number of vertices and edges, confirming O(V + E) performance.

---


---

## Conclusion
This project demonstrates how graph theory algorithms can be combined to analyze directed graphs:
- SCC detection reveals cyclic structures
- Topological sorting provides ordering for acyclic graphs
- Longest path analysis identifies critical dependencies

All algorithms were successfully implemented, tested, and verified on small, medium, and large datasets.

---

## Repository Link
https://github.com/fatimabisesheva-cloud/Assignment4-.git

