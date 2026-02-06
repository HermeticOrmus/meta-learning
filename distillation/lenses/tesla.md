# Tesla Lens: Mental Modeling & First Principles

**Archetype**: Nikola Tesla (1856-1943) - mental simulation, thought experiments, first-principles reasoning

---

## Method

Build mental models from first principles. Create thought experiments. Derive key results intuitively before formalization. Ask "what would Tesla visualize?"

## Output Template

### 1. First-Principles Derivation
For each core result:
- What are the absolute minimum assumptions?
- What follows logically from those assumptions?
- Walk through the derivation intuitively

### 2. Thought Experiments
For each major concept:
- Design a scenario that isolates the concept
- What happens if you change one variable?
- What's the extreme case?
- What's the limiting behavior?

### 3. Mental Simulation Exercises
- Close your eyes and simulate the process
- Walk through each step mentally
- What does the system "feel like" from the inside?

### 4. "What Would Tesla Visualize?"
- What mental image captures the essence?
- How does the system move, transform, flow?
- What's the shape of the solution space?

---

## Example: Information Theory

### First-Principles Derivation of Entropy
Starting from three axioms:
1. Uncertainty is a function of probabilities only
2. Maximum uncertainty when all outcomes equally likely
3. Independent events have additive uncertainty

From these three alone, Shannon proved H(X) = -sum(p_i * log(p_i)) is the ONLY function that works. No other formula satisfies all three properties.

### Thought Experiment: The Noisy Telephone
Imagine whispering a message through a chain of 100 people in a noisy room:
- Each person mishears ~10% of phonemes
- After 100 transmissions, the message is unrecognizable
- Shannon proved: with the right encoding, you can transmit perfectly even through noisy channels, up to a calculable limit (channel capacity)

### Mental Simulation: Compression
Picture a bag of 1000 colored marbles:
- If 999 are red and 1 is blue, you barely need any information to describe the bag ("all red, except one blue")
- If all 1000 are different colors, you need to describe every single one
- Entropy measures this: low entropy = highly compressible, high entropy = incompressible
