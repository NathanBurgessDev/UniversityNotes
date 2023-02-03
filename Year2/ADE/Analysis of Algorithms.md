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




### Theoretical Analysis
- **AIM: Characterise running time as a function of input size n** 
- high level description of the algorithm instead of an implentation 
- pseudocode 

#### Limitations of Theory

- Necessary to implement the theory
- Results may not be indicative of the typical run time on inputs encountered in real world

### Primitive Operations 

- Basic computations performed by an algorithm
	- largely indepedent from the language
	- excact definition not important
	- assumed to take a constant amount of time IN **RAM MODEL**

### RAM Model

- A CPU
- unbounded bank of memory 

#### Limitations 
- cant expect to store really large numbers in a single memory cell
- We ignore bigum issues
- 