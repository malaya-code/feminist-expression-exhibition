# Metadata Schema Documentation

**Version 0.1** | November 2025  
*Living document - updated as research methodologies develop*

---

## Overview

The `feminist_expression_exhibition.sql` file contains structured metadata for five artworks from the *Feminist Expression, In Action!* exhibition. This schema documents artwork metadata using relational database principles, emphasizing accessibility, reproducibility, and scholarly rigor.

---

## Database Schema

### Table: `feminist_expression_exhibition`

| Field | Type | Description |
|-------|------|-------------|
| `id` | `int(10) unsigned` | Unique identifier for each artwork (primary key, auto-increment) |
| `title` | `varchar(255)` | Full artwork title |
| `year` | `year(4)` | Year of creation |
| `medium` | `varchar(255)` | Materials and techniques used |
| `dimensions` | `varchar(128)` | Physical dimensions (format: width×height + unit) |
| `caption` | `varchar(255)` | Short descriptive caption (format: medium, dimensions, year) |
| `alt_text` | `text` | Accessibility description for screen readers and visual description |
| `description_exhibit` | `text` | Exhibition context, theoretical grounding, related works, and citations |
| `image_filename` | `varchar(255)` | Corresponding image file in `/images` directory |

### Field Details

#### `alt_text`

Provides visual descriptions following accessibility best practices. Describes composition, color, form, and visual elements without interpretation. Intended for screen readers and as standalone descriptions for those who cannot view images.

#### `description_exhibit`

Contextualizes the work within feminist theory and exhibition framework. Includes:
- Exhibition provenance
- Theoretical concepts engaged
- Related poems or texts
- Scholarly citations (APA format)
- Artist statements or declarations

#### `image_filename`

Links database entry to corresponding image file. All images are watermarked for protection against unauthorized use while maintaining scholarly accessibility.

---

## Using the Dataset

### Importing the Database

```bash
# MySQL/MariaDB
mysql -u username -p database_name < data/feminist_expression_exhibition.sql

# Or via HeidiSQL, phpMyAdmin, or similar GUI tools
```

### Example Queries

**Retrieve all artworks with metadata:**
```sql
SELECT * FROM feminist_expression_exhibition;
```

**Find artworks by medium:**
```sql
SELECT title, medium, dimensions 
FROM feminist_expression_exhibition 
WHERE medium LIKE '%canvas%';
```

**Get artwork with image filename for display:**
```sql
SELECT title, alt_text, image_filename 
FROM feminist_expression_exhibition 
WHERE id = 28;
```

**Export for citation purposes:**
```sql
SELECT title, year, medium, dimensions, description_exhibit 
FROM feminist_expression_exhibition 
ORDER BY title;
```

---

## Citing Artworks from This Dataset

When using artworks from this dataset in research, presentations, or projects:

### For Academic Papers (APA 7th Edition):

```
Wright, M. (2021). [Artwork title] [Medium]. Feminist Expression, In Action! exhibition.
Retrieved from https://www.malayawonders.info/art/feminist-expression-exhibition
```

### For the Dataset Itself:

```
Wright, M. (2025). Feminist Expression, In Action! Exhibition metadata dataset [Data set].
GitHub. https://github.com/malaya-code/feminist-expression-exhibition
```

### Attribution in Projects:

When displaying or referencing these artworks:
- Include artist name: Malaya Wright
- Include artwork title and year
- Link to exhibition page or dataset repository
- Note: "From the Feminist Expression, In Action! exhibition (2021)"

---

## Usage Guidelines

### ✅ Permitted Uses (Non-Commercial):

- Educational projects and research
- Academic papers and presentations  
- Non-profit exhibitions or galleries
- Accessibility and archival documentation
- Creating similar metadata structures for your own work
- Learning database design and documentation practices

### ❌ Prohibited Uses:

- Commercial sale or redistribution of artworks
- Use in paid products or services without permission
- Removal of watermarks or artist attribution
- Derivative works for distribution (per CC BY-ND 4.0 license)

### 💡 Encouraged:

**Recreate this structure for your own work!** This schema and documentation approach can be adapted for:
- Personal art portfolios
- Exhibition archives
- Museum collections
- Creative practice documentation

If you use this schema as a model, attribution is appreciated but not required for the database structure itself.

---

## Technical Notes

### Character Encoding
- Database uses `utf8mb4` with `utf8mb4_unicode_ci` collation
- Supports full Unicode including emojis and special characters
- Ensures proper display of diverse linguistic content

### Data Integrity
- `title` field has UNIQUE constraint (no duplicate titles)
- Primary key ensures each artwork has unique identifier
- Foreign key relationships can be added for expanded datasets

---

## Future Development

As this practice-based research evolves, the schema may expand to include:

- **Related works table**: Link artworks to poems, essays, or other pieces
- **Theory citations table**: Structured citations with DOI/ISBN fields  
- **Exhibition history**: Track where/when artworks were displayed
- **Technical process**: Document creation methods and materials in detail
- **Conservation notes**: Archival information for long-term preservation

Version updates will be documented in this file.

---

## Questions or Collaboration

For questions about this dataset structure, permission requests, or collaboration on similar documentation projects:

- Website: [malayawonders.info](https://www.malayawonders.info)
- Exhibition: [Feminist Expression, In Action!](https://www.malayawonders.info/art/feminist-expression-exhibition)

---

*Schema documentation version 0.1 created November 15, 2025*
