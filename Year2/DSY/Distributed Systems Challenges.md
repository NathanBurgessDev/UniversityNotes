
### Challenges
- Common challenges
	- **Heterogeneity** - copying with system component variability
	- **Failure Handling** - coping with partial failure 
	- **Concurrency** - correctness and performance with concurrency 
- Other Challenges
	- Openness
	- Secuirty
	- Scalability 
	- Transparency 
	- Quality of Service

### [[Distributed Systems Challenges#Challenges|Heterogeneity]]

- All the parts of a distrobuted system have to work together even if some are made differently 
	- different network technoligies, CPUs, architectures, operating systems, programming languages, developers 
- Typicaly this will mean using common protocols, interfaces and encodings 
- Example
	- Java Data I/O streams 

### [[Distributed Systems Challenges#Challenges|Failure Handling]]

- Can fail in complicated ways
- coping with failure reuires
	- redundency
	- means of detecting and respodning to partial failiures
- Example
	- Simple TCP server

### [[Distributed Systems Challenges#Challenges|Concurrency]]
- Different processes in a distrbuted system normally run concurrently
- This may require additional checks and communication to ensure global consistency 
	- can limit performance or scalabilty 
- OR use alternative but less consistent approaches
	- loosely couples / optimisitc solutions 
- Example
	- TCP server is multi threaded
	- can server multipele clients concurrently 

