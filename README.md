### Directed Graph Degree Balancer
This script analyzes a directed graph represented as an adjacency list, calculates the in-degrees and out-degrees of each node, and determines the minimum number of edges required to balance the graph.

### Usage

```
adjacency_list = {
    1: [2, 3, 5],
    2: [1, 4],
    3: [2, 5],
    4: [1, 2, 5],
    5: [3]
}
```
### The script calculates:

* Out-degrees: number of edges going out of a node.
* In-degrees: number of edges coming into a node.
* Then, it computes the minimum number of directed edges that must be added to make the graph balanced (i.e., each node has equal in-degree and out-degree).

### Example Output:
The minimum number of edges to add is: 4

### Requirements
This script is compatible with Python 3 and uses only built-in data structures (dict, set).
No external libraries are needed.

### Applications
This tool is useful in:
* Network flow analysis, to ensure input-output balance in systems such as logistics or data routing.
* Graph theory studies, to explore node degree balancing problems.
* Preprocessing directed graphs for algorithms that require balanced structures (e.g., Eulerian circuits).
* Educational purposes, for teaching concepts related to in-degrees, out-degrees, and graph balancing.

### License
This project is released under the MIT License. You may freely use, modify, and distribute this script.
