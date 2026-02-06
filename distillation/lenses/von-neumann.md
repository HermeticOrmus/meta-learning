# Von Neumann Lens: Formal Structure & Axiomatics

**Archetype**: John von Neumann (1903-1957) - rigorous formalization, axiomatic foundations, logical architecture

---

## Method

Identify the axiomatic foundations. Map logical dependencies between theorems. Build the formal hierarchy from axioms to applications. Ask "what would von Neumann formalize?"

## Output Template

### 1. Axiomatic Foundation
- What are the minimal axioms?
- Which axioms are independent?
- What falls apart if you remove each one?

### 2. Theorem Dependency Graph
Map the logical flow:
- Axioms → Lemmas → Theorems → Corollaries → Applications
- Which results depend on which?
- Where are the critical bottlenecks?

### 3. Proof Sketches
For each major theorem:
- Key insight that makes the proof work
- Proof strategy (contradiction, construction, induction, etc.)
- What makes it non-obvious

### 4. Formal vs. Intuitive
For each concept:
- The formal definition (precise)
- The intuitive meaning (accessible)
- Why the formal version is necessary

---

## Example: Information Theory

### Axiomatic Foundation of Entropy

Shannon's entropy H(X) = -Σ p(x) log p(x) is the UNIQUE function satisfying:

1. **Continuity**: H is continuous in the probabilities p_i
2. **Maximum at Uniformity**: H(1/n, ..., 1/n) is maximized for equal probabilities
3. **Recursion (Grouping)**: H can be decomposed when grouping outcomes

**Independence**: Remove any one axiom and alternative measures become possible. Remove continuity → Rényi entropies qualify. Remove maximality → trivial measures qualify.

### Theorem Dependency Graph

```
Axioms (probability space)
  ├── Shannon Entropy H(X)
  │     ├── Joint Entropy H(X,Y)
  │     │     ├── Conditional Entropy H(X|Y)
  │     │     └── Chain Rule: H(X,Y) = H(X) + H(Y|X)
  │     ├── Mutual Information I(X;Y) = H(X) - H(X|Y)
  │     │     ├── Data Processing Inequality
  │     │     └── Fano's Inequality
  │     └── Relative Entropy D(P||Q)
  │           ├── Gibbs' Inequality: D(P||Q) ≥ 0
  │           └── Maximum Entropy Principle
  ├── Source Coding Theorem
  │     ├── Kraft Inequality
  │     ├── Huffman Coding (optimal prefix codes)
  │     └── Asymptotic Equipartition Property (AEP)
  ├── Channel Coding Theorem
  │     ├── Channel Capacity C = max I(X;Y)
  │     ├── Random Coding Argument
  │     └── Converse (impossibility above C)
  └── Rate-Distortion Theory
        ├── Distortion Measures
        └── Rate-Distortion Function R(D)
```

### Critical Proof Sketches

**Source Coding Theorem**: You cannot compress n i.i.d. symbols into fewer than nH(X) bits. Proof via AEP: with high probability, a sequence falls in the "typical set" of size ~2^{nH(X)}, so you need ~nH(X) bits to index it.

**Channel Coding Theorem**: Random coding argument — generate 2^{nR} random codewords. For R < C, the probability that a random code fails goes to 0 as n → ∞. Non-constructive but existentially powerful.

**Fano's Inequality**: If you can estimate X from Y with low error probability P_e, then H(X|Y) ≤ H(P_e) + P_e log(|X|-1). Bridges information-theoretic and probabilistic reasoning.

### Formal vs. Intuitive

| Concept | Formal | Intuitive |
|---------|--------|-----------|
| Entropy | H(X) = -Σ p(x) log p(x) | Average surprise per symbol |
| Mutual Information | I(X;Y) = H(X) - H(X\|Y) | How much Y tells you about X |
| Channel Capacity | C = max_{p(x)} I(X;Y) | Speed limit for reliable communication |
| Typical Set | A_ε^n = {x^n : \|−1/n log p(x^n) − H\| < ε} | The "likely" sequences |
