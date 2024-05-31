# Dijkstra-s-Algorithm
Dijkstra’s Algorithm
Let's consider a scenario where we have a shipment to be transported from the origin (SL) to its final destination (WA). This destination could be a warehouse, distribution center, port, or customer. Our goal is to identify the shortest path between the two nodes (SL and WA), minimizing the total distance traveled. The numbers in this figure represent distances in the transportation network

![image](https://github.com/heshamosama165/Dijkstra-s-Algorithm/assets/106331921/c2632cf2-3737-4fbe-ba95-59f405b60868)
(Image Source: MIT SC0x Course)

Linear Programming Formulation:
![image](https://github.com/heshamosama165/Dijkstra-s-Algorithm/assets/106331921/48da23b4-95ab-4533-bbdb-bb0fa1915749)

Where:
•	Minimize Cost: This indicates that we want to find the path with the least total cost amongst all possible paths.
•	Cij: Cost per unit for flow from node i to node j 
•	Xij: Number of units flowing from node i to node j
•	Source: where flow starts
•	Destination: where flow ends
•	Σ (summation): This symbol indicates that we need to find the sum of the costs across all the edges in the path.
•	Σ Χ(jk) - Σ Χ(ji) = 0 for all j ≠ source, destination: This constraint ensures that the total cost of incoming edges (Σ Χ(jk)) must be equal to the total cost of outgoing edges (Σ Χ(ji)). This basically represents the flow conservation constraint, where the total flow entering a node must be equal to the total flow exiting the node.

•	Χ(js) = 1: This constraint specifies that the cost of the edge leading out of the source node (s) must be 1. This seems like an arbitrary assignment but mathematically it helps ensure that the path followed starts from the source node.
•	Χ(jd) = -1: This constraint specifies that the cost of the edge leading into the destination node (d) must be -1. Similar to the previous constraint, this assignment helps mathematically identify the path that ends at the destination node
