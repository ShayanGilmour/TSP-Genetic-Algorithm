# Traveling Salesman Problem with Genetic Algorithm
"Solving" the TSP via implementing Genetic/Memetic Algorithm with Python.

### Input:
The distances between each pair of vertices. There are two methods available in the code for reading the input. 
1.  At line `i`, there should be `n-i` space-separated integers; The `j`th integer indicates the distance between vertex `i` and `i+j`. 
2.  At line `i`, there should be three space-separated integers; First, the index of the vertex, second and third integers indicates the coordinate of the vertex.

### Process:
Using Genetic Algorithm, it finds the "shortest" cycle including every vertex. Every cycle is stored as a permutation of vertices. 

Function `crossover` inputs 2 permutations, and randomly returns one crossover (child) of those two permutations.

Function `fitness` inputs one permutation (which represents a cycle, ) then returns the length of that cycle. (The name of this function should be `cost`, as the higher the value is, the worst the cycle.)

Integer `m` in the code represents the number of the population held in every generation.

List `gen` represents the cycles of the current generation.

`mRate` represents the "Mutation Rate".

The main loop iterates the generations.

### Output:
Outputs one integer: The length of the shortest cycle. And the sequence of the found cycle.

#### Postlude:
The program reads the input from a file; The file `bayg29.tsp`, contains a sample input, consisting of 29 vertices; I've downloaded this sample from [Heidelberg University' Site](http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/). The optimal answer for this test case is `1610`, which this code can almost always find the answer of 1610 (the optimal answer) **in less than 5 seconds**.

## Update:
I've implemented my improvised version of Genetic Algortihm, which is available at [this link.](https://github.com/ShayanPey/N-Queens).
At first level, it randomly generates some permutations, and let them evolve for a little bit (Not long.) Then it saves this "little evolved" population. Then again, it generates some random permutations, and again let that evolve for a little and so on... It repeats this process several times. So, this prevents the populations to get "narrow".

At second and levels above, it randomly chooses from the previous level (just like first level, but instead of generating new permutations, it chooses from previous level.) And let them evolve a little bit but not much! And so on...

I got this idea from the structure of Segment Tree:
<p float="left">
  <img src="https://user-images.githubusercontent.com/12760574/130359662-f19c6aea-e12b-41b0-88db-90404dd35358.png" width="600" />
</p>

This makes it like hydraulic press! It's slower, but it will penetrate through the hardest of problems!
