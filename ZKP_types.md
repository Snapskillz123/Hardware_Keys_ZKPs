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
