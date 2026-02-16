## CSS grid practice

GRID COLUMNS – CSS GRID BASICS

Example: 3 columns in a grid container

Columns →    1       2       3
           +-------+-------+-------+
Row 1 →    | Item1 | Item2 | Item3 |
           +-------+-------+-------+
Row 2 →    | Item4 | Item5 | Item6 |
           +-------+-------+-------+
Rows ↓

1️⃣ Fixed Width Columns:
grid-template-columns: 100px 100px 100px;
Each column is 100px wide

2️⃣ Fraction Units (fr):
grid-template-columns: 1fr 1fr 1fr;
Each column takes 1 fraction of available space

3️⃣ Mixed Widths:
grid-template-columns: 200px 1fr 2fr;
- Column 1 = 200px
- Column 2 = 1 fraction
- Column 3 = 2 fractions

4️⃣ Gaps Between Columns/Rows:
grid-row-gap: 1rem;     ← vertical spacing
grid-column-gap: 1rem;  ← horizontal spacing
OR simply:
gap: 1rem;             ← both horizontal & vertical

5️⃣ Auto Columns:
grid-template-columns: auto auto auto;
Columns size to fit their content

---

Notes:
- If more items than columns, items wrap to the next row automatically
- Column widths can be in px, %, fr, or auto
- You can use inline-grid: display: inline-grid; to behave like inline-block
