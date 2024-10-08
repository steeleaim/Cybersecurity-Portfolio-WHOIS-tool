This small project helps demonstrate how socket import works in python and understanding WHOIS responses. 


In networking a socket is an endpoint for sending and recieving data across a network - sockets enable computers to communicate over the internet or other networks.
You can see this process in the script - 
1. Create socket (s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)) where AF_INET specifies address family and SOCK_STREAM establishes this is a TCP connection.
2. Connect to a remote server (IANA WHOIS in this instance on port 43) Port 43 is the designated port for the WHOIS protocol.
3. Send domain query (in this case, google.com). The encode() function converts the string into bytes - sockets operate on raw byte data.
4. Recieve a response. In this instance 4096 bytes is stipulated (4096 bytes matches the page size on many modern operating systems and is usually enough to retrieve the entire response
   from a WHOIS in a single call). Decode() converts back into str data. 
5. Close connection.
