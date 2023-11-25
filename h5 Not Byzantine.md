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

#### Block

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/27ac7384-a110-438d-bc35-c291b57bb136)

Analysis of the block values below:
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

#### Transaction

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/ccc22300-1498-4db3-ae97-95cd0e16869e)

Analysis of the transaction values below:

Witness :35839ed0753c7aa4a93f62eb3989dbb267a71ce3f579e79bf1beff38a367f6cd51e09b12bc1e734a828b56342b6655500e8341f662421d94f17d21305081e630 20f509e58a4e714d04e6cbb74b5f43512ab95542f56bd7fe03c49a5145cb6ebc15ac0063036f7264010118746578742f706c61696e3b636861727365743d7574662d38003b7b2270223a226272632d3230222c226f70223a226d696e74222c227469636b223a2253313038222c22616d74223a2231303030303030303030227d68 c1f01756e67285f5c2aefd17ae7475c0e03a9167c6662e78bb7f1deb08f4ff40ac
- Witness is the proof that the transaction is authentic (Reference: https://livebook.manning.com/concept/bitcoin/witness)
  
nSequence: 0xfffffffd
- nSequence is a parameter added to each input of a transaction (Reference: https://wiki.bitcoinsv.io/index.php/NLocktime_and_nSequence)

Previous output script: OP_PUSHNUM_1 OP_PUSHBYTES_32 40bceafb11a9e6ca748c97d35bc26a5a20c32023cbbb438d5501047004c0ba00 (v1_p2tr)
- Previous output script is the script from the previous transaction (Reference: https://en.bitcoin.it/wiki/Transaction)

Previous output address: bc1pgz7w47c348nv5ayvjlf4hsn2tgsvxgprewa58r24qyz8qpxqhgqqj6l64f
- Previous output address is the address of the previous transaction (Reference: https://en.bitcoin.it/wiki/Transaction)

Type: V1_P2TR
- Type V1_P2TR indicates that the type of the transaction is V1_Pay to Taproot (Reference: https://medium.com/geekculture/understanding-bitcoin-transaction-output-types-with-bigquery-c625643f2ab5)

scriptPubKey (asm): OP_PUSHNUM_1 OP_PUSHBYTES_32 4f2dbd71f9fc69ad3bd2f6988cb6d88d719dd2fce9b6d8792919843f321e4c53
- scriptPubkey is the locking script used to prevent others from spending the output (Reference: https://learnmeabitcoin.com/technical/scriptPubKey)

scriptPubKey (hex): 51204f2dbd71f9fc69ad3bd2f6988cb6d88d719dd2fce9b6d8792919843f321e4c53
- scriptPubkey is the locking script used to prevent others from spending the output (Reference: https://learnmeabitcoin.com/technical/scriptPubKey)

Spending tx: Unspent
- This means that the UTXO hasn't been used as an input in any transaction (Reference: https://help.indodax.com/hc/en-us/articles/4416480885401-What-is-spent-and-unspent-on-the-bitcoin-transaction-)

Type: V0_P2WPKH
- This means that the type is V0_Pay To Witness Script_Hash (Reference: https://medium.com/geekculture/understanding-bitcoin-transaction-output-types-with-bigquery-c625643f2ab5)

scriptPubKey (asm): OP_0 OP_PUSHBYTES_20 ad8ae33a84aaff1b703f8a990a64aec55627f6bb
- scriptPubkey is the locking script used to prevent others from spending the output (Reference: https://learnmeabitcoin.com/technical/scriptPubKey)

scriptPubKey (hex): 0014ad8ae33a84aaff1b703f8a990a64aec55627f6bb
- scriptPubkey is the locking script used to prevent others from spending the output (Reference: https://learnmeabitcoin.com/technical/scriptPubKey)

Spending tx: Unspent
- This means that the UTXO hasn't been used as an input in any transaction (Reference: https://help.indodax.com/hc/en-us/articles/4416480885401-What-is-spent-and-unspent-on-the-bitcoin-transaction-)


### e) Voluntary: Brainiac. Demonstrate how hierarchical deterministic wallet can be regenerated from the bib39 phrase. You can rename the configuration folder to simulate a fresh start. In real life, you would keep the phare away from your computer, but for this simulation, you can copy paste it instead of memorizing.
- 
- 
