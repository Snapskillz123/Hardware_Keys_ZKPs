# ZKPs
  ## Definition
  A Zero-Knowledge Proof (ZKP) is a cryptographic method that allows one party (the prover) to prove to another (the verifier) that they know a specific piece of information without revealing the information itself.
  It ensures privacy while still verifying the truth of a statement.
  ## Simple Examples
  ### Cave example
  Two friends,say Mario and Luigi, go out for a trek and find an intriguing cave with two paths(A and B) that connect to each other with a door present where the paths meet. This door has a secret password where if you whisper the magic words,it opens.
  Luigi wants to prove that he knows the password without actually telling Mario the password.

  ![image](https://github.com/user-attachments/assets/121fb001-888c-4dce-84d7-61e8deb9ffed)

  While Mario is outside the cave, Luigi goes inside and picks either path A or B to enter the cave. Mario doesn't know which path Luigi has picked as he was outside.
  
  Now Mario shouts from outside and tells Luigi to come out of a path (Let's say A). Luigi comes out of path A. Luigi could have anyways entered though A so Mario is still unsaure whether luigi actually knows the passwords or not.
  So without looking, Mario tells Luigi to enter a path again randomly and come out of a path that Mario shouts, and obviously Luigi comes out of this path. Mario is in disbelief and keeps telling Luigi to repeat the process.

  After a point the chance that Luigi doesn't know the password and is getting lucky with his choice is very low. So now Mario is convinced that Luigi knows the password, but Luigi hasn't told him what the password actually is.

  ### Pen Example
  We have two friends playing a game with pens, say Alice and Bob.
  Alice is colourblind and has 2 pens of colours red and blue in her handand to her the pens are identical. Bob tells her to either swap the pens behind her back or not and Bob will guess what she has done.

  Bob wants to prove that he knows the colours of the pen without actually telling Alice which pen is which colour.
  
  Bob can clearly see whether she has switched the pens or not but alice cannot verify it for sure whether he guessed or he knows because she is colourblind. So Alice puts the pens behind her back again and repeats the process.
  
  If Bob guess her action again she'd become more certain that he knows the colour of the pens even though she doesn't actually know the colour of the pens.
  ## Three Main Properties of ZKP:
  ### Completeness
  If the statement is true, an honest prover can convince an honest verifier.
  ### Soundness
  If the statement is false, no dishonest prover can convince the verifier that it’s true (except with a tiny probability).
  ### Zero-Knowledge
  If the statement is true, the verifier learns nothing other than that it is true (i.e., no additional information is revealed).
  
  ## Applications
  ### Crypto x Blockchain
  Private Transactions: ZKPs enable private transactions in cryptocurrencies. For example, in Zcash, zk-SNARKs allow users to prove they have enough funds and authorize a transaction without revealing details like the sender, receiver, or amount.
  
  Blockchain Scalability: zk-SNARKs and zk-STARKs help improve blockchain scalability by enabling off-chain computation verifications and minimizing on-chain data.
  
  Decentralized Identity: ZKPs allow users to prove their identity or credentials without revealing sensitive information. Projects like Sovrin use ZKPs for decentralized identity management.
  ### Crypto x File Forensics
  Proof of Data Ownership: In decentralized storage solutions (like IPFS or Storj), ZKPs can be used to prove ownership of files or access to data without revealing the data itself. This is helpful in securing data transfers or sharing files over the web in a private and efficient way.
  
  Proof of Retrievability: ZKPs can verify that a file stored on a server is retrievable (intact and uncorrupted) without requiring the client to download the entire file. This ensures data availability in cloud storage or distributed systems.
  ### Crypto x Web
  Security Testing: In web security testing (e.g., pentesting), ZKPs could allow testers to prove that they have tested certain parts of the system (e.g., specific vulnerabilities or attack vectors) without disclosing how they performed the tests or which parts of the system are involved. This is useful in ethical hacking when the details of the network or application should remain private.
  
  Proofs of Exploit Resistance: Web applications or APIs can use ZKPs to demonstrate that they are not vulnerable to common exploits (like buffer overflows, privilege escalations, etc.) without revealing their codebase or internal configurations.
  
  Mitigating Man-in-the-Middle (MITM) Attacks: ZKPs can help verify that a server is communicating with the correct client or that a connection has not been intercepted by an attacker, without revealing sensitive session or credential data. This could strengthen protections in SSL/TLS setups or ensure that certificates and encryption keys have not been tampered with.
  
  Proving Data Provenance: Web services could use ZKPs to prove the origin and authenticity of data or software updates to clients without revealing internal logs or infrastructure details. This is particularly helpful for preventing supply chain attacks or verifying data on content distribution platforms.
  ### Crypto x Networking
  Distributed VPNs or Mixnets: In privacy-preserving network protocols (such as VPNs or mixnets), ZKPs can be used to prove that a server or node is forwarding traffic correctly without exposing details about the network’s structure or traffic patterns. This helps maintain privacy and security in decentralized networks.
  
  Blockchain-Based Networks: ZKPs are already used in some blockchain-based network protocols to secure and privatize communications. For instance, users could send private messages or participate in decentralized voting without revealing their identity or other private data, while still ensuring the integrity of the process.

## Types of ZKPs
### Interactive Zero-Knowledge Proofs (IZKPs)
In this type, the prover and verifier need to interact with each other through multiple rounds of communication. The verifier sends random challenges, and the prover responds to these challenges. Over time, the verifier becomes convinced of the prover's knowledge without learning the secret itself.

Example: The colorblind pen analogy, where the prover and verifier repeatedly interact to show the pens are different colors without revealing the actual colors.
Key Characteristics:
Requires multiple rounds of communication.
Security relies on the randomness of the verifier’s challenges.
Used in theoretical contexts or specific cryptographic protocols where interactivity is acceptable.
### Non-Interactive Zero-Knowledge Proofs (NIZKPs)
Here, the prover can generate a proof that the verifier can check later without any interaction. This is done by replacing the verifier's random challenges with a cryptographic hash (as seen in the Fiat-Shamir heuristic).

Example: zk-SNARKs (Succinct Non-interactive Arguments of Knowledge) used in blockchain.
Key Characteristics:
No interaction required between prover and verifier.
The prover generates the proof once, and the verifier can check it anytime.
Ideal for distributed systems, blockchain, and public verifications.
### zk-SNARKs (Zero-Knowledge Succinct Non-Interactive Arguments of Knowledge)
zk-SNARKs are a specific type of Non-Interactive ZKP that are designed to be both succinct (small in size) and efficient to verify. These are widely used in cryptocurrencies, like Zcash, to enable privacy-preserving transactions.

#### Key Characteristics:
Succinct: The proof is very small and can be quickly verified.
Non-Interactive: Requires no back-and-forth communication.
Knowledge Argument: The prover can convince the verifier that they know a solution without revealing the details.
Use Cases:
Blockchain: zk-SNARKs are used for privacy in cryptocurrencies.
Verification: Used for verifying large computations in a short time.
### zk-STARKs (Zero-Knowledge Scalable Transparent Arguments of Knowledge)
zk-STARKs are another type of Non-Interactive ZKP, similar to zk-SNARKs, but with some improvements in terms of scalability and transparency.

Scalable: They can handle larger computations more efficiently than zk-SNARKs.
Transparent: They don’t require a trusted setup phase (which zk-SNARKs typically do).
### Key Characteristics:
Scalability: Better suited for large computations.
No Trusted Setup: Unlike zk-SNARKs, zk-STARKs don’t rely on a trusted setup, making them more secure in certain environments.
Larger Proof Size: While faster and more scalable, zk-STARKs generally produce larger proofs than zk-SNARKs.

