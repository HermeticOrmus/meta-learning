# Franklin Lens: Systematic Tracking & Practical Wisdom

**Archetype**: Benjamin Franklin (1706-1790) - systematic self-improvement, decision frameworks, practical application

---

## Method

Create practical decision frameworks. Track and compare methods. Build systematic comparison tables. Ask "what would Franklin track?"

## Output Template

### 1. Decision Tables
"Which method for which scenario?"
- Scenario description
- Available approaches
- Key decision criteria
- Recommended choice with reasoning

### 2. Pros/Cons Analysis
For each competing approach:
- Advantages (be specific)
- Disadvantages (be specific)
- When to use each
- When NOT to use each

### 3. Practical Application Checklist
Step-by-step guide for applying the subject's methods:
- What to do first
- Common mistakes to avoid
- Verification steps
- Success criteria

### 4. "What Would Franklin Track?"
Measurable metrics for the subject:
- What can be quantified?
- What progress looks like
- Key benchmarks

---

## Example: Information Theory

### Decision Table: Which Compression Algorithm?

| Scenario | Best Choice | Why |
|----------|------------|-----|
| Text files | LZ77/DEFLATE | Exploits character-level redundancy |
| Images (lossy OK) | JPEG/WebP | Rate-distortion optimal for visual data |
| Images (lossless) | PNG | Good for structured visual data |
| Audio (lossy OK) | AAC/Opus | Psychoacoustic models match perception |
| Streaming data | Arithmetic coding | Approaches entropy bound closely |
| Need speed over ratio | LZ4 | Fast decompression, decent ratio |

### Decision Table: Which Error-Correcting Code?

| Scenario | Best Choice | Why |
|----------|------------|-----|
| Deep space comms | Turbo/LDPC | Near Shannon limit at very low SNR |
| 5G wireless | Polar codes | Provably capacity-achieving, hardware-friendly |
| QR codes | Reed-Solomon | Good burst-error correction |
| RAM/storage | Hamming/SEC-DED | Simple, fast, adequate for low error rates |
| Fiber optic | LDPC | High throughput at very low error rates |

### Practical Checklist: Designing a Communication System
1. Measure channel characteristics (bandwidth, noise, error rate)
2. Calculate channel capacity C = B * log2(1 + SNR)
3. Choose target data rate R < C (leave margin)
4. Select appropriate error-correcting code for the gap
5. Apply source coding to compress input to minimum entropy
6. Verify end-to-end bit error rate meets requirements
