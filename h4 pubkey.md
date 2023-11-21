# Assignment h4 pubkey 
#### Reference: Karvinen, T., 2023. Trust to Blockchain 2023 autumn. Link: https://terokarvinen.com/2023/trust-to-blockchain/.

## x) Read and summarize (with some bullet points)

### Summary of Schneier, B, 1996. Applied Cryptography: Protocols, Algorithms and Source Code in C. Chapers 2.5-2.8. John Wiley & Sons, Inc. Read: 19.11.2023.

#### 2.5 COMMUNICATIONS USING PUBLIC-KEY CRYPTOGRAPHY

Schneier is explaining the principles, advantages and disadvantages of public-key cryptography. Disadvantages for it are that it is slow compared to symmetric algorithms and it is vulnerable to chosen-plaintext attacks. Advantages it has that it is practical and simple to use e.g., in secured messaging. In secured messaging there are two keys, public and private. The sender has the receivers public key and sender encrypts the message with the public key. The encrypted message can only be decrypted with it's pair private key and the receiver is the only one who has the private key. In this way only the receiver can decrypt the message. To add one more layer of security, it is recommended in this kind of messaging to generate the key pair only for this single messaging and delete the private and public keys after they are not needed anymore.

#### 2.6 DIGITAL SIGNATURES

There are different models for digital signatures. Documents can be signed wih Symmetric Cryptosystems and an arbitrator. In this model a trusted arbitrator is used in the middle and the arbitrator verifies all the messages from the participants are legit. This is very powerful digital and basically unforgeable signing. The only problem with these is that it is very time-consuming to arbitrator as everything goes through him. 

One other model is signing documents with public-key cryptography. This works pretty much in same way as in messaging, that was explained in previous chapter. With digital signing the key pair is used for signature. First the other party sends public key to the other one and then signs the document using his own private key. After signing it the documet is sent to other party and it can be opened and signed with the public key sent earlier. No one else can decrypt the document than the legit party as the the correct key pair is required.

Also documents can be signed using public-key cryptography and one way hash functions. In this model there is only a certain hash that is signed instead of the whole document. Otherwise it works in a similar way as signing with public-key cryptography where the correct key pair is required for signing process. This is much faster than signing the whole document as in public-key cryptography.

#### 2.7 DIGITAL SIGNATURES WITH ENCRYPTION

The best practise is to sign the document before encrypting. This has couple of key points. Encryption before signing migh cause legal dispute as the the text to be signed is not visible when signing and there are also cryptanalytic attacks against this technique. It is also recommended to use different key pair for signature and encryption of the document. This way the document encryption key can be provided e.g., to police without revealing also the signature key. Timestamps for signature are also a mandatory as it prevent the reuse of the signed document.

#### 2.8 RANDOM AND PSEUDO-RANDOM-SEQUENCE GENERATION

Random-number generators have lots of issues. The main problem is that the result is not random as purely random sequences are impossible to generate on a computer and if you run the same input again it generates the same result every time. Then there are also pseudo-random-sequence generator. These are better, but only when the sequence period is long enough and the whole length is actually used. This means that if a sequence of million is required the generator has to generate the whole length and not e.g., sixteen thousand and after sixteen thousand it repeats the next sixteen thousand as long as the end result is million. 

To classify a random sequence to real random sequence the result cannot be reliably reproduced. When same input is entered multiple times it doesn't generate same result. The results will be random sequences with no correlation.

### Summary of Rosenbaum, K. 2019. Grokking Bitcoin. Manning Publications. Chapter 2. Cryptographic hash functions and digital signatures. Read: 19.11.2023.

#### Chapter 2. Cryptographic hash functions and digital signatures

Cryptographic hashes are the cornerstone of Bitcoin and key element to understand Bitcoin's functionalities. Cryptographic has work as a fingerprint for digital information and the one Bitcoin most commonly uses is Secure Hash Algorithm with 256-bit output or SHA256. SHA256 can be used to validate changes for example, as the same data will always produce same hash. If you have data you can generate a hash from it and after the data is changed you can generate a new hash from it and the hash will be different from the previous one. SHA256 is nearly impossible to calculate, because it has possible solution 10 to the power of 77.

Digital signatures are used to verify that the receiver actually receives what the legit sender sent. This is done with matching key pair where is a private and public keys. The private key is used for digital signature and the public key can be used to validate the signature. This is a one-way process where the public key is generated from the private key, but the private key cannot be generated from the public key. This is the most important security layer with digital signatures.

There are two ways to use the key pair. Both keys can be used to encrypt or decrypt depending on the purpose. If the private key is used for decryption the communication is private and no one else can decrypt it. When public key is used for decryption communication is not secret as everyone with the public key can decrypt the message. Public key is the method used in digital signatures and it is also the method Bitcoin uses to verify payments.

The security of the private keys are full responsibility of the owner and if someone manages to copy it and use your private key to fraudulent activities and the possible fraudulent transfer aren't reversed. There are many ways to keep the private key safe. The most efficient ways are to keep private key on an offline computer so any viruses or other online attacks aren't possible. Then it is good to keep the private key encrypted instead of clear text and split the key on multiple different machines so attackker would need to get access to all the different machines in stead of one.

#### Summary of Karvinen, T. 2023. PGP - Send Encrypted and Signed Message - gpg. Link: https://terokarvinen.com/2023/pgp-encrypt-sign-verify/. Read 19.11.2023.

Tero's article is about generating a key pair and demonstrating it with two imaginary personalities. The article also contains a detailed description to generate a message, encrypt the message, digitally sign the message, send the message and decrypt the message.

### a) Pubkey today. Explain how you have used public key cryptography today or yesterday, outside of this homework. In addition to naming the system, identify how different parties use keys in different steps of the system. (Answering this question likely requries finding sources on your own. This subtask does not require tests with a computer.)

Public key cryptography is a common encryption method. For example Hypertext Transfer Protocol Secure or HTTPS is used to secure data transfer between the web browser and website. The encryption protocol for HTTPS is Transport Layer Security (TLS) and it is based on asymmetric public key infrastructure. HTTPS websites have public keys that are available for visitors of the website. The public key encrypts all the data submitted on the website and sent to the web server. The web server has the private key which is used to decrypt received data. It is recommended to use websites only with HTTPS, especially if sensitive information such as credentials is required. HTTPS prevents sniffing and on-path attacks. (Reference: Cloudflare, 2023. What is HTTPS? Link: https://www.cloudflare.com/learning/ssl/what-is-https/. Read: 18.11.2023.)
### b) Messaging. Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. Don't use Tero as a name of any party, unless that's your given name.)

Creating directories for my imaginary persons Pedro and Alice for their secret messaging

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/5bf4fb92-bc43-458e-aa06-cefe08e87bb7)

Generating key to Pedro

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/5e67d3e5-897c-4c75-aadc-bb2dec383402)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/77e59f18-2dcd-4ab5-bdb5-0ad004f6cf6c)

Exporting Pedro's key

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/edb90bda-2d8c-4f10-ad63-5aaa4a5ca6be)

Generating key to Alice

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/d22bb236-cfe4-498c-bf5a-242829c6d795)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/03d3d98d-f456-413b-8829-cb709800749b)

Alice import and sign Pedro's public key

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/46e8fb18-b881-4a29-bee7-6a3e3dd2bf5a)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/4089b68f-fae1-48e9-b5aa-bcd71e3b1432)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/7f93772c-d204-4bdc-bac6-9d5b9a1feeca)

Pedro import and sign Alice's public key

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/8ba10a83-12b4-4d85-8c11-7ca010ea8c8d)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/9e7006fe-b8dd-457c-b8d8-c278d0254831)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/604cf136-4ff5-4dca-b004-e6d41cb4318a)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/a316a4dd-1278-41a4-b62b-fb347344b946)

For some reason I cannot sign it in Pedro's directory, but managed to do it in root directory and trust between both parties is established

Alice encypt and send a secret message

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/68b68d76-da37-4647-b0ee-0b33c727682f)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/4b699ad7-d209-4129-b95b-9db21a8f3f2d)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/911d656b-4dfa-4710-b95f-ece77b557fac)

Pedro decrypts and verifies the message

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/da44739b-8309-4bbd-a1d5-378231313305)

### c) Other tool. Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen.

I used ccencrypt to encrypt and decrypt a message.

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/529fd570-cee3-4cbc-b750-be70c19e599c)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/7fc6b6ac-a3e0-42ac-bade-c2f4ccd7c281)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/19271280-f4fb-465b-a72a-5e8e5da2eefc)

After encryption I tried to open the file, but it only showed me blackscreen as seen below.

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/6b5a909e-849b-4713-8b88-a4a14e0f4b03)

Strange thing was, that it allowed me to open the fiel, as usually they ask the password at this point, but this didn't ask. Only after the separate decryption I could open it normally. As seen below.

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/308f53ef-3c97-4898-ba55-c119f15e906d)

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/1df12ad5-2614-475e-a5c0-eb9a424fcc95)

For this part of the assignment I used reference: Tecmint, 2023. 7 Tools to Encrypt/Decrypt and Password Protect Files in Linux. Link: https://www.tecmint.com/linux-password-protect-files-with-encryption/. Read. 21.11.2023.

I wasn't so impressed with this tool. It propably has other functionalities as well and might be a lot more useful, but I just ain't aware of that. For me it was just a tool to make files password protected. Compared to PGP, I couldn't use keypairs and sign to encrypt and verify the message. Just only a password. So would value PGP lot more secure than ccencrypt.

### d) Eve and Mallory. In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory malliciously modifies the messages. Explain how PGP protects against Mallory and Eve. Be specific what features, which use of keys and which flags in the command are related to this protection. (This subtasks does not require tests with a computer)

Encrypting the message makes it impossible to read it even if it is sent through open internet. Also signing it verifies that the message is really sent by the legit sender and nobody has modified it. With public and private keypairs it is also ensured that the message is coming from the trusted keypair, because otherwise it cannot be opened.

### f) Password management. Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)

Login to Haaga-Helia Citrix

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/62c98a36-ad44-40fa-af19-5592964b08df)

I saved the password to keypass, but it doesn't allow me to take screenshots, so unfortunately I cannot share my experience with pictures. But to keep it short, it generates and stores passwords for me, so I can use them in various websites. This way I only have to remember one password to keypass instead of all passwords for websites. People are lazy and for this reason many use same password to different services, but with password manager it is easy to use always different password to different services and all you need to remember is the one password for the password manager.

This prevents attacks with one leaked userid and password to different services using the same credentials and just randomly testing them everywhere. Also with password manager it is easy to generate complex password what cannot be cracked so easily with tools like Hashcat.

### g) Refer to sources. Verify each homework report (this and the earlier ones) refers to sources. Every homework report should refer to this task page. It should also have references to any other source used, such as web pages, LLMs, man pages, other reports... References are mandatory, and must be present in every report. (This subtask does not need a report, you can just do it and write "Done." as the answer for this subtask.)

Done.

### h) Voluntary, challenging, requires coding: Cryptopals: Challenge Set 1:

    1 Convert hex to base64 (feel free to use a library for base64)
    2 Fixed XOR
    3 Single-byte XOR cipher
    4 Detect single-character XOR (This looks tough before you have solved 1-3)
