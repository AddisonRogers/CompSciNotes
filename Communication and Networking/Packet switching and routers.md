## Circuit switching
Circuit switching involves creating a communication connection between two endpoints for the duration of a phone call or transfer of data. 
This does not work for the billions of inter-connected parts of the internet.

## Data packet
When sending across a network, data is broken into chunks (units) called data packets and assembled again at the receiving end. Increasing network efficiency and reliability.

## Packet switching
Packets are often sent across networks that have multiple links with multiple routes through to a destination

## Latency
Latency occurs from packets travelling across the network. ie it takes longer for packets to go from London to Sydney than London to Paris.

## Routing
Routers forward data packets from one network to another. 
Each router stores data about the available routes to the destination node.
Looks up the destination IP address in its routing table to find the best router to which to forward the packet.
Each forwarding by (or transfer across) a router is known as a hop.
Routers continue to forward the packet until it reaches its destination node.

## Building a packet
At its core, a data packet is a segment of data that needs to be sent, often referred to as the payload. 
The payload can range in size from 500 to 1,500 bytes.
The packet also has a header and a trailer.

Packets are deliberately small to ensure that individual packets do not take excessive time to transfer, preventing other packets from moving.

## Packet header
The header contains the recipient's address so that it can be directed appropriately across the network. It also includes the sender's IP so that replies can be sent easily.

The header has the sender's and Recipient's IP address protocol and packet number x of y.

## Packet trailer
Similarly, at the end of the packet a trailer is added. Containing components that verify the data received in the payload has not been corrupted on transfer.

## Gateways
A gateway is required where data is travelling from one network to another that use different protocols. Networks using different transmission media can require this. 
Header data are removed and reapplied using the correct format of the new network. It can often be combined with the router.