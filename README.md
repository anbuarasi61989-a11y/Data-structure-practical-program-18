# Data-structure-practical-program-18# Adjacency List Graph Representation

class Graph:
    def __init__(self, V):
        self.V = V
        self.adj = [[] for i in range(V)]

    # Add edge
    def add_edge(self, u, v):
        self.adj[u].append(v)
        self.adj[v].append(u)   # remove this line if graph is directed

    # Display adjacency list
    def display(self):
        for i in range(self.V):
            print(i, "->", self.adj[i])


# Example
g = Graph(4)

g.add_edge(0, 1)
g.add_edge(0, 2)
g.add_edge(1, 2)
g.add_edge(2, 3)

g.display()
