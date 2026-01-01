# Hunter: The Reckoning 5E Overview

Welcome to the world of **Hunter: The Reckoning 5th Edition** (H5E), where ordinary people are called to fight against supernatural threats lurking in the shadows. Herald brings this dark modern Gothic setting to Discord, implementing all the core mechanics that make H5E unique.

---

## What is Hunter: The Reckoning?

Hunter: The Reckoning is a tabletop roleplaying game set in the **World of Darkness**, where vampires, werewolves, and other supernatural creatures prey on humanity. You play as a **Hunter** - someone who has received the **Calling**, granting you supernatural insight and abilities to fight back against these monsters.

Unlike other World of Darkness games, Hunters are fundamentally human. You aren't a vampire with centuries of power or a werewolf with preternatural strength. You're a person with a mission, driven by purpose, armed with determination and a willingness to risk everything.

---

## How Herald Implements H5E

Herald is a **complete H5E character management and dice rolling system** for Discord. It handles:

### Core Mechanics

- **Character Creation** - Build Hunters with attributes, skills, and specialties
- **Dice Rolling** - Full H5E d10 pool mechanics with criticals and failures
- **Edge & Desperation** - The supernatural push-and-pull that defines Hunters
- **Creeds & Drives** - Your philosophy and motivation for hunting
- **Damage Tracking** - Health and Willpower with superficial and aggravated damage
- **Character Progression** - Experience points and character advancement

### Hunter-Specific Systems

- **Edge Abilities** - 17 supernatural advantages (Arsenal, Fleet, Sense the Unnatural, etc.)
- **Edge Perks** - Specialized abilities within each Edge
- **Despair System** - The psychological toll of hunting
- **Danger Tracking** - Ongoing supernatural threats
- **Active Character System** - Quick-switch between multiple characters

---

## Key Differences from Tabletop

While Herald implements H5E mechanics faithfully, there are a few differences optimized for Discord play:

### What's the Same

✅ **Dice mechanics** - D10 pools, successes on 6+, critical pairs
✅ **Attributes & Skills** - All 9 attributes and 27 skills
✅ **Edge system** - All 17 Edges with complete Perks lists
✅ **Desperation** - Full Desperation mechanics with Overreach and Despair
✅ **Damage types** - Superficial and Aggravated tracking
✅ **Experience costs** - Official XP advancement rules

### What's Different

⚙️ **Active Character** - Set one character as "active" for streamlined commands
⚙️ **Visual Health/Willpower** - Emoji-based bars for quick status checks
⚙️ **Autocomplete** - Smart dropdown menus for skills, edges, and perks
⚙️ **Automatic calculations** - Health, Willpower, and derived stats auto-update

### What's Not Included

❌ **Combat tracking** - Initiative, positioning, and tactical combat
❌ **Equipment weight/stats** - General inventory tracking only
❌ **Cell management** - Group resources and shared edges
❌ **Storyteller tools** - NPC management, plot tracking

Herald focuses on **character sheets and dice mechanics**, leaving narrative and combat flow to your group's Storyteller.

---

## Quick Start: H5E in Discord

### 1. Create Your Hunter

```
/create name:Sarah Martinez strength:2 dexterity:3 stamina:2
        charisma:3 manipulation:2 composure:3
        intelligence:2 wits:3 resolve:2
```

This creates a character with balanced attributes. Health and Willpower are calculated automatically.

### 2. Set Your Creed

```
/creed action:set
```

Choose from five Creeds (Entrepreneurial, Faithful, Inquisitive, Martial, Underground) that define your hunting approach.

### 3. Set Your Drive

```
/drive action:set
```

Pick what motivates you to hunt (Curiosity, Vengeance, Oath, etc.) and how you find Redemption.

### 4. Add Skills

```
/skill_set skill:Athletics dots:3
/skill_set skill:Firearms dots:2
/skill_set skill:Investigation dots:3
```

Build your character's capabilities across 27 different skills.

### 5. Choose Your Edges

```
/edge action:add
```

Select supernatural advantages that give you an edge (pun intended) against your prey.

### 6. Start Rolling

```
/roll pool:5 difficulty:2 comment:Investigating the warehouse
```

Use H5E's dice mechanics to resolve actions.

---

## Core H5E Concepts

### The Calling

All Hunters have experienced **the Calling** - a moment of supernatural clarity where the monsters became visible. This gift (or curse) lets you:

- **See through the Masquerade** - Detect supernatural creatures
- **Access Edges** - Gain supernatural abilities
- **Push beyond limits** - Use Desperation to achieve the impossible

### The Hunt

Your character exists to **hunt supernatural threats**. This involves:

1. **Investigation** - Finding your prey
2. **Preparation** - Gathering resources and intel
3. **Confrontation** - Facing the monster
4. **Resolution** - Dealing with the aftermath

### The Cost

Hunting exacts a terrible price:

- **Desperation** - The more you use supernatural power, the closer you come to breaking
- **Despair** - Losing yourself to the hunt
- **Danger** - Supernatural threats building up around you
- **Damage** - Physical and mental trauma

Herald tracks all of these mechanics, creating a tense push-and-pull between power and cost.

---

## Herald's H5E Implementation

### Character Sheet Components

Your Hunter character sheet in Herald includes:

#### Identity
- **Name** - Character identifier
- **Creed** - Hunting philosophy (see [Creeds](creeds.md))
- **Drive** - Motivation for hunting (see [Creeds](creeds.md))
- **Ambition** - Long-term goal (recovers Aggravated Willpower)
- **Desire** - Short-term goal (recovers Superficial Willpower)

#### Statistics
- **Attributes** - 9 core attributes (1-5 dots each) (see [Attributes & Skills](attributes-skills.md))
- **Skills** - 27 skills (0-5 dots each) (see [Attributes & Skills](attributes-skills.md))
- **Specialties** - Skill bonuses for specific applications
- **Health** - Physical resilience (Stamina + 3)
- **Willpower** - Mental resilience (Resolve + Composure)

#### Hunter Mechanics
- **Desperation** - Supernatural power rating (0-10) (see [Desperation](desperation.md))
- **Danger** - Ongoing threats (0-10)
- **Edges** - Supernatural abilities (see [Edge](edge.md))
- **Perks** - Edge specializations (see [Edge](edge.md))
- **Despair State** - Psychological breaking point (see [Desperation](desperation.md))

#### Progression
- **Experience** - Total earned, spent, and available XP (see [Progression](progression.md))
- **XP Log** - History of all experience transactions

---

## Rolling Dice in H5E

The core mechanic of H5E is the **dice pool**:

```
Attribute + Skill + Modifiers = Dice Pool
Roll d10s equal to pool size
6+ = Success
Pair of 10s = Critical (adds 2 additional successes)
```

Herald implements all H5E dice mechanics:

- **Standard rolls** - Attribute + Skill
- **Difficulty** - Target number of successes (0-6)
- **Desperation rolls** - Add your Desperation rating as extra dice
- **Messy criticals** - When Desperation dice contribute to a crit
- **Overreach** - Trading success for Danger
- **Despair** - Automatic failure that breaks your Drive

See [Dice Mechanics](dice-mechanics.md) for complete details.

---

## Tracking Damage

Hunters take two types of damage:

### Superficial Damage ⛛
- Minor injuries and stress
- Fills your Health/Willpower track
- Easier to heal

### Aggravated Damage 🔻
- Serious wounds and trauma
- Converts superficial damage to aggravated
- Reduces maximum capacity
- Harder to heal

**Example Health Bar:**
```
🔶🔶🔶⛛⛛🔻▪️▪️▪️▪️ 3/6
(3 undamaged, 2 superficial, 1 aggravated, max 6)
```

When your Health or Willpower reaches 0, your character is incapacitated or broken.

---

## Character Progression

Hunters advance through **Experience Points (XP)**:

### Earning XP
- Awarded by your Storyteller
- Typically 1-3 XP per session
- Bonus XP for accomplishments

### Spending XP
- **Attributes:** New rating × 4 XP
- **Skills:** New rating × 2 XP
- **Specialties:** 3 XP each
- **Edges:** Variable based on type

See [Progression](progression.md) for complete advancement rules.

---

## The Active Character System

Herald's unique **active character** feature streamlines play:

1. Create multiple characters with `/create`
2. Switch between them with `/character`
3. Your active character is used for all commands automatically
4. No need to specify character name every time

This makes it easy to:
- Run multiple characters in different games
- Try different character concepts
- Quickly switch between Hunters in the same chronicle

---

## Herald's Voice: Protocol Established

Herald communicates with an **analytical, present-tense style** that reflects its nature as a supernatural tracking system:

> 🔸 Query recognized
> 🔸 Protocol established
> 🔸 Pattern logged
> 🔸 What are we Hunting?

This distinctive voice creates atmosphere while keeping communication clear and efficient.

---

## Next Steps

Ready to dive deeper into H5E mechanics? Explore these topics:

- **[Attributes & Skills](attributes-skills.md)** - Build your character's capabilities
- **[Dice Mechanics](dice-mechanics.md)** - Master the core resolution system
- **[Edge](edge.md)** - Unlock supernatural advantages
- **[Desperation](desperation.md)** - Understand the cost of power
- **[Creeds](creeds.md)** - Choose your hunting philosophy
- **[Progression](progression.md)** - Advance your Hunter

Or jump straight to the [Command Reference](../commands/index.md) to start playing!

---

## Learning Resources

### New to H5E?
- Start with the [Quick Start Guide](../guides/quickstart.md)
- Try creating [Your First Character](../guides/first-character.md)
- Learn [Basic Dice Rolling](../guides/basic-rolling.md)

### Experienced with H5E?
- Jump to the [Command Reference](../commands/index.md)
- Explore [Advanced Hunter Mechanics](../guides/hunter-mechanics.md)
- Check the [FAQ](../support/faq.md) for quick answers

### Need Help?
- Browse [Common Issues](../support/common-issues.md)
- Visit our [Discord support server](../support/getting-help.md)
- Check the [Troubleshooting Guide](../admin/troubleshooting.md)

---

🔸 **Ready to hunt? Let's begin.**
