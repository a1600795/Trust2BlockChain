# Assignment h6 Iceberg

Reference: Karvinen, T., 2023. Trust to Blockchain 2023 autumn Link: https://terokarvinen.com/2023/trust-to-blockchain/

### x) Read and summarize (briefly, e.g. with some bullets)

Shavers & Bair 2016: Hiding Behind the Keyboard: The Tor Browser €; subchapters: "Introduction", "History and Intended Use of The Onion Router", "How The Onion Router Works", "Tracking Criminals Using TOR".

-  Tor is a modified version of Mozilla  Firefox browser
-  It hides the user's IP address
-  Hiding the IP makes the user activities anonymous
-  It is easy to use and free to download
-  It was originaly created by US government in 2002, but it is not controlled by them
-  US government is now actively researching methods to deanonymize Tor users
-  The anonymity allows e.g., whistleblowers to communicate anonymously with authorities
-  But the anonymity also allows criminals to operate anonymously
-  The anonymity of Tor is nearly impossible to beat
-  If getting access to machine where Tor has been installed it is possible to do forensic work and find some traces of online activity

Quintin 2014: 7 Things You Should Know About Tor

- The cryptography of Tor has not been broken
- Browser bugs or misconfigurations can be used to trace users
- Tor is not only used by criminals
- Tor has no backdoor
- Tor download is pre-configured for privacy and it is easy to use

### a) Install TOR browser and access TOR network (.onion addresses). (Explain in detail how you installed it, and how you got access to TOR).

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/f1b26d8a-e817-479f-9edb-aa684fb7e380)

Installing Tor browser for Windowsfrom torproject.org the Tor Project website

### b) Browse TOR network, find, take screenshots and comment

    search engine for onion sites
    marketplace
    fraud
    forum
    a well known organization



### c) In your own words, how does anonymity work in TOR? (e.g. how does it use: public keys, encryption, what algorithms? This subtask does not require tests with a computer.) Reference: Wherry, J., 2023. What is Tor and how does it work? Link: https://cybernews.com/privacy/what-is-tor-and-how-does-it-work/

Tor what is also known as the onion router is anonymous as long the user is surfing inside Tor. This means that the user has to use only .onion domains. These domains are going through the onion router. Onion router is connecting through multiple random relay servers. All the requests are encrypted between the relays and the current relay server only knows the previous relay and the next, but not the whole connection chain. This is where the anonymity of Tor is based. When connecting to website outside .onion domains the traffic from the exit node to destination is unencrypted, so it is possible to monitor all the traffic from the exit nodes to normal internet. The term dark web is referring to .onion domains 

### d) What kind of the threat models could TOR fit? (This subtask does not require tests with a computer.) Reference: Mathews, Sirinam & Wright, 2018. UNDERSTANDING FEATURE DISCOVERY IN WEBSITE FINGERPRINTING ATTACKS. Link: https://www.researchgate.net/publication/329743510_UNDERSTANDING_FEATURE_DISCOVERY_IN_WEBSITE_FINGERPRINTING_ATTACKS#pf1

Tor browser is vulnerable to fingerprinting attacks. Website fingerprinting attack is possible in Tor by eavesdropping the connection between the user and the first Tor node.This can be performed in various ways, e.g., wireless link, compromised cable modem or the user's internet service provider. The content is encrypted but the attacker can monitor the patterns and timing of the network packages. This might be enough to expose the user's activities and eliminate the privacy protection of Tor.

To prevent this kind of attacks Tor can try to manipulate the traffic patterns by adding fake packets or delaying real packets. The problem with this is the requirement of the network bandwit. This will slower down the speed of the browsing.
