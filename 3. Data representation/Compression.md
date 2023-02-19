Data is constantly being moved around computer systems and networks. Transfer is usually high speed and accurate but as distances get longer, transfer is slower and more susceptible to interference and storage space may be limited.
This is why we need compression. Because text image and sound data can be significantly reduced in size. If we do this then data can be sent more quickly, less bandwidth can be used and less storage is required. 

There are two different types of compression:
- Lossy
	Non-essential data is permanently removed ie frequencies of sound outside human hearing.
- Lossless
	Patterns in the data are spotted and summarised in a shorter format without removing any information.

## Lossy compression
Removes data permanently to reduce file size and then gets reconstructed without the missing data. 
![[Pasted image 20221115114425.png]]
Lossy compression removes the sounds in the frequency ranges that we can't so easily hear or that least affect the perceived playback quality. 
![[Pasted image 20221115114521.png]]


## Lossless compression
Lossless compression instead works by recording patterns in the data rather than the data itself.??

### Run length encoding
A basic method of compression that summarises the consecutive patterns of the same data. Works well with image and sound data where data could be repeated many times.
![[Pasted image 20221115114615.png]]

A sound recording could have many thousands of samples taken every second. The same sound or note played for a fraction of a second could result in hundreds of identical samples. ![[Pasted image 20221115114720.png]]

### Dictionary compression
Spots regularly occurring data and stores it separately in a dictionary. The reference to the entry in the dictionary is stored in the main file thereby reducing the original data stored. Even though the dictionary produces additional overheads the space saving negates this problem. 

"No pain no gain" => 0001 1000 1110
| Number | Entry | Binary |
| ------ | ----- | ------ |
| 1      | no_   | 00     |
| 2      | p     | 01     |
| 3      | ain_  | 10     |
| 4      | g     | 11       |


#### Compressing larger volumes
In a text document each letter could be stored as an ASCII code of 8 bits. Each word could be assigned a unique binary code, making every use of the word after the first use require much less memory. 
