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

3. Cloning of the antibodies (immune operator clone).
This creates a temporary population of clones C*, the size of which is determined by the previously entered parameter.

4. Mutation of clones (immune operator mutate). 
Change the values of randomly selected clones, the mutation probability is set by the parameter.

5. Calculating the affinity of clones of the C* population.

6. Select the clones and replace them with the appropriate antibodies (immune operator select + replace function). 
Select from the C* population antibodies with improved affinity as a result of the mutation, replace with them the corresponding antibodies from which the clones were made.

7. Edit the population (rand function + immune operator edit). 
Replace d antibodies with worse affinity with new randomly generated antibodies to maintain population diversity. 
The worse the affinity of the antibody, the more likely it is to be replaced by a new one.

## Results 

* Himmelblau's function

The result of the algorithm: (3.0026466852776252, 2.018511776569314)

![image](https://user-images.githubusercontent.com/48069220/229287811-0c14fa66-4550-4924-9020-dfcc5465fd41.png)

* $z = x \cdot e^{-x^2 - y^2}$

The result of the algorithm: (-0.7167317191914844, 0.011737349447571432)

![image](https://user-images.githubusercontent.com/48069220/229287874-8992f4bb-81fa-4fcb-b3e9-8d391dfac41e.png)

* $z = x^2 + y^2 - cos(18x) - cos(18y)$

The result of the algorithm:(0.002825976091856086, -0.0016686920329790356)

![image](https://user-images.githubusercontent.com/48069220/229287959-0480a762-4fc6-4e70-94e4-353c822592d9.png)


* $z = x \cdot y \cdot sin(x^2 + y^2)$

The result of the algorithm: (0.9991855619396119, -0.9992041585932157)
![image](https://user-images.githubusercontent.com/48069220/229288076-57e4c3d1-7f3d-49e4-b4ee-2b01c4bebadf.png)

