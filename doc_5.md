Program Documentation: Graph Traversal Using BFS and DFS

Program Name: Undirected Graph Traversal using Adjacency Matrix
Language: C
Author: Anurat Niraula
Course: COMP202
Date: 15-Feb-2026

(a) Explanation of Data Structures

The program implements an undirected graph using an Adjacency Matrix.

Adjacency Matrix
int adj[MAX][MAX];


A 2D array of size n × n

adj[i][j] = 1 → Edge exists between vertex i and j

adj[i][j] = 0 → No edge

Since the graph is undirected, the matrix is symmetric
(adj[i][j] = adj[j][i])

Visited Array
int visited[MAX];


Keeps track of visited vertices during traversal

Prevents revisiting the same vertex

Queue (for BFS)
int queue[MAX];


Used to store vertices in Breadth First Search

Implements FIFO (First In First Out) behavior

(b) Description of Functions
1. DFS(int v)

Purpose:
Traverses the graph using the Depth First Search (DFS) technique.

Working:

Prints the current vertex

Marks it as visited

Recursively visits all unvisited adjacent vertices

Technique Used: Recursion (implicit stack)

2. BFS(int start)

Purpose:
Traverses the graph using the Breadth First Search (BFS) technique.

Working:

Initializes the visited array

Inserts the starting vertex into the queue

Repeatedly:

Removes a vertex from the queue

Visits all unvisited adjacent vertices

Adds them to the queue

Technique Used: Queue (explicit)

(c) Overview of main()

The main() function performs the following tasks:

Accepts the number of vertices

Takes input for the adjacency matrix

Accepts the starting vertex

Initializes the visited array

Calls the DFS() function to perform depth-first traversal

Calls the BFS() function to perform breadth-first traversal

Displays the traversal order for both techniques

(d) Sample Input
Enter number of vertices: 4

Enter adjacency matrix:
0 1 1 0
1 0 1 1
1 1 0 0
0 1 0 0

Enter starting vertex: 0

(e) Sample Output
DFS Traversal: 0 1 2 3
BFS Traversal: 0 1 2 3


(Traversal order may vary depending on adjacency matrix arrangement)

Conclusion

This program demonstrates:

Implementation of an undirected graph using an adjacency matrix

Graph traversal using Depth First Search (DFS)

Graph traversal using Breadth First Search (BFS)

Proper use of recursion and queue data structures

Time Complexity

DFS: O(n²)

BFS: O(n²) (due to adjacency matrix)

Space Complexity

O(n²) for adjacency matrix

O(n) for visited array and queue