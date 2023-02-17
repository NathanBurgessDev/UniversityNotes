
- Programmers should be able to invoke remote operations in the same way as local procedure calls

- 3 key condierations
	- interfaces
	- semantics
	- transparency 

### Interfaces 

- Many languages support modularisatio with programmer defined interfaces
	- interface defines a public contract
	- code external to the module can only use things in the interface
		- encapsulation
		- other programmers only need to understand the interface 
	- A module can be replaced by another with the same interface and nothing else needs to be changed 

### Local vs Remote procedure calls 

- different modules may be running different processes
- still have defined interfaces
- may be different to local interfaces 