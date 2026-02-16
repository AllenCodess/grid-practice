# CSS GRID CHEAT SHEET – FULL ASCII REFERENCE

GRID COLUMNS – CSS GRID BASICS

Example: 3 columns in a grid container

Columns → 1       2       3
         +-------+-------+-------+
Row 1 →  | Item1 | Item2 | Item3 |
         +-------+-------+-------+
Row 2 →  | Item4 | Item5 | Item6 |
         +-------+-------+-------+
Rows ↓

1️⃣ Fixed Width Columns:
grid-template-columns: 100px 100px 100px;
- Each column is 100px wide

2️⃣ Fraction Units (fr):
grid-template-columns: 1fr 1fr 1fr;
- Each column takes 1 fraction of available space

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
- Columns size to fit their content

---

1️⃣ Columns & Rows Example
Columns → 1       2       3
         +-------+-------+-------+
Row 1 →  | 1-1   | 1-2   | 1-3   |
         +-------+-------+-------+
Row 2 →  | 2-1   | 2-2   | 2-3   |
         +-------+-------+-------+
Row 3 →  | 3-1   | 3-2   | 3-3   |
         +-------+-------+-------+
Rows ↓

- grid-template-columns: repeat(3, 1fr);
- grid-template-rows: repeat(3, 1fr);
- Shorthand: grid-template: repeat(3, 1fr) / repeat(3, 1fr);

---

2️⃣ Grid Auto-Flow

Default (row):

+-------+-------+-------+
| 1     | 2     | 3     |  ← Row 1
+-------+-------+-------+
| 4     | 5     | 6     |  ← Row 2
+-------+-------+-------+

With grid-auto-flow: column:

+-------+-------+
| 1     | 3     |  ← Column 1 & 2
+-------+-------+
| 2     | 4     |
+-------+-------+
| 5     | 6     |
+-------+-------+
Items fill down columns instead of across rows

---

3️⃣ Positioning & Spanning Items

Example: 3x3 grid, 9 items

| Item | CSS                  | Effect                              |
|------|---------------------|-------------------------------------|
| 1    | grid-column: span 2 | Spans 2 columns in Row 1           |
| 3    | grid-row: span 2    | Spans 2 rows in Column 3           |
| 9    | grid-column: span 2 | Spans 2 columns in Row 3           |

ASCII layout with spans:

Columns → 1       2       3
         +-------+-------+-------+
Row 1 →  | Item1 | Item1 | Item2 |
         +-------+-------+-------+
Row 2 →  | Item4 | Item5 | Item3 |
         +-------+-------+-------+
Row 3 →  | Item6 | Item9 | Item9 |
         +-------+-------+-------+
Rows ↓

---

✅ Notes:

- Columns go left → right  
- Rows go top → bottom  
- span X lets an item stretch across X columns/rows  
- Grid lines are numbered starting from 1  
- grid-template shorthand sets rows first, then columns  
- grid-auto-flow controls placement direction (row vs column)  
- Named areas can be used for more complex layouts  
- Column widths can be in px, %, fr, or auto  
- Gaps can be set with gap, grid-row-gap, or grid-column-gap  
- inline-grid: display: inline-grid; behaves like inline-block
