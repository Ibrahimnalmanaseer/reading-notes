# Graphs - Data Structure

## Overview

Graphs in data structures are non-linear data structures made up of a finite number of nodes or vertices and the edges that connect them .
Graphs in data structures are used to address real-world problems in which it represents the problem area as a network like telephone networks, circuit networks, and social networks.

![image](https://user-images.githubusercontent.com/62019258/207685651-f14cd0d1-de6b-4538-bf61-5df8ea2606de.png)


## Types of Graphs in Data Structures![UndirectedGraph](https://user-images.githubusercontent.com/62019258/207690444-a56302b8-ba30-4057-89be-0e10cdcb6323.png)


### 1. Finite Graph
The graph G=(V, E) is called a finite graph if the number of vertices and edges in the graph is limited in number .

![ghraph](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/FINITE-GRAPH-IN-GRAPHS-IN-DATA-STRUCTURE.png)


### 2. Infinite Graph
The graph G=(V, E) is called a finite graph if the number of vertices and edges in the graph is interminable.

![infinite](https://www.simplilearn.com/ice9/free_resources_article_thumb/Graph%20Data%20Structure%20-%20Soni/infinite-graph-data-structure.png)

### 3. Trivial Graph

A graph G= (V, E) is trivial if it contains only a single vertex and no edges.

### 4. Simple Graph

If each pair of nodes or vertices in a graph G=(V, E) has only one edge, it is a simple graph. As a result, there is just one edge linking two vertices, depicting one-to-one interactions between two elements.

![image](https://user-images.githubusercontent.com/62019258/207686853-8601fc73-07c0-4821-a3c9-84a3dfae2421.png)



## Graph Representation

We represent graphs through:

- Adjacency Matrix
- Adjacency List



### Adjacency Matrix

An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix:

![UndirectedGraph](https://user-images.githubusercontent.com/62019258/207690518-fe986d2a-1117-41a1-8140-39fa96ab47cf.png)

Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.


![AdjMatrix](https://user-images.githubusercontent.com/62019258/207690284-3e495244-7eb9-4fbd-807a-43c54bb275a0.png)

### Adjacency List

An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

Adjacency lists make it easy to view if one vertices connects to another.

This is what an Adjacency List looks like:

![AdjList](https://user-images.githubusercontent.com/62019258/207691715-50d16dc8-8f50-4344-8098-20a3155455dc.png)


## Traversals


### Breadth First

Here is what the algorithm breadth first traversal looks like:

- Enqueue the declared start node into the Queue.
- Create a loop that will run while the node still has nodes present.
- Dequeue the first node from the queue
- if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.
Let’s look at a visual for a breadth first:

![BreadthFirst](https://user-images.githubusercontent.com/62019258/207692602-acee3f74-3723-4eb7-b7a6-b3c762225c5b.png)

```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    DECLARE visited <-- new Set()

    breadth.Enqueue(vertex)
    visited.Add(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                visited.Add(child)
                breadth.Enqueue(child)

    return nodes;

```


