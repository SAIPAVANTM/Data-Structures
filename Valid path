#include <iostream>
#include <queue>
#include <vector>
using namespace std;
 
// Data structure to store a graph edge
struct Edge {
    int src, dest;
};
 
// A class to represent a graph object
class Graph
{
public:
    // a vector of vectors to represent an adjacency list in C++
    vector<vector<int>> adjList;
 
    // Graph Constructor
    Graph(vector<Edge> const &edges, int n)
    {
        // resize the vector to hold `n` elements each of type `vector<int>`
        adjList.resize(n);
 
        // add edges to the directed graph
        for (auto &edge: edges) {
            adjList[edge.src].push_back(edge.dest);
        }
    }
};
 
// Function to perform BFS traversal from a given source vertex in a graph to
// determine if a destination vertex is reachable from the source or not
bool isReachable(Graph const &graph, int src, int dest)
{
    // get the total number of nodes in the graph
    int n = graph.adjList.size();
 
    // to keep track of whether a vertex is discovered or not
    vector<bool> discovered(n);
 
    // create a queue for doing BFS
    queue<int> q;
 
    // mark the source vertex as discovered
    discovered[src] = true;
 
    // enqueue source vertex
    q.push(src);
 
    // loop till queue is empty
    while (!q.empty())
    {
        // dequeue front node and print it
        int v = q.front();
        q.pop();
 
        // if destination vertex is found
        if (v == dest) {
            return true;
        }
 
        // do for every edge (v, u)
        for (int u: graph.adjList[v])
        {
            if (!discovered[u])
            {
                // mark it as discovered and enqueue it
                discovered[u] = true;
                q.push(u);
            }
        }
    }
 
    return false;
}
 
int main()
{
    // vector of graph edges as per the above diagram
    vector<Edge> edges = {
        {0, 3}, {1, 0}, {1, 2}, {1, 4}, {2, 7}, {3, 4},
        {3, 5}, {4, 3}, {4, 6}, {5, 6}, {6, 7}
    };
 
    // total number of nodes in the graph (labeled from 0 to 7)
    int n = 8;
 
    // build a graph from the given edges
    Graph graph(edges, n);
 
    // source and destination vertex
    int src = 0, dest = 7;
 
    // perform BFS traversal from the source vertex to check the connectivity
    if (isReachable(graph, src, dest)) {
        cout << "Path exists from vertex " << src << " to vertex " << dest;
    }
    else {
        cout << "No path exists between vertices " << src << " and " << dest;
    }
 
    return 0;
}
