# Notion Hub Template: {Subject Name}

> Template for the Notion page structure of a distilled subject.

---

## Subject Page Content

```markdown
# {Subject Name}

## Overview
{1-2 paragraph overview of the subject}

## Source Documents
- {Document 1 title and description}
- {Document 2 title and description}
- {Document 3 title and description}

## Quick Stats
- **Key Concepts**: {count}
- **Key Figures**: {count}
- **References**: {count}
- **Learning Paths**: {count}
- **Lenses Applied**: 8/8
- **Methods Applied**: 9/9

---

## Databases

{Inline Key Concepts database}
{Inline Key Figures database}
{Inline References database}
{Inline Learning Paths database}

---

## Master Learner Perspectives

1. Da Vinci Lens — Cross-domain connections and visual thinking
2. Tesla Lens — Mental models and first-principles reasoning
3. Franklin Lens — Decision tables and practical application
4. Feynman Lens — Plain-English explanations and teaching
5. Von Neumann Lens — Axiomatic structure and formal proofs
6. Aristotle Lens — Classification and taxonomy
7. Musk Lens — Engineering applications and industry impact
8. Oakley Lens — Learning strategies and study design

---

## Learning Science Methods

1. Encoding — Relationship maps
2. Classification — Taxonomy
3. Pattern Recognition — Recurring structures
4. Deliberate Practice — Problem sets
5. Focused-Diffuse — Study sessions
6. Metalearning Map — Field overview
7. Observation — Phenomena
8. Tracking Discipline — Progress milestones
9. Visualization — Mental imagery

---

## Synthesis

1. Cross-Cutting Patterns
2. Recommended Learning Sequence
3. Quick Reference / Cheat Sheet
```

---

## Database Creation Commands

### Key Concepts Database
```json
{
  "parent": {"page_id": "<subject-page-id>"},
  "title": [{"text": {"content": "Key Concepts"}}],
  "properties": {
    "Category": {
      "type": "select",
      "select": {"options": []}
    },
    "Definition": {"type": "rich_text", "rich_text": {}},
    "Importance": {
      "type": "select",
      "select": {
        "options": [
          {"name": "Foundational", "color": "red"},
          {"name": "Core", "color": "orange"},
          {"name": "Advanced", "color": "blue"},
          {"name": "Frontier", "color": "purple"}
        ]
      }
    },
    "Key Formula": {"type": "rich_text", "rich_text": {}},
    "Analogy": {"type": "rich_text", "rich_text": {}},
    "Source Reference": {"type": "rich_text", "rich_text": {}}
  }
}
```

### Key Figures Database
```json
{
  "parent": {"page_id": "<subject-page-id>"},
  "title": [{"text": {"content": "Key Figures"}}],
  "properties": {
    "Era": {
      "type": "select",
      "select": {
        "options": [
          {"name": "Pioneer", "color": "brown"},
          {"name": "Golden Age", "color": "orange"},
          {"name": "Modern", "color": "blue"},
          {"name": "Contemporary", "color": "green"}
        ]
      }
    },
    "Primary Contribution": {"type": "rich_text", "rich_text": {}},
    "Key Papers": {"type": "rich_text", "rich_text": {}},
    "Legacy Impact": {"type": "rich_text", "rich_text": {}}
  }
}
```

### References Database
```json
{
  "parent": {"page_id": "<subject-page-id>"},
  "title": [{"text": {"content": "References"}}],
  "properties": {
    "Authors": {"type": "rich_text", "rich_text": {}},
    "Year": {"type": "number", "number": {"format": "number"}},
    "Type": {
      "type": "select",
      "select": {
        "options": [
          {"name": "Paper", "color": "blue"},
          {"name": "Book", "color": "green"},
          {"name": "Lecture", "color": "orange"},
          {"name": "Tutorial", "color": "yellow"},
          {"name": "Survey", "color": "purple"},
          {"name": "Textbook", "color": "red"}
        ]
      }
    },
    "Key Result": {"type": "rich_text", "rich_text": {}},
    "URL": {"type": "url", "url": {}}
  }
}
```

### Learning Paths Database
```json
{
  "parent": {"page_id": "<subject-page-id>"},
  "title": [{"text": {"content": "Learning Paths"}}],
  "properties": {
    "Difficulty": {
      "type": "select",
      "select": {
        "options": [
          {"name": "Beginner", "color": "green"},
          {"name": "Intermediate", "color": "yellow"},
          {"name": "Advanced", "color": "orange"},
          {"name": "Research", "color": "red"}
        ]
      }
    },
    "Prerequisites": {"type": "rich_text", "rich_text": {}},
    "Concepts Covered": {"type": "rich_text", "rich_text": {}},
    "Estimated Time": {"type": "rich_text", "rich_text": {}},
    "Description": {"type": "rich_text", "rich_text": {}}
  }
}
```
