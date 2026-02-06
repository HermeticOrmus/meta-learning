# The 7-Phase Distillation Pipeline

> Detailed process for transforming raw research into a structured Notion Knowledge Hub.

---

## Phase 1: EXTRACT

**Goal**: Parse all source documents and extract structured data.

### Inputs
- Raw research documents (markdown, PDF, text)
- Subject name and category taxonomy

### Process
1. Read all source documents sequentially
2. Identify and extract:
   - **Key Concepts**: Name, definition, category, importance level, formulas, analogies
   - **Key Figures**: Name, era, primary contribution, key papers, legacy impact
   - **References**: Title, authors, year, type, key result, URL
   - **Category Taxonomy**: Hierarchical organization of the subject

### Target Yields
| Data Type | Target Count |
|-----------|-------------|
| Key Concepts | 50-80 |
| Key Figures | 30-40 |
| References | 50-100+ |
| Categories | 5-10 top-level |

### Importance Classification
- **Foundational**: Core building blocks the entire field rests on
- **Core**: Central concepts every practitioner must know
- **Advanced**: Deeper concepts for specialists
- **Frontier**: Cutting-edge research, still developing

---

## Phase 2: STRUCTURE

**Goal**: Create the Notion database architecture under the subject page.

### Databases to Create
1. **Key Concepts Database**
   - Concept Name (title), Category (select), Definition (rich text), Importance (select), Key Formula (rich text), Analogy (rich text), Source Reference (rich text)

2. **Key Figures Database**
   - Name (title), Era (select), Primary Contribution (rich text), Key Papers (rich text), Legacy Impact (rich text)

3. **References Database**
   - Title (title), Authors (rich text), Year (number), Type (select), Key Result (rich text), URL (url)

4. **Learning Paths Database**
   - Path Name (title), Difficulty (select), Prerequisites (rich text), Concepts Covered (rich text), Estimated Time (rich text), Description (rich text)

### Page Structure
Create section pages under the subject page:
- Master Learner Perspectives (container for 8 lens pages)
- Learning Science Methods (container for 9 method pages)
- Synthesis (container for cross-cut analysis)

---

## Phase 3: POPULATE

**Goal**: Fill all databases with extracted data.

### Process
1. Batch-create Key Concepts entries (up to 100 per API call)
2. Batch-create Key Figures entries
3. Batch-create References entries
4. Create Learning Paths entries (typically 4-6 paths per subject)

### Quality Checks
- Every concept has a definition and importance level
- Every figure has era and primary contribution
- Every reference has at least title, year, and type
- Learning paths cover beginner through advanced

---

## Phase 4: ILLUMINATE

**Goal**: Apply all 8 master learner lenses to the subject.

### For Each Lens
Create a dedicated analysis page with lens-specific output:

| Lens | Key Output |
|------|-----------|
| Da Vinci | Cross-domain connection map, visual hierarchy, observation journal |
| Tesla | First-principles derivations, thought experiments, mental simulations |
| Franklin | Decision tables, pros/cons analysis, practical checklists |
| Feynman | Plain-English explanations, analogies, ELI5 versions, teaching scripts |
| Von Neumann | Axiom sets, proof sketches, logical dependency graphs |
| Aristotle | Full taxonomy tree, classification criteria, essential properties |
| Musk | Industry applications, engineering implementations, impact metrics |
| Oakley | Chunking plans, spaced repetition schedules, practice progressions |

---

## Phase 5: APPLY

**Goal**: Apply learning science methods to the subject.

### For Each Method
Create a dedicated page with method-specific content:

1. **Encoding**: Relationship maps showing how concepts connect
2. **Classification**: Hierarchical taxonomy of the subject
3. **Pattern Recognition**: Recurring structures across theorems/principles
4. **Deliberate Practice**: Graded problem sets (easy/medium/hard/expert)
5. **Focused-Diffuse**: Recommended study session structure
6. **Metalearning Map**: Field overview (what/how/why/resources)
7. **Observation**: Key phenomena and mental experiments
8. **Tracking Discipline**: Progress tracking template with milestones
9. **Visualization**: Mental imagery descriptions for abstract concepts

---

## Phase 6: SYNTHESIZE

**Goal**: Cross-cut analysis combining insights from all lenses and methods.

### Outputs
1. **Cross-Cutting Patterns**: Themes that appear across multiple lenses
2. **Recommended Learning Sequence**: Optimal order to study concepts
3. **Quick Reference / Cheat Sheet**: One-page summary of the subject

### Process
- Identify 5-10 major patterns that recur across lenses
- Sequence concepts from foundational to frontier
- Distill the entire subject into a concise reference

---

## Phase 7: PERSIST

**Goal**: Ensure knowledge survives beyond the Notion hub.

### Knowledge Graph (Memory MCP)
- Create entities for key concepts (with definitions)
- Create entities for key figures (with contributions)
- Create relations mapping connections between entities
- Entity types: concept, figure, subject
- Relation types: invented, derived, generalized, applied, contributed_to, builds_on

### GitHub Repository
- Push distillation documentation to meta-learning repo
- Include extraction summary and lens outputs
- Update README with new subject

### Subject Registry
- Update status to "Complete"
- Set final Lenses Applied and Methods Applied counts

---

## Timing Estimates

| Phase | Relative Effort |
|-------|----------------|
| Extract | 25% |
| Structure | 5% |
| Populate | 15% |
| Illuminate | 25% |
| Apply | 15% |
| Synthesize | 10% |
| Persist | 5% |

The entire pipeline for a subject with 3 source documents (~300KB) takes approximately one extended Claude Code session.
