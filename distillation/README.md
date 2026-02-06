# Meta-Learning Distillation System

> **Transform raw research into multi-perspective Notion knowledge hubs using 8 master learner lenses and 9 learning science methods.**

---

## What Is Distillation?

Distillation is the process of taking raw, unstructured research on any subject and transforming it into a structured, multi-perspective knowledge hub. It applies the meta-learning framework (8 lenses + 9 methods) to extract maximum insight from source material.

**Input**: Raw research documents (papers, notes, textbooks, references)
**Output**: A Notion Knowledge Hub with databases, multi-lens analysis, learning paths, and a knowledge graph

---

## The 7-Phase Pipeline

| Phase | Name | What Happens |
|-------|------|--------------|
| 1 | **EXTRACT** | Parse source documents for concepts, figures, references |
| 2 | **STRUCTURE** | Create Notion databases (Key Concepts, Key Figures, References, Learning Paths) |
| 3 | **POPULATE** | Batch-fill databases with extracted data |
| 4 | **ILLUMINATE** | Apply 8 master learner lenses for multi-perspective analysis |
| 5 | **APPLY** | Apply 9 learning science methods |
| 6 | **SYNTHESIZE** | Cross-cut analysis, recommended learning sequence, quick reference |
| 7 | **PERSIST** | Knowledge graph (Memory MCP) + GitHub documentation |

See `pipeline.md` for the detailed process.

---

## The 8 Master Learner Lenses

Each lens views the subject through a different archetype's methodology:

| # | Lens | Archetype | Focus |
|---|------|-----------|-------|
| 1 | **Da Vinci** | Leonardo da Vinci | Observation, cross-domain connections, visual thinking |
| 2 | **Tesla** | Nikola Tesla | Mental models, thought experiments, first-principles |
| 3 | **Franklin** | Benjamin Franklin | Systematic tracking, decision frameworks, practical wisdom |
| 4 | **Feynman** | Richard Feynman | Teaching, simplification, analogies |
| 5 | **Von Neumann** | John von Neumann | Formal structure, axioms, logical hierarchies |
| 6 | **Aristotle** | Aristotle | Classification, taxonomies, categorical thinking |
| 7 | **Musk** | Elon Musk | Practical application, engineering, industry impact |
| 8 | **Oakley** | Barbara Oakley | Learning strategy, chunking, spaced repetition |

See `lenses/` for detailed documentation of each lens.

---

## The 9 Learning Science Methods

| # | Method | Purpose |
|---|--------|---------|
| 1 | **Encoding** | Map relationships between concepts, create association networks |
| 2 | **Classification** | Build taxonomies, sort into categories |
| 3 | **Pattern Recognition** | Identify recurring structures and isomorphisms |
| 4 | **Deliberate Practice** | Design problem sets at increasing difficulty |
| 5 | **Focused-Diffuse** | Alternate concentrated study with relaxed reflection |
| 6 | **Metalearning Map** | Map the field: what to learn, how, what resources exist |
| 7 | **Observation** | Key phenomena to notice, mental experiments to run |
| 8 | **Tracking Discipline** | Track progress, measure understanding, identify gaps |
| 9 | **Visualization** | Mental imagery for abstract concepts |

---

## Notion Hub Architecture

```
Meta-Learning Knowledge Hub
  |
  +-- Subject Registry (Database: all subjects)
  |
  +-- [Subject Name] (Page per subject)
       |
       +-- Key Concepts (Database)
       +-- Key Figures (Database)
       +-- References (Database)
       +-- Learning Paths (Database)
       |
       +-- Master Learner Perspectives
       |    +-- Da Vinci Lens
       |    +-- Tesla Lens
       |    +-- Franklin Lens
       |    +-- Feynman Lens
       |    +-- Von Neumann Lens
       |    +-- Aristotle Lens
       |    +-- Musk Lens
       |    +-- Oakley Lens
       |
       +-- Learning Science Methods
       |    +-- Encoding Method
       |    +-- Classification
       |    +-- Pattern Recognition
       |    +-- Deliberate Practice
       |    +-- Focused-Diffuse
       |    +-- Metalearning Map
       |    +-- Observation
       |    +-- Tracking Discipline
       |    +-- Visualization
       |
       +-- Synthesis
            +-- Cross-Cutting Patterns
            +-- Recommended Learning Sequence
            +-- Quick Reference / Cheat Sheet
```

See `notion/` for detailed architecture and database schemas.

---

## Completed Subjects

| Subject | Status | Concepts | Figures | References | Lenses | Methods |
|---------|--------|----------|---------|------------|--------|---------|
| Information Theory | Complete | 67 | 36 | 35 | 8/8 | 9/9 |

See `examples/` for detailed output from each subject.

---

## How to Distill a New Subject

1. Gather raw research documents (papers, textbooks, notes)
2. Use the `meta-learning-distill` Claude Code skill:
   ```
   /meta-learning-distill subject_name="Your Subject" source_files="path/to/docs/*"
   ```
3. The system runs the 7-phase pipeline automatically
4. Review the generated Notion Hub and refine as needed

See `notion/setup-guide.md` for manual setup instructions.

---

## File Structure

```
distillation/
  README.md              # This file
  pipeline.md            # Detailed 7-phase process
  lenses/                # One file per lens
  notion/                # Notion Hub architecture docs
  examples/              # Completed subject examples
```
