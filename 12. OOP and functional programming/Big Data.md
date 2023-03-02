Big data includes data that is collected on such a large scale that it cannot easily be analysed. Big Data analytics can seek out patterns. There are three main characteristics of Big Data:

- Volume
	Big Data is too big to be handled by one server.
- Velocity
	Smartphones, sensor networks, and CCTV all create large volumes of data, continuously. The value and use of the data may require a response in the range of milliseconds to seconds.
- Variety
	Big Data comes in many forms; structured, unstructured, text, audio and image.

## The Relationship between Big Data and Functional Programming.

Large datasets required distributed processing: functional programming aids the production of correct and efficient distributed code.

- Immutable data structures. Meaning that none of the data is altered in a function.
- Statelessness. The program's behaviour does not depend on the order in which functions are called.
- Higher-order functions. Such as map and fold allow functions to be input as arguments.
All of these key features make Haskell and other functional programming languages very useful for data handling across multiple servers.

## Fact Based Model

Traditional data processing involving relational databases does not suit either the volume or the variety of Big Data. The fact based model captures a single piece of information.

## Graph Schema

Often there is value in exploring relationships between connected entities in a dataset.

Social networks are good examples of densely connected networks.

![[Pasted image 20230302161708.png]]

A dot or a Node represents one person or thing. Then a line or an edge represents a relationship.

These graphs can show scale.
