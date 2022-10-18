#bellman ford
function BellmanFord(list vertices, list edges, vertex source, distance[], parent[])
 
// Step 1 – initialize the graph. In the beginning, all vertices weight of
// INFINITY and a null parent, except for the source, where the weight is 0
 
for each vertex v in vertices
    distance[v] = INFINITY
    parent[v] = NULL
 
distance[source] = 0
// Step 2 – relax edges repeatedly
    for i = 1 to V-1    // V – number of vertices
        for each edge (u, v) with weight w
            if (distance[u] + w) is less than distance[v]
                distance[v] = distance[u] + w
                parent[v] = u
 
// Step 3 – check for negative-weight cycles
for each edge (u, v) with weight w
    if (distance[u] + w) is less than distance[v]
        return “Graph contains a negative-weight cycle”
 
return distance[], parent[]
