# zk SNARKS
zk-SNARKs (Zero-Knowledge Succinct Non-Interactive Arguments of Knowledge) are a powerful cryptographic tool that allows one party (the prover) to convince another party (the verifier) that they know a specific piece of information (or solution to a problem) without revealing the information itself.
Additionally, the proof is succinct (small and efficient to verify) and non-interactive (requires no back-and-forth communication).
## Arithmetic Circuits
An arithmetic circuit is like a set of mathematical operations that represent the problem, similar to a flowchart or a logical sequence of steps.
zk-SNARKs convert a computational problem into an arithmetic circuit.


Let's fix a finite field F.

$F={0,1,2,...,p-1} for p>2$

An arithmetic circuit takes a list of $n$ elements in a field $F$ and produces one element from the field. It depicted by a [direct acyclic graph (DAGs)](https://en.wikipedia.org/wiki/Directed_acyclic_graph) which is a depiction of a polynomial viaa graph.

Suppose we have a circuit like this:

![image](https://github.com/user-attachments/assets/ab8e76f0-8683-4a7c-bd25-0f57c519f217)


The input gates perform $x1,x2,1$ and the sum gates perform $x1+1,x2+2$ and the product gate performs $(x1+x2).x2.(x2+1)$
