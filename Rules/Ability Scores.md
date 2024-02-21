---
tags:
  - rules/ability
Abilities:
  - Strength
  - Dexterity
  - Constitution
  - Intelligence
  - Wisdom
  - Charisma
AbilityToModifier:
  - Key: 1
    Value: -5
  - Key: 2
    Value: -4
  - Key: 3
    Value: -4
  - Key: 4
    Value: -3
  - Key: 5
    Value: -3
  - Key: 6
    Value: -2
  - Key: 7
    Value: -2
  - Key: 8
    Value: -1
  - Key: 9
    Value: -1
  - Key: 10
    Value: 0
  - Key: 11
    Value: 0
  - Key: 12
    Value: 1
  - Key: 13
    Value: 1
  - Key: 14
    Value: 2
  - Key: 15
    Value: 2
  - Key: 16
    Value: 3
  - Key: 17
    Value: 3
  - Key: 18
    Value: 4
  - Key: 19
    Value: 4
  - Key: 20
    Value: 5
  - Key: 21
    Value: 5
  - Key: 22
    Value: 6
  - Key: 23
    Value: 6
  - Key: 24
    Value: 7
  - Key: 25
    Value: 7
  - Key: 26
    Value: 8
  - Key: 27
    Value: 8
  - Key: 28
    Value: 9
  - Key: 29
    Value: 9
  - Key: 30
    Value: 10
DifficultyClasses:
  - 5
  - 10
  - 15
  - 20
  - 25
  - 30
---

# Abilities

```dataview
LIST WITHOUT ID
  Abilities
FROM #rules/ability
FLATTEN Abilities
```

## Ability Scores and Modifiers

```dataview
TABLE WITHOUT ID
  AbilityToModifier.Key AS "Ability Score",
  AbilityToModifier.Value AS "Modifier"
FROM #rules/ability
FLATTEN AbilityToModifier
```
