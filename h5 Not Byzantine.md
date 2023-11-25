# Assignment h5 Not Byzantine

Reference: Karvinen, T., 2023. Trust to Blockchain 2023 autumn. Link: https://terokarvinen.com/2023/trust-to-blockchain/

### x) Read and summarize (with some bullet points) Nakamoto, S., 2008. Bitcoin: A Peer-to-Peer Electronic Cash System, chapters. Link: https://bitcoin.org/bitcoin.pdf
    1 Introduction
    2 Transactions
    3 Timestamp Server
    4 Proof-of-Work
    5 Network
    6 Incentive
- Bitcoin is created to use cryptographic proof instead of trust and transactions do not require a trusted third party
- It uses peer-to-peer distributed timestamp server to prevent double-spending
- The timestamp server is timestamping a hash of a block of items. It works as a proof that the data has existed at the time stamped
- Each transaction is digitally signed and publicly announced
- Proof-of Work requires a hash that begins with a number of zero bits
- For the timestamp network a nonce in the block are incremented as long as the value starting with required zero bits is found to generate a proof-of-work
- This way the blocks cannot be changed afterwards
- The single block cannot be changed, because it needs to be redone and after it has been attached to the chain all the later blocks would also require to be redone
- Network of nodes are collecting new transactions to blocks
- Incentives are used to keep the bitcoin vivid
- Nodes get incentives from supporting the network
- Transaction fee is incentive for transactions
- Incentive for bad guys with enough CPU power to defraud the blockhain is that they get more new bitcoins by staying honest, because the required CPU power could manage all the new transactions  

### a) Wallet. Create a BitCoin testnet wallet.

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/724b6ce5-3710-44c1-8e69-8b9125e2edb5)
Installing available updates

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/9925c645-e98e-44b7-aa6c-a492f8f33dbd)
Searching for bitcoin related tools

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/f0db4bbf-ac33-446c-879e-803314295dc8)
Installing Electrum

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/652a1619-db6c-462f-a680-f425951370f1)

Running electrum in testnet

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/50a420e5-b202-4f37-9cd4-7b7e7bdde29f)

Part a) completed

### b) Faucet. Get worthless fake money from a testnet Bitcoin faucet.

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/60d980f8-a404-4bc7-a94d-e887edc60d2a)

Copy column --> Address in Electrum Testnet Address tab
![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/c023fbda-b1ea-4166-8aab-be1dda1ab17c)

Enter the address to bitcoin testnet faucet site

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/010c4a13-14b4-4978-ae04-31c3dcb91ddf)

Click Get bitcoins!

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/7f2982cb-3dc4-4b9c-a4cd-59778a6a80c1)

Bitcoins sent to my wallet

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/7681b669-2e3b-4ac5-8d16-7064808b39ce)

Waiting confirmation for the transaction

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/ad326f27-162e-4592-9025-2b8e9a83b47a)

Coins received and the amount is available in my balance

### c) Giveway. Move money to another Bitcoin wallet. Choose an amount where the last two digists are 42.

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/ac7cae12-096f-4b15-8a3b-ce01d828fe8f)

Obtaining Teros Public key from his website

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/a03d1b63-e766-4eef-bcd8-49f927397210)

Sending bitcoins to Tero

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/04068184-37a6-4b16-a80f-a91f9468e81d)

Sending bitcoins to Tero

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/f795cc1c-86f2-499a-bed8-aabbfecfa949)

Payment sent

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/ad42f02e-d56a-480c-bdf9-3cf0da242aef)

Payment is being processed and waiting it to be confirmed

### d) Explorer. Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. You only need to analyze the block information and one sample transaction, as a block can contain many transactions.

I used Blockstream explorer to analyze a block and transaction. (Link: https://blockstream.info/block/0000000000000000000242f76b626811937c51a368a98ece5f845586bd5e66e8?expand) 

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/27ac7384-a110-438d-bc35-c291b57bb136)

The block I am analysing has these values:
Height: 818430
- Height is the number of blocks what have been created before this block (reference: https://www.investopedia.com/terms/b/block-height.asp)
Status: In best chain (1 confirmation)
- Status is the status of the block and in this case it means that the block is verified and it is now part of the blockchain (Reference: https://www.bitcoin.com/get-started/what-is-a-confirmation/)
Timestamp: 2023-11-25 17:15:01 GMT +2
- Timestamp is the exact date and time when the block was created (Reference: https://www.ledger.com/academy/glossary/timestamp)
Size: 1514.459 KB
- Size is the amount of data the block stores (Reference: https://www.bitstamp.net/learn/crypto-101/what-is-block-size/)
Virtual size: 999 vKB
- Virtual size is the transaction's size using segwit's rules (Reference: https://bitcoin.stackexchange.com/questions/89385/is-there-a-difference-between-bytes-and-virtual-bytes-vbytes)
Weight units: 3993.002 KWU
- Weight units are used after the segwit upgrade to measure the size of transactions and blocks (Reference: https://river.com/learn/terms/w/weight-unit/)
Version: 0x2000c004
- Version is the current version of bitcoin and it helps to track changes in the protocol (Reference: https://www.investopedia.com/terms/b/block-header-cryptocurrency.asp)
Merkle root: 01e28bf31f1d32ce364531fbe2dde6a62127842b2718a3166989c2c937bbcc86
- Merkle root is the hash from hashing all the individual transaction hashes (Reference: https://www.investopedia.com/terms/m/merkle-root-cryptocurrency.asp)
Bits: 0x17045a12
- Bits is a 4-byte field indicating the target difficulty (Reference: https://www.gemini.com/cryptopedia/what-is-block-in-blockchain-bitcoin-block-size)
Difficulty: 64678587803496
- Difficulty is the difficulty m,easurement to mine a block (Reference: https://river.com/learn/terms/d/difficulty/)
Nonce: 0xaacd5201
- Nonce is a random number miners try to identify to succesfully mine a new block (Reference: https://www.investopedia.com/terms/n/nonce.asp)

### e) Voluntary: Brainiac. Demonstrate how hierarchical deterministic wallet can be regenerated from the bib39 phrase. You can rename the configuration folder to simulate a fresh start. In real life, you would keep the phare away from your computer, but for this simulation, you can copy paste it instead of memorizing.
- 
- 
