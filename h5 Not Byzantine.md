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
- 
- 
- 
- 
