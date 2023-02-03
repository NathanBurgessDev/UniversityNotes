### Running Time 
- Consider batch algorithms - transform input data into output data - as opposed to interactive
- the running time of an algorithm typically grows with the input size
- Evan at given size the runtime is usually not fixed
- We (usually) focus on the worst case running time at given size
![[Pasted image 20230203170432.png]]

### Experimental Studies

![[Pasted image 20230203170510.png]]

- Write a pgoram implementing the algorithm
- Run it with varying size and compositon inputs
- Use a system method to get an (in)accurate measure of the actual run time
- plot the results
- Interpret and analyise 

#### Limitations

- necessary to implement the algorithm
	- difficult
	- time consuming
- Results may not be indicative of the run time on non included inputs
	- might miss "real worst case"
- In order to compare two algorithms directly the same hardware and software must be used 

### Limitations of Theory

- Necessary to implement the theory
- Results may not be indicative of the typical run time on inputs encountered in real world