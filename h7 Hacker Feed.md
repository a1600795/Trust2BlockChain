### Assignment h7 Hacker Feed. Reference: Karvinen T. 2023. Trust to Blockchain 2023 autumn. Link: https://terokarvinen.com/2023/trust-to-blockchain/

# x) Read/watch and summarize (briefly, e.g. with some bullets)

###Hacker conf. Choose a presentation video in a hacker conference. For example, you can search Youtube for HelSec, Disobey, RSA Conference, Black Hat or have a look at InfoconDB.

#### For hacker conference video I chose Hexacon 2023 - XORtigate: zero-effort, zero-expense, 0-day on Fortinet SSL VPN by Charles Fol

#### Reference: Hexacon 2023. XORtigate: zero-effort, zero-expense, 0-day on Fortinet SSL VPN by Charles Fol Link: https://www.youtube.com/watch?v=7yxTI_4vPGk&list=PLiEHUFG7koLvUe1rnycY33CjQkZfbg-c1&index=11

- Presenter was Charles Fol from France offensive security company called LEXFO
- It was about an exploiment on Fortinet SSL VPN
- They found a bug from the Fortinet software
- Then they could use bruteforce to get a valid key
- After that they used a known method to overwrite a structure named SSL
- Then they could trigger SSL handshake
- The bug needed to be repeated multiple times
- After getting everything done he could use the exploitation and get login details in cleartext from the users who logged in to the VPN
- The next day four domain admins logged in
- Affected products are FortiOS 6.0.0 to 7.2.4 and FortiVPN 1.1.0 to 7.2.3


- Fortigate is known to have lots of bugs, but there wasn't lot of attack surface
- First they took a free demo licence for 2 months
- Then they took the rooth shell
- Then they reversed it
- Target was internet facing SSL VPN interface what allows user to authenticate
- HTTP Server was modified, patched and recompiled old Apache 1.x
- After one week they found a bug
- They could identify the decryption process from the bug
- They could control part of the key from the keystream that generates the first MD%
- Then they applied the bug multiple times
- After applying it enough times they could bruteforce it and get a valid seed
- 
- 
- 
