
### Introduction
- Primary transfer protcol of browsers 
- **request-responce**

## HTTP

### Request Structure

| Method | URL or pathname                | HTTP version | headers | message body |
| ------ | ------------------------------ | ------------ | ------- | ------------ |
| GET    | //www.dcs.qmw.ac.uk/index.html | HTTP/1.1             |         |              |

- **Method**
	- nature of request
- **URL**
	- resource - object of request
- **HTTP Version**
- **Headers**
	- additional info
	- Host:\<hostname>, auth information, content type options 
- **Body**
	- Request data
	- document being uploaded 



### Methods

- **GET**
	- requests a document
- **HEAD**
	- request status information
- **POST**
	- Sends data to the server
	- form submissions
	- server APPENDS the data
- **PUT**
	- Sends data
	- server REPLACES the data
- **DELETE**
	- request document to be deleted
- **OPTIONS**
	- query which methods can be used 


### Responce 

| HTTP version | status code | reason | headers | message body  |
| ------------ | ----------- | ------ | ------- | ------------- |
| HTTP/11      | 200         | OK     |         | resource data | 

- **Status codes**
	- 200
		- OK
	- 400
		- Bad Request
	- 403
		- Forbidden
	- 404
		- not found
	- 301
		- moved
	- 307
		- redirect
- **Headers**
	- Content length
	- Content type 
		- is it HTML?

### Example 

**Request**
![[Pasted image 20230303163409.png]]

**Response **
![[Pasted image 20230303163442.png]]

![[Pasted image 20230303163455.png]]

