# Barbarian

**General**

```dataviewjs
const classes = dv.pages("#db/class/barbarian")
dv.table(
  [
    'Hit Dice', 'Saving Throws', 'Armor', 'Weapons',
    'Tools', 'Skills Count', 'Skills Options'
  ],
  classes
    .where(
      c => c.Name === 'Barbarian'
    )
    .map(c => [
      c.HitDice, c.AbilityProficiency, c.ArmorProficiency, c.WeaponProficiency,
      c.ToolProficiency, c.SkillProficiency.Quantity, c.SkillProficiency.Options
    ])
)
```

**Progression**

```dataviewjs
const barbarian = dv.pages('#db/class/barbarian').first()
dv.table(
  [
    'Level', 'Proficiency Bonus',
    'Features', 'Rages', 'Rage Damage'
  ],
  barbarian.Levels.map(l => [
    l.Level,
    l.ProficiencyBonus,
    l.Features,
    l.Rages,
    l.RageDamage
  ])
)
```

## Rage

In battle, you fight with primal ferocity. On your turn, you can enter a rage as a bonus action.

While raging, you gain the following benefits if you aren’t wearing heavy armor:

- You have advantage on Strength checks and Strength saving throws.
- When you make a melee weapon attack using Strength, you gain a bonus to the damage roll that increases as you gain levels as a barbarian, as shown in the Rage Damage column of the Barbarian table.
- You have resistance to bludgeoning, piercing, and slashing damage.

If you are able to cast spells, you can’t cast them or concentrate on them while raging.

Your rage lasts for 1 minute. It ends early if you are knocked unconscious or if your turn ends, and you haven’t attacked a hostile creature since your last turn or taken damage since then. You can also end your rage on your turn as a bonus action.

Once you have raged the number of times shown for your barbarian level in the Rages column of the Barbarian table, you must finish a long rest before you can rage again.

## Unarmored Defense

While you are not wearing any armor, your Armor Class equals 10 + your Dexterity modifier + your Constitution modifier. You can use a shield and still gain this benefit.

## Reckless Attack

Starting at 2nd level, you can throw aside all concern for defense to attack with fierce desperation. When you make your first attack on your turn, you can decide to attack recklessly. Doing so gives you advantage on melee weapon attack rolls using Strength during this turn, but attack rolls against you have advantage until your next turn.

## Danger Sense

At 2nd level, you gain an uncanny sense of when things nearby aren’t as they should be, giving you an edge when you dodge away from danger.

You have advantage on Dexterity saving throws against effects that you can see, such as traps and spells. To gain this benefit, you can’t be blinded, deafened, or incapacitated.

## Primal Path

At 3rd level, you choose a path that shapes the nature of your rage. Choose the Path of the Berserker or the Path of the Totem Warrior, both detailed at the end of the class description. Your choice grants you features at 3rd level and again at 6th, 10th, and 14th levels.

## Ability Score Improvement

When you reach 4th level, and again at 8th, 12th, 16th, and 19th level, you can increase one ability score of your choice by 2, or you can increase two ability scores of your choice by 1. As normal, you can’t increase an ability score above 20 using this feature.

## Extra Attack

Beginning at 5th level, you can attack twice, instead of once, whenever you take the Attack action on your turn.

## Fast Movement

Starting at 5th level, your speed increases by 10 feet while you aren’t wearing heavy armor.

## Feral Instinct

By 7th level, your instincts are so honed that you have advantage on initiative rolls.

Additionally, if you are surprised at the beginning of combat and aren’t incapacitated, you can act normally on your first turn, but only if you enter your rage before doing anything else on that turn.

## Brutal Critical

Beginning at 9th level, you can roll one additional weapon damage die when determining the extra damage for a critical hit with a melee attack.

This increases to two additional dice at 13th level and three additional dice at 17th level.

## Relentless Rage

Starting at 11th level, your rage can keep you fighting despite grievous wounds. If you drop to 0 hit points while you’re raging and don’t die outright, you can make a DC 10 Constitution saving throw. If you succeed, you drop to 1 hit point instead.

Each time you use this feature after the first, the DC increases by 5. When you finish a short or long rest, the DC resets to 10.

## Persistent Rage

Beginning at 15th level, your rage is so fierce that it ends early only if you fall unconscious or if you choose to end it.

## Indomitable Might

Beginning at 18th level, if your total for a Strength check is less than your Strength score, you can use that score in place of the total.

## Primal Champion

At 20th level, you embody the power of the wilds. Your Strength and Constitution scores increase by 4. Your maximum for those scores is now 24.

## Primal Paths

### Path of the Berserker

For some barbarians, rage is a means to an end - that end being violence. The Path of the Berserker is a path of untrammeled fury, slick with blood. As you enter the berserker’s rage, you thrill in the chaos of battle, heedless of your own health or well-being.

#### Frenzy

Starting when you choose this path at 3rd level, you can go into a frenzy when you rage. If you do so, for the duration of your rage, you can make a single melee weapon attack as a bonus action on each of your turns after this one. When your rage ends, you suffer one level of exhaustion (as described in appendix A).

#### Mindless Rage

Beginning at 6th level, you can’t be charmed or frightened while raging. If you are charmed or frightened when you enter your rage, the effect is suspended for the duration of the rage.

#### Intimidating Presence

Beginning at 10th level, you can use your action to frighten someone with your menacing presence. When you do so, choose one creature that you can see within 30 feet of you. If the creature can see or hear you, it must succeed on a Wisdom saving throw (DC equal to 8 + your proficiency bonus + your Charisma modifier) or be frightened of you until the end of your next turn. On subsequent turns, you can use your action to extend the duration of this effect on the frightened creature until the end of your next turn. This effect ends if the creature ends its turn out of line of sight or more than 60 feet away from you.

If the creature succeeds on its saving throw, you can’t use this feature on that creature again for 24 hours.

#### Retaliation

Starting at 14th level, when you take damage from a creature that is within 5 feet of you, you can use your reaction to make a melee weapon attack against that creature.

### Path of the Totem Warrior

The Path of the Totem Warrior is a spiritual journey, as the barbarian accepts a spirit animal as guide, protector, and inspiration. In battle, your totem spirit fills you with supernatural might, adding magical fuel to your barbarian rage.

Most barbarian tribes consider a totem animal to be kin to a particular clan, in such cases, it is unusual for an individual to have more than one totem animal spirit, though exceptions exist.

#### Spirit Seeker

Yours is a path that seeks attunement with the natural world, giving you a kinship with beasts. At 3rd level when you adopt this path, you gain the ability to cast the beast sense and speak with animals spells, but only as rituals, as described in chapter 10.

#### Totem Spirit

At the 3rd level, when you adopt this path, you choose a totem spirit and gain its feature. You must make or acquire a physical totem object - an amulet or similar adornment - that incorporates fur or feathers, claws, teeth, or bones of the totem animal. At your option, you also gain minor physical attributes that are reminiscent of your totem spirit. For example, if you have a bear totem spirit, you might be unusually hairy and thick-skinned, or if your totem is the eagle, your eyes turn bright yellow.

Your totem animal might be an animal related to those listed here but more appropriate to your homeland. For example, you could choose a hawk or vulture in place of an eagle.

**Bear**

While raging, you have resistance to all damage except psychic damage. The spirit of the bear makes you tough enough to stand up to any punishment.

**Eagle**

While you're raging and aren't wearing heavy armor, other creatures have disadvantage on opportunity attack rolls against you, and you can use the Dash action as a bonus action on your turn. The spirit of the eagle makes you into a predator who can weave through the fray with ease.

**Wolf**

While you're raging, your friends have advantage on melee attack rolls against any creature within 5 feet of you that is hostile to you. The spirit of the wolf makes you a leader of hunters.

#### Aspect of the Beast

At 6th level, you gain a magical benefit based on the totem animal of your choice. You can choose the same animal you selected at 3rd level or a different one.

**Bear**

You gain the might of a bear. Your carrying capacity (including maximum load and maximum lift) is doubled, and you have advantage on Strength checks made to push, pull, lift, or break objects.

**Eagle**

You gain the eyesight of an eagle. You can see up to 1 mile away with no difficulty and are able to discern even fine details as though looking at something no more than 100 feet away from you. Additionally, dim light doesn't impose disadvantage on your Wisdom (Perception) checks.

**Wolf**

You gain the hunting sensibilities of a wolf. You can track other creatures while traveling at a fast pace, and you can move stealthily while traveling at a normal pace.

#### Spirit Walker

At 10th level, you can cast the commune with nature spell, but only as a ritual. When you do so, a spiritual version of one of the animals you chose for Totem Spirit or Aspect of the Beast appears to you to convey the information you seek.

#### Totemic Attunement

At 14th level, you gain a magical benefit based on a totem animal of your choice. You can choose the same animal you selected previously or a different one.

**Bear**

While you're raging, any creature within 5 feet of you that's hostile to you has disadvantage on attack rolls against targets other than you or another character with this feature. An enemy is immune to this effect if it can't see or hear you or if it can't be frightened. 

**Eagle**

While raging, you have a flying speed equal to your current walking speed. This benefit works only in short bursts; you fall if you end your turn in the air and nothing else is holding you aloft.

**Wolf**

While you're raging, you can use a bonus action on your turn to knock a large or smaller creature prone when you hit it with melee weapon attack.
