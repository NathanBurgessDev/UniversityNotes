
### Definition of A Distrubuted System
- Hardware or software componennts located at networked computers communicate and coordinate their actions only by passing messages 

### Resource Sharing 
- Physical resources 
	- Printers
	- disks 
	- computers
	- people(?)
- Data
	- files
	- documents
	- databases
	- web pages
- Computational / algorithmic resources
	- search engines
	- machine learning algorithms 

### Services 
- Distinct part of a computer system that manages a collection of related reources
- presents their functionality to users and applications 
	- runs on specific machine which phsyically hosts the managed resources 
	- provides a specific and controlled interface
		- usually over a network
	- to the resources it manages 
- Many distributed systems consist only of clients making requests to servers to access or manipulate the resources managed by that services 

### Examples 
![[Pasted image 20230131110818.png]]


### Architecture 
- What are the entities that are communicating 
	- Often Operating System processes
- How do they communciated (what paradigm)
	- Often direct, request-response communication 
- What (potentially changing) roles and responsibilities do they have in the overall architecture 
	- Client and Server 
- How are they mapped on to the physical distributed infrastructure (what is their **Placement**)
	- On user desktop and cloud server 

### Summary 
![[Pasted image 20230131111151.png]]