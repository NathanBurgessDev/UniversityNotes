
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
- WWW depends on HTTP URL HTML - independent of local structure

### [[Distributed Systems Challenges#Challenges|Failure Handling]]

- Can fail in complicated ways
- coping with failure reuires
	- redundency
	- means of detecting and respodning to partial failiures
- Example
	- Simple TCP server
- WWW - if one web server fails others are not affected

### [[Distributed Systems Challenges#Challenges|Concurrency]]
- Different processes in a distrbuted system normally run concurrently
- This may require additional checks and communication to ensure global consistency 
	- can limit performance or scalabilty 
- OR use alternative but less consistent approaches
	- loosely couples / optimisitc solutions 
- Example
	- TCP server is multi threaded
	- can server multipele clients concurrently 
- WWW -most web severs will ahve to cope with many concurrent requests

### Openness
- Want to extend, re-implement and interoperate 
	- requires agreeing and publishing protocls and interfaces
- WWW -  uses standard protcols so that any web clinet can interact with any web server

### Security 
- Many of the resources in distributed systems are valuable 
- A range of security measures may be needed
- WWW - HTTPS

### Scalability 
- A system is scalable if it continues to work well as it grows
- Requires careful design and engineering 
- WWW - browsers have cache to reduce data requests

### Transparency 
- Users / other systems cant see internal details of the sysem
	- **Access**
		- Local vs remote
	- **Location**
		- Where
	- **Replication**
		- using replicas
	- **Failiure**
		- hiding partial failiures
	- **Mobility**
		- Unaffected by physical movement 
- WWW - URL's support access and location transparency

### Quality of Service 
- Various non-functional aspects
	- performance
	- reliability
		- reliable service on unreliable network]
		- Auto adjust stream video quality to cope with bandwidth variability
	- security
- WWW - HTTP is normally as reliable as TCP
	- there are extensions for reliable HTTP 
