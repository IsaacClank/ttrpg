---
tags:
  - rules/race/Human
traits:
  - Name: "Ability Score Increase"
    Description: "Your ability scores each increase by 1."
  - Name: "Age"
    Description: "Humans reach adulthood in their late teens and live less than a century."
  - Name: "Alignment"
    Description: "Humans tend toward no particular alignment. The best and the worst are found among them."
  - Name: "Size"
    Description: "Humans vary widely in height and build, from barely 5 feet to well over 6 feet tall. Regardless of your position in that range, your size is Medium."
  - Name: "Speed"
    Description: "Your base walking speed is 30 feet."
  - Name: "Languages"
    Description: "You can speak, read, and write Common and one extra language of your choice. Humans typically learn the languages of other peoples they deal with, including obscure dialects. They are fond of sprinkling their speech with words borrowed from other tongues: Orc curses, Elvish musical expressions, Dwarvish military phrases, and so on."
---
# Human

```dataview
TABLE WITHOUT ID
  traits.Name AS "Trait",
  traits.Description AS "Description"
FROM #rules/race/Human 
FLATTEN traits
```