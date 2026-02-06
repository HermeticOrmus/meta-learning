# Notion Hub Setup Guide

> Step-by-step instructions for creating the Meta-Learning Knowledge Hub from scratch.

---

## Prerequisites

- Notion workspace with API access
- Notion MCP server configured (for Claude Code automation)
- Raw research documents for at least one subject

---

## Step 1: Create the Hub Page

Create a top-level Notion page called **"Meta-Learning Knowledge Hub"**.

This serves as the root container for all subjects.

```
Tool: mcp__notion__notion-create-pages
Parent: workspace level (or a specific parent page)
Properties: { "title": "Meta-Learning Knowledge Hub" }
Content: Overview of the system, links to subjects
```

## Step 2: Create the Subject Registry Database

Under the Hub page, create a database to track all subjects.

```
Tool: mcp__notion__notion-create-database
Parent: { "page_id": "<hub-page-id>" }
Title: "Subject Registry"
Properties:
  - Subject Name (title)
  - Status (select: Not Started, Extracting, Structuring, Populating, Illuminating, Applying, Synthesizing, Complete)
  - Source Files (rich_text)
  - Lenses Applied (number)
  - Methods Applied (number)
  - Last Updated (date)
```

## Step 3: Create a Subject Page

For each new subject, create a page under the Hub.

```
Tool: mcp__notion__notion-create-pages
Parent: { "page_id": "<hub-page-id>" }
Properties: { "title": "<Subject Name>" }
Content: Subject overview, section headers
```

Also create an entry in the Subject Registry database.

## Step 4: Create Subject Databases

Under the subject page, create 4 databases:

### 4a. Key Concepts Database
See `database-schemas.md` for full schema.

### 4b. Key Figures Database
See `database-schemas.md` for full schema.

### 4c. References Database
See `database-schemas.md` for full schema.

### 4d. Learning Paths Database
See `database-schemas.md` for full schema.

## Step 5: Populate Databases

Use the distillation pipeline's Extract phase to parse source documents, then batch-create entries.

```
Tool: mcp__notion__notion-create-pages
Parent: { "data_source_id": "<database-collection-id>" }
Pages: [up to 100 entries per call]
```

Repeat for each database. Verify counts match extraction targets.

## Step 6: Create Section Pages

Under the subject page, create three section containers:

1. **Master Learner Perspectives** — Container for 8 lens pages
2. **Learning Science Methods** — Container for 9 method pages
3. **Synthesis** — Container for 3 synthesis pages

Then create individual pages under each section following the lens templates in `../lenses/` and the pipeline documentation.

## Step 7: Apply Lenses and Methods

For each lens/method, create a dedicated page with analysis content. Use the templates in `../lenses/` as guides for the expected output format.

Update the Subject Registry entry's Lenses Applied and Methods Applied counts as you go.

## Step 8: Synthesize

Create the three synthesis pages:
1. Cross-Cutting Patterns
2. Recommended Learning Sequence
3. Quick Reference / Cheat Sheet

## Step 9: Persist to Knowledge Graph

Use Memory MCP to create entities and relations:

```
Tool: mcp__memory__create_entities
Entities: Key concepts (type: concept) and key figures (type: figure)

Tool: mcp__memory__create_relations
Relations: invented, derived, generalized, applied, contributed_to, builds_on
```

## Step 10: Update Subject Registry

Set the subject's status to "Complete" and verify final counts.

---

## Automation

The entire process can be automated using the `meta-learning-distill` skill:

```
Skill: meta-learning-distill
Args: subject_name="<name>" source_files="<path1>,<path2>"
```

This skill executes all 7 pipeline phases automatically.

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| URL property error | Use `userDefined:URL` prefix for URL-type properties |
| Batch create limit | Maximum 100 pages per API call |
| Database not found | Fetch the database first to get the `collection://` data source ID |
| Select option colors | Define options in database creation, not during page creation |
| Content too long | Split into multiple update calls using `insert_content_after` |
