### Java TCP API
- `ServerSocket` represents a server TCP socket
	- bound to a particular port 
	- waiting to accept connecton requests from client sockets
- `Socket` represents one end of a TCP connection
	- Explicitly created by a client with a specified sever IP address and port number 
	- returned from `accept` in server
	- can be queried for local and reote addresses and port numbers 
	- has na `java.io.InputStream` to receive bytes from and a `java.io.OutputStream` to send bytes to

### TCP Client 
``` Java
import java.net.*;  
import java.io.*;  
public class TCPClient {  
public static void main (String args[]) {  
// arguments supply message and hostname of destination  
Socket s = null;  
try{  
int serverPort = 7896;  
s = new Socket(args[1], serverPort);  
DataInputStream in = new DataInputStream( s.getInputStream() );  
DataOutputStream out =  
new DataOutputStream( s.getOutputStream() );  
out.writeUTF(args[0]); // see encoding and representation  
String data = in.readUTF();  
System.out.println("Received: "+ data) ;  
} catch (UnknownHostException e) {  
System.out.println("Sock:"+e.getMessage());  
} catch (EOFException e) {System.out.println("EOF:"+e.getMessage());  
} catch (IOException e) {System.out.println("IO:"+e.getMessage());  
} finally {if(s!=null) try {s.close();} catch (IOException e)  
{System.out.println("close:"+e.getMessage());}}  
}  
}
```


### TCP Server 
```Java
import java.net.*;  
import java.io.*;  
public class TCPServer {  
public static void main (String args[]) {  
try{  
int serverPort = 7896;  
ServerSocket listenSocket = new ServerSocket(serverPort);  
while(true) {  
Socket clientSocket = listenSocket.accept();  
Connection c = new Connection(clientSocket);  
}  
} catch(IOException e) {System.out.println("Listen :"+e.getMessage());}  
}  
}
class Connection extends Thread {  
DataInputStream in;  
DataOutputStream out;  
Socket clientSocket;  
public Connection (Socket aClientSocket) {  
try {  
clientSocket = aClientSocket;  
in = new DataInputStream( clientSocket.getInputStream() );  
out =new DataOutputStream( clientSocket.getOutputStream() );  
this.start();  
} catch(IOException e) {System.out.println("Connection:"+e.getMessage());}  
}  
public void run(){  
try { // an echo server  
String data = in.readUTF();  
out.writeUTF(data);  
} catch(EOFException e) {System.out.println("EOF:"+e.getMessage());  
} catch(IOException e) {System.out.println("IO:"+e.getMessage());  
} finally{ try {clientSocket.close();}catch (IOException e){/*close failed*/}}  
}  
}
```
### TCP Considerations 
- **Message Size**  - application reads / writes any number of bytes at a time until the connection is closed 
	- App does not see any message boundaries
	- needs to communicated any message boundaries explicitly in the bytes sent 
- **Message destinations** - a server can accept connection requests from any client 
	- once the connection is esablished then bytes are communicated only between that pair of processes 
- **blocking** - a limited amount of data is buffered at sender and receiver sockets and sends will **block** once the sender buffer is full
	- **flow control** 
	- connecting to a sever
	- acception a connection 
	- and reading from a socket normally block
- **Failure model** - COmmunication is reliable short of complete connection failure
	- lost messages are automatically retransmitted
	- duplicate packets are discarded and out of order packets are re-ordered
	- if a loss is not resolved within a time limit
		- connection fails

### Summary

- **TCP** proved a reliable connection oriented bidirectional byte based stream service
	- persistent network packet losses result in the connection failing 
	- blocking connect accept and receieve 
	- for almost any application transfering data reliably and or in significant amounts
		- HTTP, SSH, FTP, SMTP
-