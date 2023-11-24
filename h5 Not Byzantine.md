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

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/652a1619-db6c-462f-a680-f425951370f1)
Running electrum in testnet

### b) Faucet. Get worthless fake money from a testnet Bitcoin faucet.

### c) Giveway. Move money to another Bitcoin wallet. Choose an amount where the last two digists are 42.

### d) Explorer. Use a block explorer to analyze a block on the real Bitcoin blockchain. Explain what each value and field means. You only need to analyze the block information and one sample transaction, as a block can contain many transactions.

### e) Voluntary: Brainiac. Demonstrate how hierarchical deterministic wallet can be regenerated from the bib39 phrase. You can rename the configuration folder to simulate a fresh start. In real life, you would keep the phare away from your computer, but for this simulation, you can copy paste it instead of memorizing.
- 
- 
