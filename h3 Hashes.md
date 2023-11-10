# h3 Hashes
#### x) Read and summarize (with some bullet points)

The Protocols are the trust factors behind the transactions. Typically a protocol contains cryptographic algorithm to avoid exploitation, but usually they are used in everyday activities without the users even realizing the protocols behind the actions. In general there are three types of protocols arbitrated, adjucicated and self-enforcing. Arbitrated is a protocol where every transaction is verified by a third party (arbitrator) and adjucicated is where only the unclear transactions are verified by third party (adjucicator). The self-enforcing protocol is as the name says verifying the transactions by itself and no third party arbitrator is required. Self-enforcing protocols are categorized as best types of protocols.

When using the symmetric cryptography the communication is encrypted and can only be opened by a key. All the security is in the key and none in the algorithm. The key must remain secret as long as the communication must remain secret, because if the key is public, anyone can use it to open the message. There is also a public key cryptography where the other key is private and the other public. The public key is used to encrypt the message and private key is used to decrypt the message. In this kind of communication the sender uses the receivers public key and in idealistic world only the legitimate receiver of the message has the private key to open the message.

These technologies are used in multiple different purposes e.g., verifying the digital signature belongs to the legitimate signatory. 

Of course there is also threat factors who try to attack against these kind of security practises with bad intentions. This is why there are also hardened techniques to prevent threat factors replacing your public keys with their public keys. If this would happen the legitimate receiver would send the replaced public key to the sender and without the possibility to dcrypt the message after receiving it. In this case only the threat factor can open the message. To avoid this the public key can be signed by the private key and then the owner of the public key can be verified by using Key Distribution Center. 

##### a)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/2f71ecf1-2775-4aeb-a584-822aab898aea)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/598ee3e2-9e73-4b8c-b5c4-d289436da1d3)

To get sha256 to start with 0 I needed to go to google. I couldn't find any direct instructions, but after I found this: $ echo -n "351" | sha1sum I just tried $ echo -n "351" | sha256sum and there it was

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/c607876a-13dd-4875-aadf-4546f7ba49fe)
Reference: https://stackoverflow.com/questions/3180374/can-an-md5-hash-begin-with-a-zero

