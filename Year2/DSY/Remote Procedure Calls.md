
- Programmers should be able to invoke remote operations in the same way as local procedure calls

- 3 key condierations
	- interfaces
	- semantics
	- transparency 

## Interfaces 

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

- It is not possible for code in one process to access variables in another

- Call by reference parameter passing is not possible between processes over networks
	- the pointer means nothing to a different machine 
- Parameters need to be clearly identifiable as passed to the procedure (in) return from it (out) or both (inout) 

### Interface Definition Languages
- Interfaces may be defined using a languages built in interface specification facilities 
- Or a separate interface definition language may be used
	- esp if interfaces are language independent
- Or built in interface specification facilites may be used but with additional constraints or annotations 

## Semantics 

- local procedure call semantions are always exactly one
	- every proedure call is executed exactly once
- Remote procedure calls can have different semantics
	- **maybe** - executed one or not at all
	- **at least once** - caller receives aresult or an exception is raisx