# Feynman Lens: Teaching & Simplification

**Archetype**: Richard Feynman (1918-1988) - explain to a child, analogies, teaching as understanding

---

## Method

Explain every concept in plain English. Create analogies. Apply the Feynman Technique: if you can't explain it simply, you don't understand it. Ask "how would Feynman teach this?"

## Output Template

### 1. Plain-English Explanations
For each key theorem/concept:
- What it says (no jargon)
- Why it matters
- What changes because of it

### 2. Analogies
For each abstract concept:
- A concrete analogy from everyday life
- Where the analogy breaks down
- What the analogy captures perfectly

### 3. "Explain Like I'm 5" Versions
Ultra-simple versions of the most important ideas

### 4. Teaching Script
A 10-minute lecture that covers the core of the subject:
- Hook (why should anyone care?)
- Three key ideas
- The surprising insight
- What to explore next

### 5. Common Misconceptions
What people get wrong and why

---

## Example: Information Theory

### Shannon's Source Coding Theorem (Plain English)
"There's a mathematical floor to how small you can compress data without losing anything. That floor is called entropy. No matter how clever your algorithm, you can never beat entropy. But you can get arbitrarily close."

### Channel Coding Theorem (Plain English)
"Even through a noisy channel, you can communicate perfectly -- as long as you don't try to send data faster than the channel's speed limit. That speed limit is called channel capacity. Below it: perfect transmission is possible. Above it: errors are unavoidable."

### Analogy: Entropy as Surprise
Think of entropy like the average surprise in a news feed:
- A feed that only posts "the sun rose today" has zero surprise (zero entropy)
- A feed that posts completely random characters has maximum surprise (maximum entropy)
- Your actual news feed is somewhere in between -- some predictable, some surprising

Entropy measures the average surprise per message. High entropy = hard to predict = hard to compress. Low entropy = predictable = easy to compress.

### ELI5: What Is Information?
Imagine you're playing 20 Questions. Each yes/no answer gives you exactly 1 bit of information. If there are 8 possible animals, you need exactly 3 questions (2^3 = 8). Information is just "how many yes/no questions do I need to figure this out?"

### Common Misconception
"More data = more information." Wrong. A file of 1 million zeros contains almost no information. A file of 1 million random bits contains maximum information. Information is about unpredictability, not volume.
