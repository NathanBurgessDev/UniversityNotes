
### Network Protocol 

- Set of fules about how to communicate 
	- what a service user can ask for
	- what info to send
	- when to send it
	- how to encode the info
	- what to do when something goes wrong 

### Network Protocol Stacks
- Each layer in the [[Networking (and virtualisation)#Typical Network Protocol Stack|protocol stack]]
- Has its own set of protocols 

### Distributed System Challenges
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

### [[Request Reply#Distributed System Challenges|Heterogeneity]]

- All the parts of a distrobuted system have to work together even if some are made differently 
	- different network technoligies, CPUs, architectures, operating systems, programming languages, developers 
- Typicaly this will mean using common protocols, interfaces and encodings 
- 