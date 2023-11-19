# h4 pubkey

### x) Read and summarize (with some bullet points)

#### Summary of Schneier, B, 1996. Applied Cryptography: Protocols, Algorithms and Source Code in C. Chapers 2.5-2.8. John Wiley & Sons, Inc. Read: 19.11.2023.

##### 2.5 COMMUNICATIONS USING PUBLIC-KEY CRYPTOGRAPHY

Schneier is explaining the principles, advantages and disadvantages of public-key cryptography. Disadvantages for it are that it is slow compared to symmetric algorithms and it is vulnerable to chosen-plaintext attacks. Advantages it has that it is practical and simple to use e.g., in secured messaging. In secured messaging there are two keys, public and private. The sender has the receivers public key and sender encrypts the message with the public key. The encrypted message can only be decrypted with it's pair private key and the receiver is the only one who has the private key. In this way only the receiver can decrypt the message. To add one more layer of security, it is recommended in this kind of messaging to generate the key pair only for this single messaging and delete the private and public keys after they are not needed anymore.

##### 2.6 DIGITAL SIGNATURES

### a) Pubkey today. Explain how you have used public key cryptography today or yesterday, outside of this homework. In addition to naming the system, identify how different parties use keys in different steps of the system. (Answering this question likely requries finding sources on your own. This subtask does not require tests with a computer.)

Public key cryptography is a common encryption method. For example Hypertext Transfer Protocol Secure or HTTPS is used to secure data transfer between the web browser and website. The encryption protocol for HTTPS is Transport Layer Security (TLS) and it is based on asymmetric public key infrastructure. HTTPS websites have public keys that are available for visitors of the website. The public key encrypts all the data submitted on the website and sent to the web server. The web server has the private key which is used to decrypt received data. It is recommended to use websites only with HTTPS, especially if sensitive information such as credentials is required. HTTPS prevents sniffing and on-path attacks. (Reference: Cloudflare, 2023. What is HTTPS? Link: https://www.cloudflare.com/learning/ssl/what-is-https/. Read: 18.11.2023.)

### b) Messaging. Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. Don't use Tero as a name of any party, unless that's your given name.)

### c) Other tool. Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen.

### d) Eve and Mallory. In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory malliciously modifies the messages. Explain how PGP protects against Mallory and Eve. Be specific what features, which use of keys and which flags in the command are related to this protection. (This subtasks does not require tests with a computer)

### f) Password management. Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)

### g) Refer to sources. Verify each homework report (this and the earlier ones) refers to sources. Every homework report should refer to this task page. It should also have references to any other source used, such as web pages, LLMs, man pages, other reports... References are mandatory, and must be present in every report. (This subtask does not need a report, you can just do it and write "Done." as the answer for this subtask.)

### h) Voluntary, challenging, requires coding: Cryptopals: Challenge Set 1:

    1 Convert hex to base64 (feel free to use a library for base64)
    2 Fixed XOR
    3 Single-byte XOR cipher
    4 Detect single-character XOR (This looks tough before you have solved 1-3)
