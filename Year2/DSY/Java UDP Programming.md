
### Java UDP API

- **DatagramPacket** - UDP datagram
	- Message bytes, length, remote address, remote port
- **DatagramSocket** - UDP socket
	- Bound to a specific port
	- `send()` and `receive()` methods for **DatagramPackets** 
	- configureable receive timeout
	- `connect()` optionally associate with a single remote address