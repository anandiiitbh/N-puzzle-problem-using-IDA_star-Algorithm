# N-puzzle-problem-using-IDA_star-Algorithm
Solving N puzzle using the IDA* algorithm using heuristic function based on Manhattan Distance and number of misplaced tiles

Language Used: C

Problem Introduction:

Sliding puzzle problems are good examples to understand informored search algorithms. In Artificial Intelligence, A* and IDA* algorithms are used to find the goal using the heuristic.

A* algorithm follows BFS approach, With admisible heuristic we can find optimal path by expanding the less nodes.

Since A* algorithim has memory constraint(BFS space complexity is b power d), it is not possible to solve when the state space increases, ex. 15 puzzle. To overcome this limit ida* algorithim is used. In ida*, depth-first search (space complexity is b*d) being called iteratively with depth limit value. When f(n) reaches iterative depth limit( when depth-limit>f(n) ) its path is cutoff and continoueses again. Here f(n)=g(n)+h(n), g(n) is the cost to the node and h(n) is heuristic calculated using Manhattan Distance,number of misplaced tiles.

Usage:

run the program after writing input array size (N=8/15) , initial state of tiles and goal state os tiles into start and goal file repectively. considering the blank tile represented by number 0

Sample run

start.txt :

3
4 3 0
6 7 2
8 1 5

goal.txt :

0 1 2
3 4 5
6 7 8

Further Enhancements:

There is lot of chance to improve the performance of this program further. Since I was in hurry to submit my assignment I did code boilor plate coding and using the unnecesary variables(like pathVisited is HashMap variable used to track the required moves to reach goal state this can be avoided by keeping path variable in Node and handling state properly).
