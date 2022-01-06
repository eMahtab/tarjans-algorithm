# Tarjan's Algorithm
Tarjan's algorithm is used to find the strongly connected components in a graph using DFS.

## Algorithm :
1. Initialize both `discovery` and `low` array with -1, note that `discovery` array will serve two purposes : if discovery[vertex] == -1 it means this vertex was not discovered before and second purpose is we will store the discovery id of vertex at discovery[vertex]. 
2. Take a variable which denotes the id at which a vertex was first discovered and initialize it to 0
3. Start the DFS from vertex 0
4. If the vertex is not already discovered then set `discovery[vertex] and low[vertex] to be id` and increment id by 1 for next node.
5. Next check all the neighbors of this vertex (those which are not yet discovered and also those which are already discovered).


