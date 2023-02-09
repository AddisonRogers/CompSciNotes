## Firewall
The entrance to a network can be protected in the same way. A firewall is either software or hardware that controls access to and from a network. Numbered doors called ports are opened so that only certain traffic is allowed to pass through. 

## Packet filtering
Packets of data are inspected by the firewall to check which port they are attempting to access. Different network protocols use different port numbers. If this traffic is to be allowed through, the port must be opened for the duration of the connection, otherwise the firewall will automatically reject it.

![[Pasted image 20230209104406.png]]

## Stateful inspection
Rather than relying on port numbers and IP addresses to determine passage, stateful inspection examines the payload of the packet before allowing access and remembers actions for future decisions.

## Proxy servers
A proxy server makes a web request on behalf of your own computer, hiding the true request IP addresses from the recipient.
![[Pasted image 20230209122619.png]]

Proxy servers can be used for:
- Anonymous surfing.
- Filtering undesirable online content.
- Logging user data with requests.
- Providing a cache of previously visited sites to speed access.

## Encryption
The act of encoding a plaintext message so that it cannot be deciphered unless you have numerical key to decrypt it. 

### Symmetric encryption
Symmetric encryption uses the same key to encrypt and then decrypt the data being transferred.
![[Pasted image 20230209123155.png]]
This is a relatively fast form of encryption and is generally used in small office Wi-Fi networks.

### Man in the middle attack
Once an attacker has the key they can be in the middle of the conversation and pretend to be the other party.
![[Pasted image 20230209123205.png]]

### Asymmetric encryption
Uses two separate but related keys.|
![[Pasted image 20230209123219.png]]
Also known as private/public key encryption, this is used to initiate TLS but is generally slower than symmetric encryption. 

## Digital signatures
In order to verify the integrity of a message, the sender can add a digital signature to a message.
This digital signature is created by encrypting a hash from the unencrypted message using the sender's private key.
The sender can bundle this with the message and encrypt the bundle using the public key
Then when the recipient receives the data they can use their private key to decrypt the bundle, then use the public key to decrypt the signature. If the hashes then match then the integrity of the message is verified.

## Digital certificates
When a sender digitally signs a message, they also send their digital certificate. A trusted company known as a certificate authority provides this. This certificate has:
- A serial number.
- Name of the CA.
- Expiry date.
- Subject (name of the holder).
- Subject's public key.
- CA's digital signature of the certificate to verify the certificate's origin and integrity.
These certificates are used to verify the identity of the owner of each public key and to obtain the key itself. 

## Malicious software

### Worms
A worm is a standalone program that does not require a user to run it in order for it to spread. They exploit vulnerabilities in the destination system and spread automatically.

### Trojans
Trojans are malicious pieces of software that masquerade as something seemingly innocuous or useful. They often serve to open up back doors in your computer to the internet so that the processing power, Internet bandwidth and data can be exploited remotely.

### Phishing
Phishing is using email to manipulate a victim into visiting a fake website and giving away personal information.

### Code quality
Improving code quality, together with monitoring attempts to gain unauthorised access and protection can significantly reduce threats from malware. Two factor auth and protecting against SQL injections are examples of this.

### Monitoring 
Monitoring can protect against the threat of hacking, which can introduce malware. These can also be used to protect against the threat of malware and hacking.

### Protection
Up-to-date patches to the operating system and application programs reduce vulnerabilities in the system.