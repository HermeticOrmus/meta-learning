# Database Schemas

> Complete schema definitions for all Notion databases in the Meta-Learning Knowledge Hub.

---

## 1. Subject Registry Database

**Purpose**: Track all subjects being distilled across the hub.

| Property | Type | Description | Values |
|----------|------|-------------|--------|
| Subject Name | Title | Name of the subject | Free text |
| Status | Select | Current pipeline phase | Not Started, Extracting, Structuring, Populating, Illuminating, Applying, Synthesizing, Complete |
| Source Files | Rich Text | Paths to raw research documents | File paths |
| Lenses Applied | Number | Count of completed lens analyses | 0-8 |
| Methods Applied | Number | Count of completed method pages | 0-9 |
| Last Updated | Date | Last modification date | Auto |

---

## 2. Key Concepts Database

**Purpose**: Catalog all important concepts within a subject.

| Property | Type | Description | Values |
|----------|------|-------------|--------|
| Concept Name | Title | Name of the concept | Free text |
| Category | Select | Subject sub-field | Subject-specific (e.g., Foundations, Source Coding, Channel Coding) |
| Definition | Rich Text | Clear definition of the concept | Markdown-formatted text |
| Importance | Select | Significance level | Foundational, Core, Advanced, Frontier |
| Key Formula | Rich Text | Primary formula or equation | LaTeX or text |
| Analogy | Rich Text | Intuitive analogy for the concept | Plain English |
| Source Reference | Rich Text | Citation to primary source | Author (Year) format |

### Importance Classification Guide

- **Foundational**: Core building blocks the entire field rests on. Everyone must know these.
- **Core**: Central concepts every practitioner should understand.
- **Advanced**: Deeper concepts for specialists and researchers.
- **Frontier**: Cutting-edge research, still actively developing.

### Target: 50-80 concepts per subject

---

## 3. Key Figures Database

**Purpose**: Document historical and contemporary contributors to the subject.

| Property | Type | Description | Values |
|----------|------|-------------|--------|
| Name | Title | Full name of the figure | Free text |
| Era | Select | Historical period | Subject-specific (e.g., Pioneer, Golden Age, Modern, Contemporary) |
| Primary Contribution | Rich Text | Most important contribution | Concise description |
| Key Papers | Rich Text | Landmark publications | Title (Year) format |
| Legacy Impact | Rich Text | Lasting influence on the field | Description of impact |

### Era Classification Guide

- **Pioneer**: Founding figures who established the field
- **Golden Age**: Major contributors during the field's rapid development
- **Modern**: Contributors from the computational/digital era
- **Contemporary**: Active researchers pushing current boundaries

### Target: 30-40 figures per subject

---

## 4. References Database

**Purpose**: Curated bibliography of essential readings.

| Property | Type | Description | Values |
|----------|------|-------------|--------|
| Title | Title | Title of the work | Free text |
| Authors | Rich Text | Author name(s) | Comma-separated |
| Year | Number | Publication year | YYYY format |
| Type | Select | Publication type | Paper, Book, Lecture, Tutorial, Survey, Textbook |
| Key Result | Rich Text | Main finding or contribution | Concise summary |
| URL | URL | Link to the resource | Valid URL |

### Type Classification Guide

- **Paper**: Original research article
- **Book**: Comprehensive textbook or monograph
- **Lecture**: Recorded lecture or lecture notes
- **Tutorial**: Introductory tutorial or guide
- **Survey**: Review paper covering a sub-field
- **Textbook**: Standard educational textbook

### Target: 50-100+ references per subject

---

## 5. Learning Paths Database

**Purpose**: Structured study routes at different difficulty levels.

| Property | Type | Description | Values |
|----------|------|-------------|--------|
| Path Name | Title | Descriptive name for the path | Free text |
| Difficulty | Select | Target audience level | Beginner, Intermediate, Advanced, Research |
| Prerequisites | Rich Text | Required prior knowledge | Concept names or general knowledge areas |
| Concepts Covered | Rich Text | Key concepts included in this path | Concept names from Key Concepts DB |
| Estimated Time | Rich Text | Expected study duration | "X weeks at Y hours/week" format |
| Description | Rich Text | Overview of the path | What you'll learn and why |

### Target: 4-6 paths per subject

---

## Notion API Notes

### Property Naming Gotchas
- Properties named `URL` or `url` must use the prefix `userDefined:URL` when creating pages via the API (reserved name conflict in Notion)
- Properties named `id` or `ID` similarly need `userDefined:id`

### Batch Creation
- `mcp__notion__notion-create-pages` supports up to 100 pages per call
- Use `parent: {"data_source_id": "..."}` when targeting a database's data source
- Data source IDs look like `collection://UUID` in Notion fetch results

### Select Properties
- Select options are auto-created when a new value is used
- For consistent colors, define options when creating the database
