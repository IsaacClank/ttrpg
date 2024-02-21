---
tags:
  - db/class/{{class_name}}
Name: "{{class_name}}"
HitDice: "{{hit_dice}}"
AbilityProficiency:
ArmorProficiency:
WeaponProficiency:
ToolProficiency:
SkillProficiency:
  Quantity:
  Options:
Levels:
---
# {{class_name}}

**General**

```dataview
TABLE WITHOUT ID
  HitDice AS "Hit Dice",
  AbilityProficiency AS "Saving Throws",
  ArmorProficiency AS "Armor",
  WeaponProficiency AS "Weapons",
  ToolProficiency AS "Tools",
  SkillProficiency.Quantity AS "Skills Count",
  SkillProficiency.Options AS "Skills Options"
FROM #db/class/{{class_name}} 
```

**Progression**

```dataview
TABLE WITHOUT ID
  Levels.Level AS Level,
  Levels.ProficiencyBonus AS "Proficiency Bonus",
  Levels.Features AS "Features"
FROM #db/class/{{class_name}} 
FLATTEN Levels
```