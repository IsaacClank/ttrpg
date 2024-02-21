---
tags:
  - db/class/Monk
Name: "Monk"
HitDice: "1d8"
AbilityProficiency: 
  - Strength
  - Dexterity
ArmorProficiency:
WeaponProficiency:
  - Simple
  - Shortsword
ToolProficiency: 
  - 1 Artisan
  - or
  - 1 Musical Instrument
SkillProficiency:
  Quantity: 2
  Options:
    - Acrobatics
    - Athletics
    - History
    - Insight
    - Religion
    - Stealth
Levels:
  - Level: 1
    ProficiencyBonus: 2
    MartialArts: 1d4
    KiPoints: 
    UnarmoredMovement: 
    Features:
      - Unarmored Defense
      - Martial Arts
  - Level: 2
    ProficiencyBonus: 2
    MartialArts: 1d4
    KiPoints: 2
    UnarmoredMovement: 10
    Features:
      - Ki
      - Unarmored Movement
  - Level: 3
    ProficiencyBonus: 2
    MartialArts: 1d4
    KiPoints: 3
    UnarmoredMovement: 10
    Features:
      - Monastic Tradition
      - Deflect Missiles
  - Level: 4
    ProficiencyBonus: 2
    MartialArts: 1d4
    KiPoints: 4
    UnarmoredMovement: 10
    Features:
      - Ability Score Improvement
      - Slow Fall
  - Level: 5
    ProficiencyBonus: 3
    MartialArts: 1d6
    KiPoints: 5
    UnarmoredMovement: 10
    Features:
      - Extra Attack
      - Stunning Strike
  - Level: 6
    ProficiencyBonus: 3
    MartialArts: 1d6
    KiPoints: 6
    UnarmoredMovement: 15
    Features:
      - Ki-Empowered Strikes
      - Monastic Tradition Feature
  - Level: 7
    ProficiencyBonus: 3
    MartialArts: 1d6
    KiPoints: 7
    UnarmoredMovement: 15
    Features:
      - Evasion
      - Stillness of Mind
  - Level: 8
    ProficiencyBonus: 3
    MartialArts: 1d6
    KiPoints: 8
    UnarmoredMovement: 15
    Features:
      - Ability Score Improvement
  - Level: 9
    ProficiencyBonus: 4
    MartialArts: 1d6
    KiPoints: 9
    UnarmoredMovement: 15
    Features:
      - Unarmored Movement improvement
  - Level: 10
    ProficiencyBonus: 4
    MartialArts: 1d6
    KiPoints: 10
    UnarmoredMovement: 20
    Features:
      - Purity of Body
  - Level: 11
    ProficiencyBonus: 4
    MartialArts: 1d8
    KiPoints: 11
    UnarmoredMovement: 20
    Features:
      - Monastic Tradition Feature
  - Level: 12
    ProficiencyBonus: 4
    MartialArts: 1d8
    KiPoints: 12
    UnarmoredMovement: 20
    Features:
      - Ability Score Improvement
  - Level: 13
    ProficiencyBonus: 5
    MartialArts: 1d8
    KiPoints: 13
    UnarmoredMovement: 20
    Features:
      - Tongue of the Sun and Moon
  - Level: 14
    ProficiencyBonus: 5
    MartialArts: 1d8
    KiPoints: 14
    UnarmoredMovement: 25
    Features:
      - Diamond Soul
  - Level: 15
    ProficiencyBonus: 5
    MartialArts: 1d8
    KiPoints: 15
    UnarmoredMovement: 25
    Features:
      - Timeless Body
  - Level: 16
    ProficiencyBonus: 5
    MartialArts: 1d8
    KiPoints: 16
    UnarmoredMovement: 25
    Features:
      - Ability Score Improvement
  - Level: 17
    ProficiencyBonus: 6
    MartialArts: 1d10
    KiPoints: 17
    UnarmoredMovement: 25
    Features:
      - Monastic Tradition Feature
  - Level: 18
    ProficiencyBonus: 6
    MartialArts: 1d10
    KiPoints: 18
    UnarmoredMovement: 30
    Features:
      - Empty Body
  - Level: 19
    ProficiencyBonus: 6
    MartialArts: 1d10
    KiPoints: 19
    UnarmoredMovement: 30
    Features:
      - Ability Score Improvement
  - Level: 20
    ProficiencyBonus: 6
    MartialArts: 1d10
    KiPoints: 20
    UnarmoredMovement: 30
    Features:
      - Perfect Self
---
# Monk

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
FROM #db/class/Monk 
```

**Progression**

```dataview
TABLE WITHOUT ID
  Levels.Level AS Level,
  Levels.ProficiencyBonus AS "Proficiency Bonus",
  Levels.Features AS "Features",
  Levels.MartialArts AS "Martial Arts",
  Levels.KiPoints AS "Ki Points",
  Levels.UnarmoredMovement AS "Unarmored Movement"
FROM #db/class/Monk 
FLATTEN Levels
```