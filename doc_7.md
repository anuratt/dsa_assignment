Program Documentation: Dijkstra’s Algorithm (Shortest Path)

Program Name: Single Source Shortest Path using Dijkstra’s Algorithm
Language: C
Author: Anurat Niraula
Course: COMP202
Date: 15-Feb-2026

(a) Explanation of Data Structures

The program implements a weighted graph using an Adjacency Matrix and applies Dijkstra’s Algorithm to find the shortest path from a given source vertex.

Adjacency Matrix
int graph[V][V];


Represents a weighted graph

graph[i][j] stores the weight of the edge between vertex i and j

0 indicates no direct edge

The graph is assumed to have non-negative edge weights

Distance Array
int dist[V];


Stores the shortest distance from the source vertex to all other vertices

Initialized with a large value (INF) to represent infinity

Visited Array
int visited[V];


Keeps track of vertices whose shortest distance is already finalized

Prevents revisiting processed vertices

(b) Description of Functions
1. minDistance(int dist[], int visited[])

Purpose:
Finds the vertex with the minimum distance value from the set of unvisited vertices.

Working:

Iterates through all vertices

Selects the unvisited vertex with the smallest distance value

Returns the index of that vertex

2. printSolution(int dist[])

Purpose:
Displays the shortest distance from the source vertex to each vertex.

Working:

Prints vertex number and its corresponding shortest distance

Output is displayed in tabular format

3. dijkstra(int graph[V][V], int src)

Purpose:
Implements Dijkstra’s shortest path algorithm.

Working:

Initialize all distances as INF and visited as 0

Set distance of source vertex to 0

Repeat V-1 times:

Select the unvisited vertex with minimum distance

Mark it as visited

Update distances of adjacent vertices if a shorter path is found

Print final shortest distances using printSolution()

(c) Overview of main()

The main() function:

Defines a weighted graph using an adjacency matrix

Calls dijkstra() with source vertex 0

Displays the shortest distance from the source to all vertices

(d) Sample Input (Graph)

Adjacency Matrix Representation:

    0   1   2   3   4
0   0   4   1   0   0
1   4   0   2   5   0
2   1   2   0   8   0
3   0   5   8   0   3
4   0   0   0   3   0


Source Vertex: 0

(e) Sample Output
Vertex  Distance from Source
0       0
1       3
2       1
3       8
4       11

Conclusion

This program demonstrates:

Implementation of Dijkstra’s Algorithm

Representation of a weighted graph using an adjacency matrix

Computation of shortest paths from a single source

Use of greedy strategy to find optimal paths

Time Complexity

O(V²) (using adjacency matrix)

Space Complexity

O(V²) for adjacency matrix

O(V) for distance and visited arrays