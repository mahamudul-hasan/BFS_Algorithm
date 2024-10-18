# Graph Algorithms in Java: BFS and Floyd-Warshall

This project contains Java implementations of two fundamental graph algorithms:

Breadth-First Search (BFS)
Floyd-Warshall Algorithm

## Table of Contents

- [Introduction](#introduction)
- [Algorithms](#algorithms)
  - [Breadth-First Search (BFS)](#breadth-first-search-bfs)
  - [Floyd-Warshall Algorithm](#floyd-warshall-algorithm)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This repository contains two essential graph algorithms implemented in Java:

- **BFS** for graph traversal.
- **Floyd-Warshall** for finding the shortest paths between all pairs of nodes in a weighted graph.

Both algorithms are foundational for solving graph-related problems in computer science.

## Algorithms

### Breadth-First Search (BFS)

**Breadth-First Search (BFS)** is an algorithm for traversing or searching tree or graph data structures. It starts at the root (or an arbitrary node) and explores all nodes at the present "depth" before moving on to nodes at the next level.

- **Use cases**:
  - Shortest path in unweighted graphs.
  - Connectivity checking.

#### Time Complexity
- **O(V + E)** where `V` is the number of vertices and `E` is the number of edges.

### Floyd-Warshall Algorithm

The **Floyd-Warshall** algorithm is a dynamic programming approach used for finding shortest paths in a weighted graph between all pairs of vertices.

- **Use cases**:
  - All-pairs shortest path calculation.
  - Handling negative weights (but not negative cycles).

#### Time Complexity
- **O(V^3)** where `V` is the number of vertices.

## Installation

To run the project locally, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/mahamudul-hasan/BFS_Algorithm.git
   cd BFS_Algorithm
   ```

2. **Set up the Java environment**:

   Make sure you have Java installed. You can check by running:

   ```bash
   java -version
   ```

3. **Compile the Java files**:

   Compile the Java files using the `javac` command.

   ```bash
   javac src/*.java
   ```

## Usage

To run the implementations, use the following commands.

### Running BFS:

```bash
java -cp src BFS
```

### Running Floyd-Warshall:

```bash
java -cp src FloydWarshall
```

## Examples

### Example 1: Running BFS on a sample graph
After compiling the project, run the BFS algorithm as follows:

```bash
java -cp src BFS
```

Sample input:
```
Enter the number of nodes: 5
Enter the adjacency list for each node:
1 -> 2 3
2 -> 4
3 -> 4 5
4 -> 
5 -> 
Enter the starting node: 1
```

Sample output:
```
BFS traversal starting from node 1: 1 -> 2 -> 3 -> 4 -> 5
```

### Example 2: Running Floyd-Warshall on a weighted graph
To run the Floyd-Warshall algorithm:

```bash
java -cp src FloydWarshall
```

Sample input:
```
Enter the number of vertices: 4
Enter the adjacency matrix (use a large number for infinity):
0 3 INF INF
2 0 INF 1
INF 7 0 2
INF INF 3 0
```

Sample output:
```
Shortest distances between every pair of vertices:
[0, 3, 5, 6]
[2, 0, 7, 1]
[9, 7, 0, 2]
[12, 10, 3, 0]
```

## Contributing

Contributions are welcome! To contribute to this repository:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/my-feature`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/my-feature`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
