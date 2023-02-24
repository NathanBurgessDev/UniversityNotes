
### DNS name spaces

- Names in DNS are called **domain names**
- Name space is **hierarchical** 
	- **name components** or **labels**
	- delimiters i.e. "."
- **Absolute** not relative 
	- However - default domains are often configured to try as a possible suffix for unqualified names
- Attributes are encoded as **resource records** of various types or various purposes 

### DNS Applications and Resource Records 

- **Host name resolution** - mapping a domain name to an IP address
	- DNS A (IPv4) and AAAA (IPv6) records
		- attribute value -> IP address
	- DNS **CNAME** records specifical an **alias**
		- Attribute value is another domain name 
		- auto checked when resolving a domain name to an IP address
- **Mail host location** - finding mail server to send internet email to
	- DNS **MX** records
		- attributevalue is the mail servers domain name and a priority
-
### DNS data records
![[Pasted image 20230224123207.png]]


### Other Applications (less important)

- **Reverse Resolution** - mapping IP address to domain name
	- uses DNS **PTR** records under the domain *in-addr.arpa* 
	- sometimes used for security
- **Host information** - OS
- **Service** lookup 

### Multiple Records 
- A single domain name can have multiple records of the **same** type
	- alternative values
	- for redundency, reliability and load balancing 
- Multiple NS records => duplicate nameservers  
-  Multiple MX records => alternative mail servers  
- Multiple A records => multiple network interfaces for same host, or multiple hosts providing the same service

- Returned in diff orders to diff clients

### Administrative domains 

- A subset of namespace with a single administrative authority
- Corresponds to a domain name suffix
	- DNS **zone**
	- e,g, nottingham.ac.uk
- Each **authority** has complete control over its own administrative zones 


### DNS Name Servers 

- A DNS **server** is responsible for one (or more) **zones** 
	- gives **authoritative answers** for those zones
	- Must be **replicated** - redundency
	- Each zone / server is identified in DNS by a **Start Of Authority** record
	- **NS** (Name Server) records identify responsible (authoritative) name servers 

- A **root server** gives answords for "." the **root** domain
	- Highly replicated
	- Must know at least all top-level domain servers 
	
![[Pasted image 20230224123847.png]]

### Name resolution
- DNS name resolution is performed by a **resolver** 
	- sends initial request to a pre-configured name server
- Resolution may take multiple steps
	- the first name server may not know the answer
	- but knows the address of a different name server to ask
- These steps may be
	- **Iterative** - resolver asks each name server in turn
	- **Recursive** - the first servers asks the second 

### Caching 

- Every resource record has a **TIme To Live**
	- how long the value can be cached
- **Cacheing** is critical to the performance of DNS
- Cached responses are **non-authoritative**

### Other Notes

- DNS records may be updated autoamtically - **Dynamic DNS** 
	- as a PC joins a network
- DNS is rather insecure
	- give address of a malicious server
	- **Secure** extensions for DNS are not unversially used
	- **DNS over HTTPS** is a controversial standard for browsers 

### Summary

- **DNS** is a global name service
- **DNS** is divided into **administrative domains** or **zones**
- **DNS Clients** use a **resolver** to resolve domain names
- **DNS** includes **cacheing** in resolvers and servrs for scalability and performance 