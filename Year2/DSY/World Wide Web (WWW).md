
### Introduction 

![[Pasted image 20230303160031.png]]

- **request-responce** - HTTP

## Web Protocols

- **HTTP**
	- How browser interacts with a web server
- **URL**
	- Specifies the format of web page identifiers
- **HTML**
	- Specifies the contents and layout of a webpage 

### Viewing a web page 
![[Pasted image 20230303160317.png]]

### URL
- *protocol://computer_name:port/document_name?parameters*
- Can omit any of the parts 
- *www.cs.nott.ac.uk
- removes protocol (assumes http)
- assumes the port (80 or 443)
- document name (/ or /index.html)
- paraments (none)


#### Handling 
1. Divides URL into parts
2. uses protcol to decide which protocol (HTTP, HTTPS)
3. uses computer name and port to form a TCP connection
4. uses name, document name and parameters to request a specific page 
5. displays the content from the server 

### Summary
- WWW is an open distributed system
	- based on standard protocols and representations
- URL specifies a web page 


