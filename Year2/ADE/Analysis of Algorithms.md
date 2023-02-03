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

#### Counting Primitive Operations 
![[Pasted image 20230203171529.png]]

- Can determine the max number of primitive operations executed by an algorithm
- 

### RAM Model

- A CPU
- unbounded bank of memory 

#### Limitations 
- cant expect to store really large numbers in a single memory cell
- We ignore bigum issues

### Counting 

- Underspecified 
- Consider c = A[i]
	- get A = pointer to start of array A, and store into a  register  
	-  get i, and store into a register  
	- compute A+i = pointer to location of A[i], and store  back into a register  
	- get value of “*(A+i)” (from RAM) and store value it  into a register  
	- copy the value into the location of c in the RAM
- might not want to count all this, e.g. just count  
	- ‘plus’ of “A+i”  
	- the assignment

### Correctness vs Efficiency 

- Pimitive operation counting is relevant to Efficiency but not for Correctness
- Correctness do not care about tuntime 


### Estimating Run time 

- Algorithm `arrayMax` executes `8n − 4` primitive  
	operations in the worst case. Define:  
- a = Time taken by the fastest primitive operation  
- b = Time taken by the slowest primitive operation

- Let T(n) be worst-case time of arrayMax. Then  
- a (8n − 4) $\leq$ T(n) $\leq$ b(8n − 4)

Hence, T(n) is bounded ‘above and below’ by  
two linear functions  
• Usually said as “  
arrayMax runs in linear time”

### Growth Rate of Running Time
- Changingthe hardware / software enviroment
	- affects `T(n)` by a constant factor
	- does not alter the growth rate of `T(n)`
- Linear growth rate of the running time `T(n)` is an instrinsic property of `arrayMax`