---
tags:
  - rules/skill
Skills:
  - Name: "Acrobatics"
    Ability: "Dexterity"
  - Name: "Animal Handling"
    Ability: "Wisdom"
  - Name: "Arcana"
    Ability: "Intelligence"
  - Name: "Athletics"
    Ability: "Strength"
  - Name: "Deception"
    Ability: "Charisma"
  - Name: "History"
    Ability: "Intelligence"
  - Name: "Insight"
    Ability: "Wisdom"
  - Name: "Intimidation"
    Ability: "Charisma"
  - Name: "Investiation"
    Ability: "Intelligence"
  - Name: "Medicine"
    Ability: "Wisdom"
  - Name: "Nature"
    Ability: "Intelligence"
  - Name: "Perception"
    Ability: "Wisdom"
  - Name: "Performance"
    Ability: "Charisma"
  - Name: "Persuasion"
    Ability: "Charisma"
  - Name: "Religion"
    Ability: "Intelligence"
  - Name: "Sleight of Hand"
    Ability: "Dexterity"
  - Name: "Stealth"
    Ability: "Dexterity"
  - Name: "Survival"
    Ability: "Wisdom"
---
# Skills

```dataview
TABLE rows.Skills.Name
FROM #rules/skill
FLATTEN Skills
GROUP BY Skills.Ability
```
