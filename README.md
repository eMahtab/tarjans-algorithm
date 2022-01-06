# Tarjan's Algorithm
Tarjan's algorithm is used to find the strongly connected components in a graph using DFS.

## Algorithm :
1. Initialize both `discovery` and `low` array with -1, note that `discovery` array will serve two purposes : if discovery[vertex] == -1 it means this vertex was not discovered before and second purpose is we will store the discovery id of vertex at discovery[vertex].
2. Take a `parents` array and initialize all the entries with -1. parents array will be used so that while doing dfs for neighbor v from parent u, we don't consider the parent node u. Before calling the DFS on neighbor v we will set `parents[v] = u`
3. Take a variable which denotes the id at which a vertex was first discovered and initialize it to 0
4. Start the DFS from vertex 0
5. If the vertex is not already discovered then set `discovery[vertex] and low[vertex] to be id` and increment id by 1 for next node.
6. Next check all the neighbors of this vertex (those which are not yet discovered and also those which are already discovered).
 
  (i). For a neighbor which was not already discovered, set the `parents[v]=u` and call dfs(), when dfs is completed for neighbor v, we update `low[u]` as `minimum of low[u] and low[v]` ; low[u] = Math.min(low[u], low[v]); also we check if discovery[u] < low[v] then it means (u,v) is a critical edge
  
  (ii). For a neighbor which was already discovered and which is not parents of this vertex, update low[u] as minimum of discovery[v] and low[u] ; low[u] = Math.min(low[u], discovery[v])
  
  


