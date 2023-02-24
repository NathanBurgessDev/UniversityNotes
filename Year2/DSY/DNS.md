
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

### Admnistrative domains 
