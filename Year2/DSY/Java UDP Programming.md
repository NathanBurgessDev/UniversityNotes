
### Java UDP API

- **DatagramPacket** - UDP datagram
	- Message bytes, length, remote address, remote port
- **DatagramSocket** - UDP socket
	- Bound to a specific port
	- `send()` and `receive()` methods for **DatagramPackets** 
	- configureable receive timeout
	- `connect()` optionally associate with a single remote address

### UDP Client

- Sends a message to the server and gets a reply 

1. Make a DatagramSocket  
2. Make a DatagramPacket with payload and destination (server) host & port  
3. .send the DatagramPacket as a UDP packet  
4. Make an empty DatagramPacket  
5. .receive the next UDP packet into that  
DatagramPacket  
6. ...
``` Java
import java.net.*;  
import java.io.*;  
public class UDPClient{  
	public static void main(String args[]){  
		// args give message contents and server hostname  
		DatagramSocket aSocket = null;  
		try {  
		aSocket = new DatagramSocket();  
		byte [] m = args[0].getBytes();  
		InetAddress aHost = InetAddress.getByName(args[1]);  
		int serverPort = 6789;  
		DatagramPacket request = new DatagramPacket(m, m.length(), aHost,  
		serverPort);  
		aSocket.send(request);  
		byte[] buffer = new byte[1000];  
		DatagramPacket reply = new DatagramPacket(buffer, buffer.length);  
		aSocket.receive(reply);  
		System.out.println("Reply: " + new String(reply.getData()));  
		} catch (SocketException e){System.out.println("Socket: " + e.getMessage());  
		} catch (IOException e){System.out.println("IO: " + e.getMessage());  
		} finally {if(aSocket != null) aSocket.close();}  
	}  
}
```

### UDP Server 

