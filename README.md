# lab-report-03
 Implementation of Graph Coloring Using Backtracking

NAME : Thiaba Rahman Methi ID : 232002042

Course Title: Artificial Intelligence Lab Course Code: CSE-316 Section:232_D7

**Problem**

You are given an undirected graph with N vertices and M edges. Your task is to implement a Python program that uses Backtracking to determine whether the graph can be colored using K colors such that no two adjacent vertices share the same color. The input will be read from a file, where the first line contains three integers: N (number of vertices, numbered from 0 to N−1), M (number of edges), and K (number of available colors). Each of the following M lines contains two integers u and v, representing an undirected edge between vertex u and vertex v.

**Solution**

In this problem, I used the backtracking approach to solve the graph coloring task. The idea is to assign colors to each vertex one by one while making sure that no two connected vertices get the same color. For each vertex, I try all the available colors and check if the selected color is safe by comparing it with its neighboring vertices. If the color does not cause any conflict, I assign it and move to the next vertex. If a conflict occurs or no color works, I go back to the previous vertex and try a different color. This process continues until either a valid coloring is found or it is clear that the graph cannot be colored with the given number of colors.

**Steps**

First, read the input values and build the graph using an adjacency list. Then initialize all vertices as uncolored. Start from the first vertex and try assigning colors one by one. For each assignment, check if it is safe with neighboring vertices. If safe, move to the next vertex; otherwise, try another color. If no color works, backtrack and change the previous assignment. Continue this process until all vertices are colored or no solution is possible.


Case#1Input:
4 5 3
0 1
0 2
1 2
1 3
2 3

Case#1Output:
Coloring Possible with 3 Colors
Color Assignment: [1, 2, 3, 1]

Case#2Input:
4 5 2
0 1
0 2
1 2
1 3
2 3

Case#2Output:
Coloring Not Possible with 2 Colors
