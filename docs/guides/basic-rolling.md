# Basic Dice Rolling

Learn how to roll dice with Herald using H5E mechanics.

---

## Rolling Methods

Herald offers three ways to roll dice:

### 1. Manual Roll (`/roll`)

Roll dice manually without a character:

```
/roll attribute:3 skill:2 difficulty:2
```

**Best for:**
- Quick rolls
- Rolling for NPCs
- Testing dice mechanics
- When you don't have a character

### 2. Character Roll (`/roll_char`)

Roll using your character's stats:

```
/roll_char character:Raven attribute:Dexterity skill:Firearms difficulty:2
```

**Best for:**
- Regular play
- Character actions
- When you want stat tracking
- Automatic Edge/Desperation

### 3. Simple Roll (`/simple`)

Basic dice pool without H5E mechanics:

```
/simple pool:5
```

**Best for:**
- Non-H5E rolling
- Pure dice pools
- Quick tests

---

## Understanding H5E Dice Mechanics

### Dice Pool

Your dice pool = Attribute + Skill + Modifiers + Edge

```
Dexterity 4 + Firearms 3 + Edge 2 = 9 dice
```

### Successes

- **6-9** = Success (1 success)
- **10** = Critical (2 successes)
- **1-5** = Failure (no success)

### Difficulty

Difficulty is the **target number of successes** you need:

| Difficulty | Description |
|------------|-------------|
| 0 | Automatic (no roll needed) |
| 1 | Simple task |
| 2 | Standard challenge |
| 3 | Hard task |
| 4 | Extreme challenge |
| 5 | Nearly impossible |
| 6+ | Legendary feat |

### Margin

**Margin = Total Successes - Difficulty**

- Margin 0+ = Success
- Margin below 0 = Failure
- Higher margin = Better success

---

## Basic Roll Examples

### Simple Attack Roll

```
/roll_char character:Raven attribute:Dexterity skill:Firearms difficulty:2
```

**Herald shows:**
- Pool calculation (Dexterity 4 + Firearms 3 = 7 dice)
- Dice results with emojis
- Total successes
- Whether you met the difficulty
- Margin of success

### Investigation Check

```
/roll_char character:Raven attribute:Wits skill:Investigation difficulty:3
```

### Stealth Action

```
/roll_char character:Raven attribute:Dexterity skill:Stealth difficulty:2
```

---

## Edge Dice

Edge adds dice to your pool:

### Automatic Edge

Herald automatically adds your character's Edge rating:

```
/roll_char character:Raven attribute:Strength skill:Brawl

# Herald adds Raven's Edge (2) automatically
# Pool = Strength 2 + Brawl 2 + Edge 2 = 6 dice
```

### Override Edge

Override your character's Edge for this roll:

```
/roll_char character:Raven attribute:Strength skill:Brawl edge:4

# Uses Edge 4 instead of Raven's normal Edge 2
```

### No Edge

Roll without Edge:

```
/roll_char character:Raven attribute:Strength skill:Brawl edge:0
```

---

## Desperation Dice

Desperation dice are special - they can cause **messy criticals**!

### When Desperation Triggers

Herald uses your character's Desperation rating to determine when to roll Desperation dice:

```
/roll_char character:Raven attribute:Wits skill:Awareness desperation:True
```

### Messy Criticals

If **Desperation dice** roll 10s:

- You get the successes
- **BUT** something goes wrong
- Storyteller determines the complication

!!! danger "Messy Critical"
    When you see "Messy Critical!" in your roll result, you succeeded but at a cost. The Storyteller will describe what went wrong.

---

## Modifiers

Add or subtract dice from your pool:

### Add Dice

```
/roll_char character:Raven attribute:Dexterity skill:Stealth modifier:2
```

Good for:
- Favorable circumstances
- Equipment bonuses
- Help from allies
- Using specialties (Herald does this automatically!)

### Subtract Dice

```
/roll_char character:Raven attribute:Strength skill:Athletics modifier:-2
```

Good for:
- Penalties
- Poor conditions
- Injuries
- Distractions

---

## Specialties

When your specialty applies, Herald automatically adds +1 die!

### Example

Character has: `Firearms (Pistols)`

```
/roll_char character:Raven attribute:Dexterity skill:Firearms

# If using a pistol, Herald adds +1 automatically
# Storyteller confirms if specialty applies
```

!!! tip "Specialty Bonus"
    Talk to your Storyteller about when specialties apply. Herald tracks them but relies on you to use the right skill!

---

## Reading Roll Results

Herald displays rolls in Inconnu style:

### Result Display

```
═══════════════════════════════
Raven
═══════════════════════════════

3 successes

Dexterity + Firearms = 7 dice

🎲 10 9 6 5 4 3 2

Margin: +1 (met difficulty 2)
═══════════════════════════════
```

**What this means:**

- **Character name** - Who rolled
- **Successes** - How many you got (10=crit, 6-9=success)
- **Pool** - What you rolled
- **Dice** - Individual results
- **Margin** - How much you beat the difficulty by

### Success Types

| Result | Description |
|--------|-------------|
| **Critical!** | Double 10s - exceptional success |
| **X successes** | Standard success |
| **Failure** | Didn't meet difficulty |
| **Messy Critical!** | Success from Desperation 10s - with complication |

---

## Advanced Rolling

### Contested Rolls

Both parties roll, highest successes wins:

```
# Player rolls
/roll_char character:Raven attribute:Dexterity skill:Stealth

# Storyteller rolls for NPC
/roll attribute:3 skill:2 difficulty:0

# Compare totals
```

### Extended Actions

Roll multiple times, accumulating successes:

```
# Session 1
/roll_char character:Raven attribute:Intelligence skill:Investigation
# 2 successes

# Session 2  
/roll_char character:Raven attribute:Intelligence skill:Investigation
# 3 successes (total: 5)

# Keep tracking until you reach goal
```

### Teamwork

Multiple characters help:

```
# Helper rolls first
/roll_char character:Sarah attribute:Intelligence skill:Occult

# Primary actor gets bonus
/roll_char character:Raven attribute:Intelligence skill:Occult modifier:2
```

---

## Common Roll Types

### Combat

```
# Attack
/roll_char character:Raven attribute:Dexterity skill:Firearms difficulty:2

# Defense
/roll_char character:Raven attribute:Dexterity skill:Athletics difficulty:2

# Damage (if hit)
# Usually fixed by weapon, not rolled
```

### Social

```
# Persuasion
/roll_char character:Raven attribute:Manipulation skill:Persuasion difficulty:2

# Intimidation
/roll_char character:Raven attribute:Strength skill:Intimidation difficulty:3

# Insight
/roll_char character:Raven attribute:Wits skill:Empathy difficulty:2
```

### Investigation

```
# Research
/roll_char character:Raven attribute:Intelligence skill:Academics difficulty:3

# Search
/roll_char character:Raven attribute:Wits skill:Investigation difficulty:2

# Track
/roll_char character:Raven attribute:Wits skill:Survival difficulty:3
```

---

## Tips for Better Rolling

### 1. Describe Your Action

Tell the story before rolling:

> "I peek around the corner, trying to spot the vampire without being seen."

```
/roll_char character:Raven attribute:Wits skill:Awareness difficulty:2
```

### 2. Ask About Difficulty

Check with your Storyteller:

> "How hard is this to pick this lock? Difficulty 2 or 3?"

### 3. Consider Edge Usage

Sometimes saving Edge for later is smart:

```
# Save Edge for important rolls
/roll_char character:Raven attribute:Dexterity skill:Stealth edge:0
```

### 4. Track Your Desperation

Know when Desperation might trigger:

> "I'm at Desperation 3, so this roll might be messy..."

---

## Practice Rolls

Try these to get comfortable:

```
# Easy investigation (Difficulty 1)
/roll_char character:YourName attribute:Intelligence skill:Investigation difficulty:1

# Standard combat (Difficulty 2)
/roll_char character:YourName attribute:Dexterity skill:Firearms difficulty:2

# Hard challenge (Difficulty 3)
/roll_char character:YourName attribute:Strength skill:Athletics difficulty:3

# With modifiers
/roll_char character:YourName attribute:Wits skill:Awareness modifier:2 difficulty:2
```

---

## Next Steps

- **[Edge & Desperation Guide](edge-desperation.md)** - Master advanced mechanics
- **[Hunter Mechanics](hunter-mechanics.md)** - Combat, damage, and healing
- **[Command Reference](../commands/dice.md)** - All dice command details

---

!!! question "Questions?"
    - Use `/help topic:Dice Rolling` in Discord
    - Check [Common Issues](../support/common-issues.md)
    - Ask in our [Support Server](https://discord.gg/9bEZk6ARG9)
