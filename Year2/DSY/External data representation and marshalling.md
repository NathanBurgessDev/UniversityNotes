- Networks just transport streams or blocks of bytes 
- Applications must agree on how data withina program will be represented as bytes on a network 
	- what encoding of an integer what character set for a character how to identify an object how to represent an array, how to represent a request
- **Marshalling** - process of converting program data to network form


### Java examples
- `getBytes` - String -> Array of bytes
	- reverse - `new string `
- `DataOutputStream` / `DataInputStream`
	- Java specific encoding for all primitive data types 
- **JSON** - Cross langauge UTF-8 text based encoding including maps and arrays 
	- {"a":"Hello!", "b":123}
- **XML** - cross language text-based encoding with HTML like markup 
- 