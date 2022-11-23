---
banner: "![[Pasted image 20220509155218.png]]"
banner_y: 0.74
---

# Bytes

09/05/2022

> The byte is a unit of digital information that most commonly consists of eight bits. Historically, the byte was the number of bits used to encode a single character of text in a computer and for this reason it is the smallest addressable unit of memory in many computer architectures. To disambiguate arbitrarily sized **Bytes** from the common 8-bit definition, network protocol documents such as The Internet Protocol (RFC 791) refer to an 8-bit byte as an octet. Those bits in an octet are usually counted with numbering from 0 to 7 or 7 to 0 depending on the bit endianness. The first bit is number 0, making the eighth bit number 7.
> [Wikipedia](https://en.wikipedia.org/wiki/Byte)

## Electricity

A computer is an electrical device. Surprise.
Everything is written in base 2, with either a 1 or a 0 being accepted as a valid data form.
It is either 1 or 0 because electricity is either ON or OFF.
Each individual digit in a binary value is referred to as a bit.

> [!NOTE] Algebra
> For n bits a computer can produce $2^n$ different combinations of values

## Larger Values

As the binary value gets larger more bits are required to store the number. A group of 8 bits is a byte.
Two or more bytes can be grouped together to hold larger values.

> [!seealso] Nibble / Nybble / Nyble / Nybl
> A 4 bit group that is less commonly used in the modern day apart from it’s use in networking.

![[Pasted image 20220509164854.png]]`center`

![[Pasted image 20220509164908.png]]`center`

# Representing Text Characters

If a computer only understands 1s and 0s, what happens when we need to enter text?

## ASCII

> **ASCII** ( (listen) ASS-kee),: 6  abbreviated from American Standard Code for Information Interchange, is a character encoding standard for electronic communication. ASCII codes represent text in computers, telecommunications equipment, and other devices. Most modern character-encoding schemes are based on ASCII, although they support many additional characters.
> [Wikipedia](https://en.wikipedia.org/wiki/ASCII)

Every character on the keyboard is represented by a binary value. Uppercase letters have different values than lowercase symbols. Punctuation and space etc have their own character.
> [!note] Bit length
> Only used 7 bits as well making it extremely efficient for sending and storing data. It could also use the final bit as a parity bit for error checking.

However because 7 bits isn’t enough for any language other than English so Unicode is generally used.

## Unicode

> **unicode**, formally the Unicode Standard, is an information technology standard for the consistent encoding, representation, and handling of text expressed in most of the world's writing systems. The standard, which is maintained by the Unicode Consortium, defines 144,697 characters covering 159 modern and historic scripts, as well as symbols, emoji, and non-visual control and formatting codes.
> Unicode's success at unifying character sets has led to its widespread and predominant use in the internationalization and localization of computer software. The standard has been implemented in many recent technologies, including modern operating systems, XML, and most modern programming languages.
> [Wikipedia](https://en.wikipedia.org/wiki/Unicode)

The Unicode system was introduced to standardise the encoding of characters from all languages, using either 16 or 32 bit lengths and it is cross compatible with the ASCII code as the first 128 Unicode characters are the same ASCII ones.

# Error Checking

When data is transmitted there may be electrical interference, power surges, synchronisation issues and or wear and tear on the cable transmitting it. This means that errors may occur that can cause bits to shift from 1s to 0s or 0s to 1.
In order to check if there has been an error in transmission you can use a few methods:
- [[Bytes, ASCII, UNICODE, Error Checking.#Parity bits|Parity bits]]
- [[##Majority voting|Majority voting]]
- [[##Check digits|Check digits]]
- [[##Checksums|Checksums]].

## Parity Bits

A parity bit is a bit in the byte that makes the total sum of the binary odd or even depending on the machine.
So when data is transmitted and the sum of all bits are wrong then the receiving computer notifies the sender for data to be resent.

## Majority Voting

Each byte is sent 3 times then once received all three bytes, the computer compares them bit by bit in order to resolve one byte that has the correct bit the majority of the time.

## Check Digits

A check digit is additional digit at the end of a string of other numbers designed to check for mistakes in input or transmission. MODULO 10 system.

## Checksums

A checksum works in a similar way to a check digit. With all of the digits added into a sum, if the sum is what is expected by the receiver then the data is accepted otherwise it will signal it is wrong.


#compsci #datascience
