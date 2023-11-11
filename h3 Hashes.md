# h3 Hashes
#### x) Read and summarize (with some bullet points)

The Protocols are the trust factors behind the transactions. Typically a protocol contains cryptographic algorithm to avoid exploitation, but usually they are used in everyday activities without the users even realizing the protocols behind the actions. In general there are three types of protocols arbitrated, adjucicated and self-enforcing. Arbitrated is a protocol where every transaction is verified by a third party (arbitrator) and adjucicated is where only the unclear transactions are verified by third party (adjucicator). The self-enforcing protocol is as the name says verifying the transactions by itself and no third party arbitrator is required. Self-enforcing protocols are categorized as best types of protocols.

When using the symmetric cryptography the communication is encrypted and can only be opened by a key. All the security is in the key and none in the algorithm. The key must remain secret as long as the communication must remain secret, because if the key is public, anyone can use it to open the message. There is also a public key cryptography where the other key is private and the other public. The public key is used to encrypt the message and private key is used to decrypt the message. In this kind of communication the sender uses the receivers public key and in idealistic world only the legitimate receiver of the message has the private key to open the message.

These technologies are used in multiple different purposes e.g., verifying the digital signature belongs to the legitimate signatory. 

Of course there is also threat factors who try to attack against these kind of security practises with bad intentions. This is why there are also hardened techniques to prevent threat factors replacing your public keys with their public keys. If this would happen the legitimate receiver would send the replaced public key to the sender and without the possibility to dcrypt the message after receiving it. In this case only the threat factor can open the message. To avoid this the public key can be signed by the private key and then the owner of the public key can be verified by using Key Distribution Center. 

##### a) Billion dollar busywork

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/2f71ecf1-2775-4aeb-a584-822aab898aea)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/598ee3e2-9e73-4b8c-b5c4-d289436da1d3)

To get sha256 to start with 0 I needed to go to google. I couldn't find any direct instructions, but after I found this: $ echo -n "351" | sha1sum I just tried $ echo -n "351" | sha256sum and there it was

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/c607876a-13dd-4875-aadf-4546f7ba49fe)
Reference: https://stackoverflow.com/questions/3180374/can-an-md5-hash-begin-with-a-zero

#### b) Compare hash. Create a small text file. Take it's hash (e.g. 'sha256sum tero.txt'). Change one letter. Take the hash again. Compare hashes. What do you notice?

Hash changes
![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/73ff9dcc-c0d5-4943-9d52-9a97e44909e6)

#### c) Install hashcat and test that it works.

Installed before started these in chapter x)

#### d) Crack this hash: 21232f297a57a5a743894a0e4a801fc3

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/c3044481-e778-4961-a936-bd61bc71c9ff)

Trying with MD5

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/35369d8d-ebae-4f0c-b4e4-de140ae7a502)

e) Try cracking this hash and comment on your hash rate $2y$18$axMtQ4N8j/NQVItQJed9uORfsUK667RAWfycwFMtDBD6zAo1Se2eu . This subtask d does not require actually cracking the hash, just trying it and commenting on the hash rate.

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/afed2de7-81c9-428a-8054-bdcd494970e4)
![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/5573880f-2518-4030-91cb-4822b25c7d27)
![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/267035f4-1e0c-447a-9bc0-1deb5b10ce6e)

Time estimated 7 years, 258 days

#### n) Voluntary bonus: create some hashes of your own, then crack them with hashcat.

Generating a SHA-256 hash from the Linux command line (Reference: https://stackoverflow.com/questions/3358420/generating-a-sha-256-hash-from-the-linux-command-line)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/162e7c92-64aa-4da1-8412-5aec6566850f)
![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/4a3ea467-ae00-4a92-85f0-5d26a2a5160b)
![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/dd89ee94-cef7-4976-a4b0-ab784b423582)



 
