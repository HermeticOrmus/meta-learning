# Notion Hub Architecture

> Design document for the Meta-Learning Knowledge Hub in Notion.

---

## Overview

The Meta-Learning Knowledge Hub is a hierarchical Notion workspace that organizes distilled knowledge across multiple subjects. Each subject gets its own page with standardized databases, lens analyses, and learning method pages.

## Top-Level Structure

```
Meta-Learning Knowledge Hub (page)
├── Subject Registry (database)
│     ├── Information Theory (entry → page)
│     ├── Category Theory (entry → page)
│     └── ... (future subjects)
│
└── Per-Subject Pages
      ├── 4 Databases (Key Concepts, Key Figures, References, Learning Paths)
      ├── Master Learner Perspectives (8 lens pages)
      ├── Learning Science Methods (9 method pages)
      └── Synthesis (3 synthesis pages)
```

## Subject Registry Database

Central tracking database for all distilled subjects.

| Property | Type | Values |
|----------|------|--------|
| Subject Name | Title | Free text |
| Status | Select | Not Started / Extracting / Structuring / Populating / Illuminating / Applying / Synthesizing / Complete |
| Source Files | Rich Text | Paths to raw research documents |
| Lenses Applied | Number | 0-8 |
| Methods Applied | Number | 0-9 |
| Last Updated | Date | Auto-set |

## Per-Subject Page Structure

Each subject page contains:

### Header Section
- Subject overview paragraph
- Source document list
- Quick stats (concepts, figures, references)

### Databases Section
Four inline databases:

1. **Key Concepts** — Core concepts with definitions, categories, importance levels
2. **Key Figures** — Historical contributors with eras, contributions, legacy
3. **References** — Papers, books, lectures with key results
4. **Learning Paths** — Structured study routes at different difficulty levels

### Master Learner Perspectives Section
Eight sub-pages, one per lens:
1. Da Vinci Lens (cross-domain connections)
2. Tesla Lens (mental models, first principles)
3. Franklin Lens (decision tables, practical checklists)
4. Feynman Lens (plain-English explanations, analogies)
5. Von Neumann Lens (axiomatic structure, proof sketches)
6. Aristotle Lens (taxonomy, classification)
7. Musk Lens (industry applications, engineering impact)
8. Oakley Lens (study strategies, chunking, spaced repetition)

### Learning Science Methods Section
Nine sub-pages, one per method:
1. Encoding — Relationship maps
2. Classification — Taxonomic hierarchy
3. Pattern Recognition — Recurring structures
4. Deliberate Practice — Graded problem sets
5. Focused-Diffuse — Study session design
6. Metalearning Map — Field overview
7. Observation — Phenomena and experiments
8. Tracking Discipline — Progress milestones
9. Visualization — Mental imagery

### Synthesis Section
Three sub-pages:
1. Cross-Cutting Patterns — Themes across all lenses
2. Recommended Learning Sequence — Optimal study order
3. Quick Reference / Cheat Sheet — One-page summary

## Page Naming Convention

```
{Subject Name} — {Section Type}: {Specific Name}
```

Examples:
- "Information Theory — Da Vinci Lens"
- "Information Theory — Deliberate Practice"
- "Information Theory — Quick Reference"

## Data Flow

```
Raw Research Documents
        ↓
   Phase 1: EXTRACT
        ↓
   Structured Data (concepts, figures, references)
        ↓
   Phase 2: STRUCTURE (create Notion databases)
        ↓
   Phase 3: POPULATE (fill databases)
        ↓
   Phase 4: ILLUMINATE (8 lens pages)
        ↓
   Phase 5: APPLY (9 method pages)
        ↓
   Phase 6: SYNTHESIZE (3 synthesis pages)
        ↓
   Phase 7: PERSIST (knowledge graph + GitHub)
```

## Notion IDs Reference (Information Theory)

| Entity | Notion ID |
|--------|-----------|
| Hub Page | `2ffef9ce-cda4-81a0-a51f-c7db230fff96` |
| Subject Registry | `be915e09-b215-4927-b786-10c5e94d9c6b` |
| IT Page | `2ffef9ce-cda4-81a2-8f3f-ee4f7a192b83` |
| Key Concepts DB | `595758e6-f0b3-4f5a-9cab-c24a7f1aa687` |
| Key Figures DB | `5c48adc8-cb42-445c-b74b-1d38006be2a1` |
| References DB | `50c29cec-2d92-4837-a7d5-764c8a776893` |
| Learning Paths DB | `ac167aa2-c358-4b57-b375-d2a831f3dbe0` |
