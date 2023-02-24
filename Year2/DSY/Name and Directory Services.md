
## Names

- A **name** uniquely distinguishes one thing from another like it
- **Identifiers** are names intended for machine use 
- **Desriptions** are statements about some aspect of a thing 

- A **pure name** is just an array of bits
	- no sturcutre or meaning - just identifies
- An **address** specifically locates a resources
	- good for access
	- bad if the object can move (address not valid)
- Different **services** may use different names 

### URI, URN and URL

- **Uniform Resource Identifiers** - service independent names
	- defined for WWW
- **Uniform Resource Names** - pure names
	- must always be looked up before being used 
- **Uniform Resource Locators** - include information to locate and access a resource 
![[Pasted image 20230224121033.png]]

### Name Services 

- In a **name service** - names are bound to attributes of the resource
	- A name is **resolved** to get these attribute values
- A **name space** is the set of possible names in a name service 
	- name spaces may be flat or hierarchical
	- any given name may be **bound** or **unbound**
	- Name spaces can be subdivided into naming **contexts**
- Name services can be independent of the distributed system
	- may contain names from diff systems (**unification**)
	- may contain names from diff admin domains (**Integration**)

### JavaRMI registry Example

- The **rmiregistry** application provides the **name service** 
	- one instance on each node
	- port 1099
	- any process on the local machine can register an object
- **names** are of the form "//HOST/OBJECT"
	- i.e. a fixed two-level hierarchical **name space**
		- first level is a host name
		- second is object name on that host
- **specific** to Java RMI

### Summary

- A **name** distringuishes one particular thing from others like it
	- **identifiers** are names intended for machine use 
- A **name service** allows a (pure) **name** to be **resolved** to an **address** or other **attritbutes** bound to that name
	- i.e. to contact the named resource
	- The set of possible names constitute the **name space** which is often a **hierarchy** 
- WWW **Uniform Resource Identifiers** 
	- **Uniform Resource Locators**
	- **Uniform Resource Names** - pure names 


## Directory Services

- **Directory services** allow clients to look up names or addresses using more flexible queries
	- SQL like queries over **attribute** values 
- AKA
	- **yellow pages** services
	- attributed based name services
- No globally used approach or system (contrast DNS)

### Summary
- A **directory service** allows resources to be looked up more flexibly than a name service
	- using **queries** based on attribute values 