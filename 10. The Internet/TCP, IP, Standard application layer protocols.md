The TCP/IP stack is a set of rules used in turn, to format a message so it can be sent over a network. Each layer provides a specific function within the transmission of the message.

![[Pasted image 20230209095858.png]]

The stack uses four connected layers to allow network communication to take place. Each layer wraps the packets with its own header. At the destination the message is passed back up through the layers.

- [[#Application Layer]]
- [[#Transport Layer]]
- [[#Network Layer]]
- [[#Link Layer]]

## Application Layer

Used to provide services for applications that want to communicate across a network, often the internet.

Using high-level protocols that set an agreed standard between the communicating end-points. IE SMTP, FTP and HTTP.

Does not actually determine how the data is transmitted rather specifies the rules of what should be sent.

## Transport Layer

Uses the Transmission Control Protocol (TCP) to establish an end-to-end connection with the recipient computer.

- Splits data into packets and numbers them sequentially.
- Adds the port number to be used based on HTTP protocol.
- At the receiving end this layer confirms that packets have been received and requests any missing packets to be resent.

## Network Layer

Uses the Internet Protocol (IP) to address packets with the source and destination IP addresses.

A router forwards each packet towards an endpoint called a socket, defined by the combination of IP address and port number.

## Link Layer

The link Layer operates across a physical connection.

- Adds the MAC address of the physical NIC that packets should be sent to based on the destination IP address.
- MAC addresses change with each hop.

## Port Numbers

A port is used to alert a specific application to deal with data sent to a computer. These are used by protocols to specify what data is being sent. The combination of an IP address and a port number, separated by a colon, is known as a socket.

| Server port number | Protocol                             |
| ------------------ | ------------------------------------ |
| 20                 | File transfer protocol DATA (FTP)    |
| 21                 | File transfer protocol CONTROL (FTP) |
| 22                 | Secure Shell remote login (SSH)      |
| 23                 | Telnet remote login                  |
| 25                 | Simple mail transfer protocol (SMPT) |
| 80 and 8080        | HyperText transfer protocol (HTTP)   |
| 110                | Post office protocol v3 (POP3)       |
| 143                | Internet mail access protocol (IMAP) |
| 443                | HyperText transfer protocol secure (HTTPS)                                     |

## Transferring Files with FTP

File transfer protocol is an application level protocol used to move files across a network. Usernames and passwords are frequently used to protect access to files and to identify users.

## Secure Shell

Secure shell (SSH) is an encrypted protocol that allows secure communication between nodes across a network. SSH can be used to create a tunnel through a network. This tunnel can be used to pass through data that might otherwise be blocked.

![[Pasted image 20230209101832.png]]

## Sending and Receiving Email

Mail servers are dedicated computers that are responsible for storing email, providing access to clients and providing services to send emails.

They use three protocols:

- SMTP: Used to send emails and forward them between mail servers to their destination
- POP3: Downloads email stored on a remote server to a local client (removed after download)
- IMAP: Manages emails on a server so multiple clients can access the same email account in synchronicity.

### Comparison between IMAP and POP

IMAP holds mail on the server so that multiple devices can access all mail.

POP downloads mail to a local device and removes it from the server.

## Web Servers

Dedicated computers that host websites and provide resources on request. HTML, CSS and JavaScript are separated and broken down into their constituent parts. These text elements are further broken down and rendered on the client browser according to a standard hierarchical model. Other page resources such as images, videos or scripts are subsequently downloaded as the page is rendered.
