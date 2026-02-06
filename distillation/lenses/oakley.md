# Oakley Lens: Learning Strategy & Cognitive Science

**Archetype**: Barbara Oakley (1955-) - learning how to learn, chunking, spaced repetition, focused-diffuse modes

---

## Method

Design optimal learning strategies. Plan chunking sequences. Build spaced repetition schedules. Map focused vs. diffuse practice. Ask "how would Oakley structure the learning?"

## Output Template

### 1. Chunking Plan
Sequence concepts into learnable chunks:
- Foundational chunks (learn first)
- Building chunks (require foundations)
- Advanced chunks (require building blocks)
- Integration chunks (connect everything)

### 2. Spaced Repetition Schedule
For each chunk:
- Initial learning session design
- Review intervals (day 1, 3, 7, 14, 30, 90)
- Active recall prompts
- Interleaving strategy

### 3. Focused-Diffuse Balance
For each concept type:
- Focused mode activities (problem solving, proofs)
- Diffuse mode activities (walks, analogies, rest)
- When to switch modes
- Signs of productive struggle vs. unproductive grinding

### 4. Practice Progression
- Beginner exercises (pattern matching)
- Intermediate problems (application)
- Advanced challenges (synthesis)
- Expert problems (research-level)

### 5. Common Learning Pitfalls
- Illusions of competence to watch for
- Einstellung (being stuck in wrong approach)
- Overlearning traps
- When to seek help vs. persist

---

## Example: Information Theory

### Chunking Plan

**Chunk 1: Foundations (Week 1-2)**
- Probability review: distributions, expectation, independence
- Logarithms and their properties
- Surprise/self-information: I(x) = -log p(x)
- Shannon entropy: H(X) = E[I(X)]
- Practice: Calculate entropy for simple distributions

**Chunk 2: Core Measures (Week 3-4)**
- Joint entropy H(X,Y)
- Conditional entropy H(X|Y)
- Chain rule for entropy
- Mutual information I(X;Y)
- Practice: Compute measures for joint distributions, verify chain rule

**Chunk 3: Source Coding (Week 5-6)**
- Kraft inequality and prefix codes
- Huffman coding algorithm
- Source coding theorem (statement and intuition)
- Asymptotic Equipartition Property
- Practice: Build Huffman codes, calculate compression ratios

**Chunk 4: Channel Coding (Week 7-8)**
- Channel models (BSC, BEC, AWGN)
- Channel capacity calculation
- Channel coding theorem (statement and significance)
- Basic error-correcting codes (Hamming)
- Practice: Calculate capacity for standard channels

**Chunk 5: Advanced Topics (Week 9-12)**
- Rate-distortion theory
- Network information theory basics
- Connections to other fields (ML, physics, biology)
- Practice: Apply IT to real problems

### Spaced Repetition Prompts

| Concept | Active Recall Prompt |
|---------|---------------------|
| Entropy | "Write the entropy formula. What are the three axioms? Calculate H for fair coin." |
| Mutual Information | "Define I(X;Y) three ways. When is it zero? Draw the Venn diagram." |
| Source Coding Theorem | "State the theorem. Why can't you beat entropy? What's the AEP?" |
| Channel Capacity | "Define capacity. Calculate for BSC with p=0.1. What happens above capacity?" |
| Huffman Coding | "Build a Huffman code for {A:0.4, B:0.3, C:0.2, D:0.1}. Is it optimal? Why?" |
| KL Divergence | "Define D(P\|\|Q). Why isn't it symmetric? When is it zero?" |
| Fano's Inequality | "State Fano's inequality. What does it connect? Why does it matter?" |

### Focused-Diffuse Balance

| Activity | Mode | Purpose |
|----------|------|---------|
| Deriving entropy properties | Focused | Build formal understanding |
| Walking after studying channel capacity | Diffuse | Let intuition form |
| Working problem sets | Focused | Strengthen recall pathways |
| Explaining concepts to someone else | Focused | Test understanding |
| Thinking about real-world compression | Diffuse | Connect theory to intuition |
| Reading Shannon's original paper | Focused | See the source reasoning |
| Sleeping after learning new theorems | Diffuse | Consolidate memory |

### Common Learning Pitfalls

1. **Illusion of competence**: Reading proofs feels like understanding them. Test yourself by reproducing key steps from memory.

2. **Einstellung on continuous vs. discrete**: Students trained on discrete IT struggle when switching to differential entropy. The formulas look similar but the properties differ (differential entropy can be negative).

3. **Overlearning entropy calculations**: Students drill entropy computation but never internalize WHY entropy is the right measure. Spend time on the axiomatic motivation, not just computation.

4. **Skipping probability prerequisites**: IT is built on probability theory. Weak probability foundations create cascading confusion. Review probability thoroughly before starting.

5. **Treating theorems as formulas**: The source coding theorem and channel coding theorem are existence results, not algorithms. Understanding the conceptual significance matters more than memorizing bounds.
