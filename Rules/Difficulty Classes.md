---
tags:
  - rules/difficulty
Classes:
  - Value: 5
    Description: "Very easy"
  - Value: 10
    Description: "Easy"
  - Value: 15
    Description: "Medium"
  - Value: 20
    Description: "Hard"
  - Value: 25
    Description: "Very hard"
  - Value: 30
    Description: "Nearly impossible"
---
# Difficulty Classes

```dataview
TABLE WITHOUT ID
  Classes.Description AS "Difficulty",
  Classes.Value AS "Difficulty Class (DC)"
FROM #rules/difficulty
FLATTEN Classes
```