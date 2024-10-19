# Types of ZKPs
## Interactive Zero-Knowledge Proofs (IZKPs)
In this type, the prover and verifier need to interact with each other through multiple rounds of communication. The verifier sends random challenges, and the prover responds to these challenges. Over time, the verifier becomes convinced of the prover's knowledge without learning the secret itself.

Example: The colorblind pen analogy, where the prover and verifier repeatedly interact to show the pens are different colors without revealing the actual colors.
Key Characteristics:
Requires multiple rounds of communication.
Security relies on the randomness of the verifier’s challenges.
Used in theoretical contexts or specific cryptographic protocols where interactivity is acceptable.
## Non-Interactive Zero-Knowledge Proofs (NIZKPs)
Here, the prover can generate a proof that the verifier can check later without any interaction. This is done by replacing the verifier's random challenges with a cryptographic hash (as seen in the Fiat-Shamir heuristic).

Example: zk-SNARKs (Succinct Non-interactive Arguments of Knowledge) used in blockchain.
Key Characteristics:
No interaction required between prover and verifier.
The prover generates the proof once, and the verifier can check it anytime.
Ideal for distributed systems, blockchain, and public verifications.
## zk-SNARKs (Zero-Knowledge Succinct Non-Interactive Arguments of Knowledge)
zk-SNARKs are a specific type of Non-Interactive ZKP that are designed to be both succinct (small in size) and efficient to verify. These are widely used in cryptocurrencies, like Zcash, to enable privacy-preserving transactions.

### Key Characteristics:
Succinct: The proof is very small and can be quickly verified.
Non-Interactive: Requires no back-and-forth communication.
Knowledge Argument: The prover can convince the verifier that they know a solution without revealing the details.
Use Cases:
Blockchain: zk-SNARKs are used for privacy in cryptocurrencies.
Verification: Used for verifying large computations in a short time.
## zk-STARKs (Zero-Knowledge Scalable Transparent Arguments of Knowledge)
zk-STARKs are another type of Non-Interactive ZKP, similar to zk-SNARKs, but with some improvements in terms of scalability and transparency.

Scalable: They can handle larger computations more efficiently than zk-SNARKs.
Transparent: They don’t require a trusted setup phase (which zk-SNARKs typically do).
### Key Characteristics:
Scalability: Better suited for large computations.
No Trusted Setup: Unlike zk-SNARKs, zk-STARKs don’t rely on a trusted setup, making them more secure in certain environments.
Larger Proof Size: While faster and more scalable, zk-STARKs generally produce larger proofs than zk-SNARKs.
