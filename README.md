Graph Degree Balancer
Graph Degree Balancer is a tool to calculate and balance the in-degrees and out-degrees of a directed graph. This process is useful to ensure that all nodes have the same number of incoming and outgoing edges, which is important in problems like path reconstruction in De Bruijn graphs or in load-balancing algorithms.

Functionality
Calculates the in-degree and out-degree of each node.

Determines the minimum number of edges that need to be added to the graph to balance the in-degrees and out-degrees of all nodes.

Graph Structure
The input graph is represented as a Python dictionary, where each node is a key and its neighbors (outgoing nodes) are stored in a list as the value.

Example graph: 

adjacency_list = {
    1: [2, 3, 5],
    2: [1, 4],
    3: [2, 5],
    4: [1, 2, 5],
    5: [3]
}

Installation
You can use the code directly or import the functions into your own project. There are no external dependencies required.

How to Use
Define the graph as a dictionary, where each key is a node and each value is a list of neighbors.

The algorithm will compute the in-degrees and out-degrees and determine the minimum number of edges required to balance the degrees.

Example Usage

# Example graph
adjacency_list = {
    1: [2, 3, 5],
    2: [1, 4],
    3: [2, 5],
    4: [1, 2, 5],
    5: [3]
}

# Initialize degree dictionaries
in_degrees = {}
out_degrees = {}

# Calculate in-degrees and out-degrees
for node, neighbors in adjacency_list.items():
    out_degrees[node] = len(neighbors)
    for neighbor in neighbors:
        in_degrees[neighbor] = in_degrees.get(neighbor, 0) + 1

# Calculate the minimum number of edges to add
min_edges_to_add = sum(abs(in_degrees.get(node, 0) - out_degrees.get(node, 0)) for node in set(in_degrees) | set(out_degrees))

print(f"The minimum number of edges to add is: {min_edges_to_add}")

Expected Output
This code will calculate the minimum number of edges that need to be added to balance the in-degrees and out-degrees of the graph.

Contribution
If you would like to contribute to this project, feel free to fork the repository and submit pull requests with improvements or fixes.

License
This project is licensed under the MIT License.

