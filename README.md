# ClonAlg

## An idea of the algorithm

Clonal selection is the name given to the theory that explains how the adaptive immune system (acquired immunity) copes with pathogens. 
In the process of clonal selection, the natural immune system involves B- and T-lymphocytes, with the difference that B-lymphocytes are subject to mutation, 
while T-lymphocytes are not. 
Therefore, in computational models of clonal selection, only B lymphocytes are modelled,
because it is thanks to mutation that the immune system becomes adaptive. 
In the theory of clonal selection, the most important provisions from a computational point of view are the following:

* An antibody recognises a foreign antigen with a certain affinity;
* this antibody is selected for cloning and produces a set of antibody clones, which are then subjected to a mutation process;
* The mutation process results in newly created antibodies with better affinity for a given antigen than the original antibody selected;
* activated antibodies with high affinity are stored in memory.

## Areas of application of the CLONALG algorithm

* Pattern recognition (binary images);
* Optimisation of multimodal functions;
* Combinatorial optimisation (traveling salesman problem).

## Steps of the CLONALG algorithm for solving the optimisation problem 

1. Generation of the antibody population Ab (rand function). 
The population of antibodies is a set of possible solutions to the optimisation problem. 
Each antibody is a bit string that stores the coordinates of the point of possible minimum (x1, x2), encoded in the Gray code. 
The population is generated randomly by filling the bits with values 0 and 1.

2. Calculation of the affinity of Ab antibodies to an antigen (affinity function)
The antigen is the objective function F(x1, x2). 
In this case, the affinity of each antibody will be calculated as the value of the objective function at the point whose coordinates are encoded in the antibody.

Himmelblau's function
