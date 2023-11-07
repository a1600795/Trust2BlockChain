# h2 Crown Jewels and Bad Guys

x) Summarize Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains.

### Summarization

The white-paper is about computer network threats and defence mechanism. It highlights Advanced Persistent Threats or APT. APT is a threat where bad guys are patient and wait for long tme about the correct time to attack. This method different from traditional viruses and worms, what makes it more difficult to mitigate the risks of APTs with current technologies and processes. These toolset are based on the principle that the response should happen after the point of compromise and the compromise was the result of a fixable flaw. This isn't the way APT works, as it can take significantly long time after the intruder finally attacks. (Hutchin, Cloppert and Amin, 2011, 1-2.)

As far as I know the APTs are difficult to defect. They typically happen after human mistake and after that they get unauthorized access to system or server they can wait there very long time and monitor all the traffic. After they have collected enough information they attack. This can happen in various ways, they can send false emails, prevent access to servers or steal critical business data etc. For example this is one of the reason why organizations should have efficient password policies in use. 

Quick responces to prevent APTs are required. The white paper is focused on creating an effective methods to mitigate the risks of APTs. This can be done by using kill chain analysis where the whole incident is analysed from the beginning to the end and this is used as intelligence information. This information can then be used for investments in new technologies or processes for defenders of the APTs. (Hutchin, Cloppert and Amin, 2011, 2.)

In the text is described related work on phase based models of defense and countermeasure strategy and an intelligence-driven computer network defense model (CND). Also it shows an  real case study of CND. (Hutchin, Cloppert and Amin, 2011, 2.)

The paper identifies the CND as an important part in the fight against APTs. To create resilience against these threats requires understanding them. After understanding them it is possible to create defensive mechanism against them. Analysing the kill chain shows if the attackers have for example repeating patterns and after identifying certain compnents of the attacks it is possible for defenders to reduce the gaps. This lowers the chance of success with intrusion attempts. After imbalancing the situation by showing information superiority against threat factors it gives advantage for defenders over the attackers. This gives defenders a vantage and it mitigates the risks of APTs. (Hutchin, Cloppert and Amin, 2011, 12.)

I am not an security expert and for me it is difficult to say how valid the white paper is, as it is 12 years old. But to speak generally, I say that the knowledge is power and the more you understand these kind of attackers, the more capable you are to prevent these attempts. Kill chain is propably still an efficient tool to analyse APTs. Like said before I am not an expert of this topic, but I am pretty sure APTs are still today a serious threat. The paper mentioned that these attackers are flexible and evolve all the time. This means they invent all the time new methods to for their attacks and this requires evolving methods for responses.  

## References

Hutchin, E., Cloppert, M., and Amin, R., 2011. Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains. Link: https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf. Read: 6.11.2023

### a) Make-belief boogie-man. Create a treath model for imaginary company

My imaginary company is a pharmaceutical drug lab that creates new medicines. The key assets for this company are the drugs that are currently under development. They are just going to have a breakthrough on a drug that cures lymphona. Based on the test results the drug has worked for 99 percent of the cases and they are preparing to release it after 10 months. The development of the new drug has taken 11 years. It would be catastrophic if the chemistry and preparation process would leak out.

#### Threat modeling (Reference: Karvinen, T., 2023. Trust to Blockchain 2023 autumn / h2 Crown Jewels and Bad Guys. Link: https://terokarvinen.com/2023/trust-to-blockchain/. Read 7.11.2023

1) What are we working on:
   - Our Assets
      + Pharmaceutical drug development and research
   -  Security supports business
      + This is a small pharmaceutical drug lab and all of it's IT services are outsourced
   - Diagram of the company systems below
     
   ![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/72a0429d-ffc1-425a-8c25-c1937a024c5b)

   - Description of the diagram
     + All the systems in use are accessed through public internet and they have Azure AD multi factor authentication.
     + The servers are located in the outsourcing partners datacenter
     + Traffic to and from the environment goes through firewall and loadbalancer
     + All the servers are antivirus protected
     + System A is the research management system and all the crown yewels are in system A
     + Security patching is done regularly
     + Servers os is always on supported version

2) What can go wrong
   - Bad guys want to get access to the data of the almost finished research project where the cure for lymphona is discovered
   - Attack tree (Reference: Schneier, B., 1999. Schneier on Security. Link: https://www.schneier.com/academic/archives/1999/12/attack_trees.html. Read: 7.11.2023.

![image](https://github.com/a1600795/Trust2BlockChain/assets/149095048/edb7beca-8e0c-4ea0-85b3-66e476c2431d)

   - Biggest risks are that the threat actor gets access to the database or to the database server
      + Expected value = 2 x 1 000 000 000 = 2 000 000 000
      + Monetary value is very high. 11 years of work and the drug companies are constantly contacting them as they want to make a contract with them
          - Monetary value is one billion
          - Probability is two on the scale from 1-3
   - They are targeted all the time by different threat actors
      + Cyber criminals are using known TTPs (Reference: Exabeam, 2023. What Are TTPs and How Understanding Them Can Help Prevent the Next Incident. Link: https://www.exabeam.com/explainers/mitre-attck/what-are-ttps-and-how-understanding-them-can-help-prevent-the-next-incident/. Read: 7.11.2023.
         - They try to gain unauthorized access by findin a backdoor (Tactical)
         - They try to compromise the website the application is hosted (Tactical)
         - They try to find a way for SQL injection (Technical)
         - They have scanned the website of the application for backdoors and SQL injections (Procedure)
   - What are we going to do about it
      + Reducing the attack surface and limiting
         - IP restriction for the website of the application
            + Access only from the intranet of the research lab or remotely from home through VPN
         - Traffic between the webserver and database server only in private intranet of the datacenter
   - Did we do a good job
      + Preventing public access to the website has reduced attacks
      + Regular security audits has has reduced the gaps in processes and policies
      + Pentest has identified loopholes in the application and they have been corrected
   - Bad guys get access to one of the researchers personal email and they found out he is participating in remarkable research project
   - After monitoring his personal email the researcher send an email from his work email account to his personal email account
   - After this the bad guys target his work email account and after a while they get access in to it
   - After monitoring his work email account they found out what this remarkable project is and that it is most likely going to be succesful
   - After this they research what is the company offering them IT services
   - After this they attack the companys datacenter
   - After this they wait long enough to get the user id and password for an admin account leveled up enough, so they can get admin access to the database servers
   - After this they copy all the data from the research management system and lock the database server with a password
   - Then the blackmailing begins





