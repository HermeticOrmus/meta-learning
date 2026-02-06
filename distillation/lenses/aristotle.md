# Aristotle Lens: Classification & Taxonomy

**Archetype**: Aristotle (384-322 BCE) - systematic classification, essential vs. accidental properties, categorical reasoning

---

## Method

Build a complete taxonomy of the subject. Identify essential properties that define each category. Distinguish genus from species. Ask "how would Aristotle classify this?"

## Output Template

### 1. Full Taxonomy Tree
Hierarchical classification of the entire subject:
- Top-level categories (genera)
- Sub-categories (species)
- Individual concepts (instances)
- Classification criteria at each level

### 2. Essential Properties
For each major concept:
- What makes it what it IS (essential)
- What it happens to have but could lack (accidental)
- The defining characteristic that separates it from siblings

### 3. Category Boundaries
- Where do categories blur?
- What are the edge cases?
- What doesn't fit neatly into the taxonomy?

### 4. Aristotelian Four Causes
For each major result:
- Material cause: What is it made of?
- Formal cause: What is its structure?
- Efficient cause: What produced it?
- Final cause: What is it for?

---

## Example: Information Theory

### Full Taxonomy Tree

```
Information Theory
├── Foundations
│   ├── Entropy & Information Measures
│   │   ├── Shannon Entropy
│   │   ├── Conditional Entropy
│   │   ├── Joint Entropy
│   │   ├── Mutual Information
│   │   ├── Relative Entropy (KL Divergence)
│   │   └── Rényi Entropy (generalized)
│   ├── Probability & Stochastic Processes
│   │   ├── Discrete Memoryless Sources
│   │   ├── Markov Sources
│   │   └── Ergodic Sources
│   └── Fundamental Limits
│       ├── Source Coding Theorem
│       ├── Channel Coding Theorem
│       └── Rate-Distortion Theorem
├── Source Coding (Compression)
│   ├── Lossless Compression
│   │   ├── Symbol Codes (Huffman, Shannon-Fano)
│   │   ├── Arithmetic Coding
│   │   ├── Dictionary Methods (LZ77, LZ78, LZW)
│   │   └── Universal Codes (Elias, Fibonacci)
│   └── Lossy Compression
│       ├── Scalar Quantization
│       ├── Vector Quantization
│       ├── Transform Coding (DCT, Wavelets)
│       └── Predictive Coding
├── Channel Coding (Error Correction)
│   ├── Block Codes
│   │   ├── Linear Codes (Hamming, Reed-Muller)
│   │   ├── Cyclic Codes (BCH, Reed-Solomon)
│   │   └── Algebraic Geometry Codes
│   ├── Convolutional Codes
│   │   └── Viterbi Decoding
│   ├── Modern Codes
│   │   ├── Turbo Codes
│   │   ├── LDPC Codes
│   │   └── Polar Codes
│   └── Channel Models
│       ├── Binary Symmetric Channel
│       ├── Binary Erasure Channel
│       ├── AWGN Channel
│       └── Fading Channels
├── Network Information Theory
│   ├── Multi-Access Channels
│   ├── Broadcast Channels
│   ├── Relay Channels
│   ├── Interference Channels
│   └── Network Coding
├── Quantum Information Theory
│   ├── Quantum Entropy (von Neumann)
│   ├── Quantum Channels
│   ├── Quantum Error Correction
│   ├── Entanglement Theory
│   └── Quantum Key Distribution
├── Algorithmic Information Theory
│   ├── Kolmogorov Complexity
│   ├── Algorithmic Randomness
│   ├── Minimum Description Length
│   └── Connections to Gödel Incompleteness
└── Applications
    ├── Communications Engineering
    ├── Machine Learning (cross-entropy, mutual info)
    ├── Cryptography
    ├── Statistical Inference
    ├── Computational Biology
    └── Natural Language Processing
```

### Essential Properties

| Concept | Essential Property | Distinguishing Feature |
|---------|-------------------|----------------------|
| Entropy | Quantifies average uncertainty | The unique measure satisfying Shannon's axioms |
| Mutual Information | Measures statistical dependence | Symmetric, non-negative, zero iff independent |
| Channel Capacity | Maximum achievable reliable rate | Operational meaning: the boundary of possibility |
| Lossless coding | Perfect reconstruction guaranteed | Rate bounded below by entropy |
| Lossy coding | Allows controlled distortion | Rate-distortion tradeoff |
| Block codes | Fixed-length input → fixed-length output | Minimum distance determines error capability |
| Convolutional codes | Sliding window encoding | Memory in the encoder, decoded by trellis |

### Four Causes of Shannon's Channel Coding Theorem

- **Material cause**: Probability distributions over input/output alphabets
- **Formal cause**: C = max_{p(x)} I(X;Y), the mathematical structure
- **Efficient cause**: Shannon's 1948 random coding argument
- **Final cause**: To establish the fundamental limit of reliable communication
