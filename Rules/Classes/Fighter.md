---
tags:
  - db/class/Fighter
Name: "Fighter"
HitDice: "1d10"
AbilityProficiency: 
  - Strength
  - Constitution
ArmorProficiency: 
  - Light
  - Medium
  - Heavy
  - Shield
WeaponProficiency: 
  - Simple
  - Martial
ToolProficiency:
SkillProficiency: 
  Quantity: 2
  Options:
    - Acrobatics
    - Animal Handling
    - Athletics
    - History
    - Insight
    - Intimidation
    - Perception
    - Survival
Levels:
  - Level: 1
    ProficiencyBonus: 2
    Features:
      - Fighting Style
      - Second Wind
  - Level: 2
    ProficiencyBonus: 2
    Features:
      - Action Surge (one use)
  - Level: 3
    ProficiencyBonus: 2
    Features:
      - Martial Archetype
  - Level: 4
    ProficiencyBonus: 2
    Features:
      - Ability Score Improvement
  - Level: 5
    ProficiencyBonus: 3
    Features:
      - Extra Attack
  - Level: 6
    ProficiencyBonus: 3
    Features:
      - Ability Score Improvement
  - Level: 7
    ProficiencyBonus: 3
    Features:
      - Martial Archetype Feature
  - Level: 8
    ProficiencyBonus: 3
    Features:
      - Ability Score Improvement
  - Level: 9
    ProficiencyBonus: 4
    Features:
      - Indomitable (one use)
  - Level: 10
    ProficiencyBonus: 4
    Features:
      - Martial Archetype Feature
  - Level: 11
    ProficiencyBonus: 4
    Features:
      - Extra Attack (2)
  - Level: 12
    ProficiencyBonus: 4
    Features:
      - Ability Score Improvement
  - Level: 13
    ProficiencyBonus: 5
    Features:
      - Indomitable (two uses)
  - Level: 14
    ProficiencyBonus: 5
    Features:
      - Ability Score Improvement
  - Level: 15
    ProficiencyBonus: 5
    Features:
      - Martial Archetype Feature
  - Level: 16
    ProficiencyBonus: 5
    Features:
      - Ability Score Improvement
  - Level: 17
    ProficiencyBonus: 6
    Features:
      - Action Surge (two uses)
      - Indomitable (three uses)
  - Level: 18
    ProficiencyBonus: 6
    Features:
      - Martial Archetype Feature
  - Level: 19
    ProficiencyBonus: 6
    Features:
      - Ability Score Improvement
  - Level: 20
    ProficiencyBonus: 6
    Features:
      - Extra Attack (3)
---
# Fighter

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
FROM #db/class/Fighter
```

**Progression**

```dataview
TABLE WITHOUT ID
  Levels.Level AS Level,
  Levels.ProficiencyBonus AS "Proficiency Bonus",
  Levels.Features AS "Features"
FROM #db/class/Fighter 
FLATTEN Levels
```

## Fighting Style

You adopt a particular style of fighting as your specialty. Choose one of the following options. You can't take a Fighting Style option more than once, even if you later get to choose again.

### Archery

You gain a +2 bonus to attack rolls you make with ranged weapons.

### Defense

While you are wearing armor, you gain a +1 bonus to AC.

### Dueling

When you are wielding a melee weapon in one hand and no other weapons, you gain a +2 bonus to damage rolls with that weapon.

### Great Weapon Fighting

When you roll a 1 or 2 on a damage die for an attack you make with a melee weapon that you are wielding with two hands, you can reroll the die and must use the new roll, even if the new roll is a 1 or a 2. The weapon must have the two-handed or versatile property for you to gain this benefit.

### Protection

When a creature you can see attacks a target other than you that is within 5 feet of you, you can use your reaction to impose disadvantage on the attack roll. You must be wielding a shield.

### Two-Weapon Fighting

When you engage in two-weapon fighting, you can add your ability modifier to the damage of the second attack.

## Second Wind

You have a limited well of stamina that you can draw on to protect yourself from harm. On your turn, you can use a bonus action to regain hit points equal to 1d10 + your fighter level. Once you use this feature, you must finish a short or long rest before you can use it again.

## Action Surge

Starting at 2nd level, you can push yourself beyond your normal limits for a moment. On your turn, you can take one additional action on top of your regular action and a possible bonus action.

Once you use this feature, you must finish a short or long rest before you can use it again. Starting at 17th level, you can use it twice before a rest, but only once on the same turn.

## Martial Archetype

At 3rd level, you choose an archetype that you strive to emulate in your combat styles and techniques. Choose Champion, Battle Master, or Eldritch Knight, all detailed at the end of the class description. The archetype you choose grants you features at 3rd level and again at 7th, 10th, 15th, and 18th level.

## Ability Score Improvement

When you reach 4th level, and again at 6th, 8th, 12th, 14th, 16th, and 19th level, you can increase one ability score of your choice by 2, or you can increase two ability scores of your choice by 1. As normal, you can't increase an ability score above 20 using this feature.

## Extra Attack

Beginning at 5th level, you can attack twice, instead of once, whenever you take the Attack action on your turn.

The number of attacks increases to three when you reach 11th level in this class and to four when you reach 20th level in this class.

## Indomitable

Beginning at 9th level, you can reroll a saving throw that you fail. If you do so, you must use the new roll, and you can't use this feature again until you finish a long rest.

You can use this feature twice between long rests starting at 13th level and three times between long rests starting at 17th level.

## Martial Archetypes

Different fighters choose different approaches to perfecting their fighting prowess. The martial archetype you choose to emulate reflects your approach.

### Champion

The archetypal Champion focuses on the development of raw physical power honed to deadly perfection. Those who model themselves on this archetype combine rigorous training with physical excellence to deal devastating blows.

#### Improved Critical

Beginning when you choose this archetype at 3rd level, your weapon attacks score a critical hit on a roll of 19 or 20.

#### Remarkable Athlete

Starting at 7th level, you can add half your proficiency bonus (round up) to any Strength, Dexterity, or Constitution check you make that doesn't already use your proficiency bonus.

In addition, when you make a running long jump, the distance you can cover increases by a number of feet equal to your Strength modifier.

#### Additional Fighting Style

At 10th level, you can choose a second option from the Fighting Style class feature.

#### Superior Critical

Starting at 15th level, your weapon attacks score a critical hit on a roll of 18-20.

#### Survivor

At 18th level, you attain the pinnacle of resilience in battle. At the start of each of your turns, you regain hit points equal to 5 + your Constitution modifier if you have no more than half of your hit points left. You don't gain this benefit if you have 0 hit points.

### Battle Master

#### Combat Superiority

#### Student of War

#### Know Your Enemy

#### Maneuvers

### Eldritch Knight

#### Spell Casting

#### War Magic

#### Eldritch Strike

#### Arcane Charge

#### Improved War Magic