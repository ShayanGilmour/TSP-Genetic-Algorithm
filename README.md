# Traveling Salesman Problem with Genetic Aglrotihm
### Input:
The distances between each pair of vertices. There are two methods available in the code for reading the input. 
1.  At line `i`, there should be `n-i` space-separated integers; The `j`th integer indicates the distance between vertex `i` and `i+j`. 
2.  At line `i`, there should be three space-separated integers; First, the index of the vertex, second and third integers indicates the coordinate of the vertex.

### Process:
Using Genetic Algotihm, it find the "shortest" cycle including every vertex. Every cycle is stored as a permutation of vertices. 

Function `crossover` inputs 2 permutations, and randomly returns one crossover (child) of those two permutations.
Function `fitness` inputs one permutation (which represents a cycle,) then returns the length of that cycle. (The name of this function should be `cost`, as the higher the value is, the worst the cycle.)
Integer `m` in the code represents the number of the population held in every generation.
List `gen` represents the cycles of the current generation.
`mRate` represents the "Mutation Rate".

The main loop iterates the generations.

### Output:
Outputs one integer: The length of the shortest cycle. And the sequence of the found cycle.
