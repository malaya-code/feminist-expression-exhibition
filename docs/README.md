# Feminist Expression, In Action!


**A feminist-based art exhibition exploring identity, embodiment, and resistance through visual art and poetry.**


Created Summer 2021 | Funded by [Berea College's Women, Gender, and Sexuality Studies Department](https://www.berea.edu/academics/departments-programs/womens-gender-and-sexuality-studies)

[View Live Exhibition](https://www.malayawonders.info/art/feminist-expression-exhibition)

---

## About

During Summer 2021, Berea College's Women, Gender, and Sexuality Studies department funded the creation of this feminist-based exhibition. Each piece engages with feminist praxis and theory, accompanied by original poetry and critical analysis.

### Artist Statement

I often question feminist theory; I ask: "How can we visualize these critiques? How can we navigate change?"

These pieces are a response to my queries. Feminism addresses the uncomfortable—the muffled screams and fleeting glances. The whispers of change.

I hope my art provides solace for the hushed, and unabashedly bares nakedness to your soul. May you stare at them as they stare back at you.

—**Malaya Wright**

---

## Exhibition Works

### 1. BODY (Sold)
**Markers on canvas | 14×11 inches**

Explores bodily autonomy, medical violence, and reclaiming ownership of one's physical self. Accompanied by an [original poem](https://www.malayawonders.info/body) interrogating whose body gets to belong to whom.

### 2. Sis, Life's a Paradox
**Alcohol-resistant markers on canvas | 30×20 inches**

Confronts paradoxes of desire, violence, worship, and selfhood through bold text and vivid imagery. Read the [accompanying poem](https://www.malayawonders.info/sis-paradox).

### 3. A Burning Fire: Sula Ablaze
**Markers on canvas | 40×30 inches**

Inspired by Toni Morrison's *Sula*, proclaiming: "Whatever is burning in me is mine!" Engages with themes of Black feminine power and internal fire.

### 4. RAPE: It's Here
**Mixed media | 26×34 inches**

A survivor-affirming statement piece created for all survivors. Engages with Roxane Gay's *Not That Bad: Dispatches from Rape Culture*.

### 5. Notions of Beauty: Fear the Gaze (Sold)
**Mixed media collage | 36×18 inches**

Layered collage engaging with bell hooks' concepts of Black women and self-recovery, and the oppositional gaze. Declares: "Not only will I stare. I want my look to change reality."

---

## Repository Contents

```
feminist-expression-exhibition/
├── README.md                 # Project overview (you are here)
├── LICENSE                   # CC BY-ND 4.0 International
├── data/
│   └── feminist_expression_exhibition.sql  # Structured metadata for all 5 works
├── images/
│   ├── 2021_BODY_1_watermark.png
│   ├── 2021_cis_paradox_watermark.png
│   ├── 2021_sulaablaze_watermark.jpeg
│   ├── 2021_SA_watermark.png
│   └── 2021_feargaze_watermark.png
└── docs/
    ├── citations.md          # Full APA references
    └── metadata-schema.md    # SQL database schema documentation
```

---

## Using the Dataset

The SQL file contains structured metadata for all exhibition artworks, including:

- Title, year, medium, dimensions
- Alt text (for accessibility)
- Exhibition descriptions and theoretical grounding
- Image filenames

### Import the dataset:

```sql
mysql -u username -p database_name < data/feminist_expression_exhibition.sql
```

### Query example:

```sql
SELECT title, medium, description_exhibit 
FROM feminist_expression_exhibition 
WHERE year = 2021;
```

See `docs/metadata-schema.md` for full field descriptions.

---

## Citations & References

All feminist theory references, artwork citations, and poetry citations are documented in `docs/citations.md`.

### Key theorists engaged:

- bell hooks (*Black Looks: Race and Representation*, *Killing Rage: Ending Racism*)
- Toni Morrison (*Sula*)
- Roxane Gay (*Not That Bad: Dispatches from Rape Culture*)

---

## License

This work is licensed under [Creative Commons Attribution-NoDerivatives 4.0 International (CC BY-ND 4.0)](https://creativecommons.org/licenses/by-nd/4.0/).

**You are free to:**
- Share and redistribute the material in any medium or format

**Under the following terms:**

- **Attribution** — You must give appropriate credit and provide a link to the license
- **NoDerivatives** — You may not remix, transform, or build upon the material for distribution
- 

All artworks © 2021 Malaya Wright. All rights reserved.

---

## Contact

- Website: [malayawonders.info](https://www.malayawonders.info)
- Exhibition page: [Feminist Expression, In Action!](https://www.malayawonders.info/art/feminist-expression-exhibition)

---

*Repository created November 2025 as part of ongoing practice-based research documentation.*