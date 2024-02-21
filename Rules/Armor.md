---
tags:
  - rules/armor
Armor:
  - Type: Padded
    Cost:
      - Value: 5
        Currency: gp
    ArmorClassBase: 11
    ArmorClassModifierAbility: Dexterity
    Requirements:
    Disadvantages:
      - Name: Stealth
    Weight:
      Value: 8
      Metric: lb
    WeightClass: Light
  - Type: Leather
    Cost:
      - Value: 10
        Currency: gp
    ArmorClassBase: 11
    ArmorClassModifierAbility: Dexterity
    Requirements:
    Disadvantages:
    Weight:
      Value: 10
      Metric: lb
    WeightClass: Light
  - Type: Studded leather
    Cost:
      - Value: 45
        Currency: gp
    ArmorClassBase: 12
    ArmorClassModifierAbility: Dexterity
    Requirements:
    Disadvantages:
    Weight:
      Value: 13
      Metric: lb
    WeightClass: Light
  - Type: Hide
    Cost:
      - Value: 10
        Currency: gp
    ArmorClassBase: 12
    ArmorClassModifierAbility: Dexterity
    Requirements:
    Disadvantages:
    Weight:
      Value: 12
      Metric: lb
    WeightClass: Medium
  - Type: Chain shirt
    Cost:
      - Value: 50
        Currency: gp
    ArmorClassBase: 13
    ArmorClassModifierAbility: Dexterity
    Requirements:
    Disadvantages:
    Weight:
      Value: 20
      Metric: lb
    WeightClass: Medium
  - Type: Scale mail
    Cost:
      - Value: 50
        Currency: gp
    ArmorClassBase: 14
    ArmorClassModifierAbility: Dexterity
    Requirements:
    Disadvantages:
      - Name: Stealth
    Weight:
      Value: 45
      Metric: lb
    WeightClass: Medium
  - Type: Breastplate
    Cost:
      - Value: 400
        Currency: gp
    ArmorClassBase: 14
    ArmorClassModifierAbility: Dexterity
    Requirements:
    Disadvantages:
    Weight:
      Value: 20
      Metric: lb
    WeightClass: Medium
  - Type: Half plate
    Cost:
      - Value: 750
        Currency: gp
    ArmorClassBase: 15
    ArmorClassModifierAbility: Dexterity
    Requirements:
    Disadvantages:
      - Name: Stealth
    Weight:
      Value: 40
      Metric: lb
    WeightClass: Medium
  - Type: Ring mail
    Cost:
      - Value: 30
        Currency: gp
    ArmorClassBase: 14
    Requirements:
    Disadvantages:
      - Name: Stealth
    Weight:
      Value: 40
      Metric: lb
    WeightClass: Heavy
  - Type: Chain mail
    Cost:
      - Value: 75
        Currency: gp
    ArmorClassBase: 16
    Requirements:
      - Name: Strength
        Value: 13
    Disadvantages:
      - Name: Stealth
    Weight:
      Value: 55
      Metric: lb
    WeightClass: Heavy
  - Type: Splint
    Cost:
      - Value: 200
        Currency: gp
    ArmorClassBase: 17
    Requirements:
      - Name: Strength
        Value: 15
    Disadvantages:
      - Name: Stealth
    Weight:
      Value: 60
      Metric: lb
    WeightClass: Heavy
  - Type: Plate
    Cost:
      - Value: 1,500
        Currency: gp
    ArmorClassBase: 18
    Requirements:
      - Name: Strength
        Value: 15
    Disadvantages:
      - Name: Stealth
    Weight:
      Value: 65
      Metric: lb
    WeightClass: Heavy
  - Type: Shield
    Cost:
      - Value: 10
        Currency: gp
    ArmorClassBase: +2
    Requirements:
    Disadvantages:
    Weight:
      Value: 6
      Metric: lb
    WeightClass: Heavy
---
# Armor

```dataview
TABLE WITHOUT ID
  Armor.Type AS "Type",
  Armor.WeightClass AS "Weight Class",
  string(Armor.Weight.Value) + " " + Armor.Weight.Metric AS "Weight",
  map(filter(Armor.Cost, (c) => c.Currency = "gp"), (c) => c.Value) AS "Cost (gp)",
  Armor.ArmorClassBase AS "AC Base",
  substring(Armor.ArmorClassModifierAbility, 0, 3) AS "AC Modifier",
  string(Armor.Requirements.Value) + " " + substring(Armor.Requirements.Name, 0, 3) AS "Requirements",
  Armor.Disadvantages.Name AS "Disadvantages"
FROM #rules/armor
FLATTEN Armor
```