# Dijkstra Algorithm Implementation

This is a Python implementation of Dijkstra's algorithm for finding the shortest path in a graph.

## How to use

The `dijkstra` function takes in a graph and a starting node, and returns the shortest path to all nodes from the starting node. The graph should be a dictionary where each key is a node, and the value is a dictionary containing the edges from that node and the distance to each connected node.

```python
graph = {
    'A': {'B': 5, 'C': 1},
    'B': {'A': 5, 'C': 2, 'D': 1},
    'C': {'A': 1, 'B': 2, 'D': 4, 'E': 8},
    'D': {'B': 1, 'C': 4, 'E': 3, 'F': 6},
    'E': {'C': 8, 'D': 3},
    'F': {'D': 6}
}

shortest_paths = dijkstra(graph, 'A')

print(shortest_paths)
```

Output:
```
{
    'A': {'cost': 0, 'path': ['A']},
    'B': {'cost': 5, 'path': ['A', 'B']},
    'C': {'cost': 1, 'path': ['A', 'C']},
    'D': {'cost': 6, 'path': ['A', 'B', 'D']},
    'E': {'cost': 9, 'path': ['A', 'C', 'E']},
    'F': {'cost': 12, 'path': ['A', 'B', 'D', 'F']}
}
```

## Requirements

This implementation requires Python 3.x.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
