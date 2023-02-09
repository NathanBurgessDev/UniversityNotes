
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

- Repeatedly receives a request and sends it back to the client
- single threaded (note)
1. Make a DatagramSocket with known port  
2. (repeatedly...)  
3. Make an empty DatagramPacket  
4. .receive the next UDP packet into that DatagramPacket  
5. ...  
6. Make a DatagramPacket with payload and destination (client) host & port  
7. .send the DatagramPacket as a UDP packet

``` Java
import java.net.*;  
import java.io.*;  
public class UDPServer{  
	public static void main(String args[]){  
		DatagramSocket aSocket = null;  
		try{  
			aSocket = new DatagramSocket(6789);  
			byte[] buffer = new byte[1000];  
			while(true){  
				DatagramPacket request = new DatagramPacket(buffer, buffer.length);  
				aSocket.receive(request);  
				DatagramPacket reply = new DatagramPacket(request.getData(),  
				request.getLength(), request.getAddress(), request.getPort());  
				aSocket.send(reply);  
			}  
		} catch (SocketException e){System.out.println("Socket: " + e.getMessage());  
		} catch (IOException e) {System.out.println("IO: " + e.getMessage());}  
		} finally {if(aSocket != null) aSocket.close();}  
	}  
}
```


### Considerations 

- **Message Size**
	- Hard limit of 65508 Bytes
	- often 8k or less
		- larger messages are broken into smaller fragments
		- reassembled by the receiver if / when all are received
		- less reliable
- **Blocking**
	- Receive blocks normally until a message is received
		- A socket timeout can be specified 
- **Receive from any**
	- normaly a socket will accept messages from any sender 
- **Failure model- best effort**
	- Check sums detect most corruption 
	- Messages may be dropped
		- Corruption
		- no space in buffer at end of system
		- network congestion
		- messages may arrive out of order
		- messages may occasionally be duplicated 
- **Uses**
	- Small messages and simple interactions 
	- Avoids overheads of TCP
	- More complex applications require application to implement flow and congestion control
	- Supports Multicast communication 
