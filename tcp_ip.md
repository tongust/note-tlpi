# TCP v.s. UDP
- UDP (Unreliable Datagram Protocal) extend IP slightly, so that packets can be transformed from process to process, rather than host to host.
- TCP is a complex protocol that builds on IP to provide reliable full duplex (bidirectional) connections between protocol.

# DNS
ip addr mapped to domain name (human-friendly)
The mechanism: Domain Name System:
The mapping is maintained by a distributed world-wide database.

# Internet connection
A connection is full-duplex and reliable.

A scoket is an end point of a connection.

Scoket address consisting of an IP address and a 16-bit integer port, is denoted by address:port.

> The port on client who makes a request is assigned automatically by kernel, known as ephemeral port.
> The port on server is associated with the service, well-known port. Such as 22 for ssh, 80 for Web server.

Scoket pair: tuple

*(cliaddr:cliport, servaddr:servport)*


# TCP
The Transmission Control Protocol (TCP) level of the TCP/IP transport protocol is connection-oriented. Connection-oriented means that, before any data can be transmitted, a reliable connection must be obtained and acknowledged. TCP level data transmissions, connection establishment, and connection termination maintain specific control parameters that govern the entire process. The control bits are listed as follows:

- URG: Urgent Pointer field significant
- ACK: Acknowledgement field significant
- PSH: Push Function
- RST: Reset the connection
- SYN: Synchronize sequence numbers
- FIN: No more data from sender

