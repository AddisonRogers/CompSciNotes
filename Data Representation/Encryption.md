A way of making sure data cannot be understood if you don't possess the means to decrypt it. Plain text of a message sent is encrypted using a cipher algorithm and key into equivalent cipher text. When received, the ciphertext is decrypted back to plaintext using the same or different key. 
Two methods to encrypt this plain text are the Caesar cipher and the Vernam cipher.

## The Caesar cipher
The caeser cipher is the most basic type of encryption and the most insecure. Letters of the alphabet are shifted by a consistent amount. 

## Brute force attack
A brute force attack attempts to apply every possible key to decrypt the ciphertext until one works.

## Frequency analysis
Letters are not used equally often. E for example is by far the most common letter. 

## Vernam cipher
The encryption key, also known as the one-time pad, is the only cipher proven to be unbreakable.
The key must be :
- A truly random sequence greater or equal to in length than the plaintext and only ever used once.
- Shared with the recipient by hand, independently of the message and destroyed immediately after use.

## Decoding
Encryption and decryption of the message is performed bit by bit using an exclusive or (XOR) operation with the shared key. 

## The one-time pad
It must be truly random generated from a physical and unpredictable phenomenon. Sources such as atmospheric noise, radioactive decay, the movements of a mouse or the snapshots of a lava lamp. A truly random key will render any frequency analysis useless as it would have a uniform distribution. Computer generated random sequences are not actually random.

## Algorithmic security
Ciphers are based on computational security. If the keys are determined using a computer algorithm then the key derived from an algorithm can be unpicked using an algorithm, given enough ciphertext, computer power and time.