# Command Reference

Complete reference for all Herald commands organized by category.

---

## Command Categories

Herald's commands are organized into logical categories based on their function:

### 🎭 [Character Commands](character.md)

Create, manage, and view your Hunter characters.

- `/create` - Create a new character
- `/delete` - Delete a character
- `/rename` - Rename a character
- `/characters` - List all your characters
- `/sheet` - View character sheet

### 🎲 [Dice Commands](dice.md)

Roll dice using H5E mechanics with or without characters.

- `/roll` - Manual dice roll
- `/roll_char` - Character-based roll
- `/simple` - Simple dice pool
- `/rouse` - Desperation rouse check

### 📈 [Development Commands](development.md)

Improve your character through skills, specialties, and experience.

- `/skill_set` - Set individual skill dots
- `/skill_template` - Apply skill templates
- `/skill_bulk` - Set multiple skills at once
- `/specialty` - Manage skill specialties
- `/specialty_bulk` - Add multiple specialties
- `/xp` - Manage experience points
- `/spend_xp` - Spend XP for improvements
- `/xp_log` - View XP transaction history

### ⚡ [Hunter Mechanics](hunter.md)

Manage H5E-specific Hunter traits and abilities.

- `/edge` - Set Edge rating
- `/desperation` - Track Desperation level
- `/creed` - Set Hunter's Creed
- `/ambition` - Set long-term Ambition
- `/desire` - Set short-term Desire
- `/drive` - Set hunting Drive
- `/damage` - Apply health/willpower damage
- `/heal` - Heal damage

### 🛠️ [Utility Commands](utility.md)

Additional tools and character extras.

- `/equipment` - Manage gear and items
- `/notes` - Character journal and notes
- `/help` - In-Discord help system

---

## Quick Command List

| Command | Description | Example |
|---------|-------------|---------|
| `/create` | Create new character | `/create name:Raven` |
| `/sheet` | View character sheet | `/sheet character:Raven` |
| `/roll_char` | Roll with character stats | `/roll_char character:Raven attribute:Dexterity skill:Stealth` |
| `/roll` | Manual dice roll | `/roll attribute:3 skill:2 difficulty:2` |
| `/skill_set` | Set a skill rating | `/skill_set character:Raven skill:Firearms dots:3` |
| `/specialty` | Add skill specialty | `/specialty character:Raven skill:Firearms specialty:Pistols` |
| `/edge` | Set Edge rating | `/edge character:Raven edge:3` |
| `/desperation` | Set Desperation | `/desperation character:Raven desperation:2` |
| `/xp` | Award experience | `/xp character:Raven amount:5 reason:Session 12` |
| `/help` | Get help | `/help topic:Dice Rolling` |

---

## Command Syntax Conventions

Herald uses Discord's slash command system. Here's how to read command syntax:

### Required Parameters

Parameters without brackets are required:

```
/create name:Raven
```

You must provide a name.

### Optional Parameters

Parameters in `[square brackets]` are optional:

```
/roll_char character:Raven attribute:Dexterity [skill:Stealth]
```

You can include or omit the skill parameter.

### Choices

Some parameters have predefined choices shown in a dropdown:

```
/roll_char attribute:Dexterity  ← Shows dropdown of all 9 attributes
/skill_template template:Balanced  ← Shows: Balanced, Specialist, Jack-of-all-trades
```

### Autocomplete

Character names and skills use autocomplete - start typing and Herald suggests options:

```
/sheet character:Ra  ← Shows "Raven", "Rachel", etc.
```

---

## Command Response Types

Herald responds to commands in two ways:

### Public Responses

Results appear in the channel for everyone to see:

- Dice rolls (by default)
- Character sheets (optional)
- XP awards

### Ephemeral Responses (You Only)

Some responses only you can see:

- Error messages
- Character lists
- Help menus
- Private character sheets (if requested)

!!! tip "Privacy"
    Use the `ephemeral:True` parameter on commands like `/sheet` to keep results private!

---

## Common Command Patterns

### Rolling Dice

```
# Manual roll
/roll attribute:3 skill:2 difficulty:2

# With character
/roll_char character:Raven attribute:Dexterity skill:Firearms difficulty:2

# With Edge
/roll_char character:Raven attribute:Wits skill:Awareness edge:3

# With Desperation
/roll_char character:Raven attribute:Strength skill:Brawl desperation:True
```

### Managing Characters

```
# Create
/create name:Raven strength:2 dexterity:4 intelligence:3

# View
/sheet character:Raven

# Update attributes (through XP or character creation)
/create name:Raven strength:3  # Updates existing character

# Delete
/delete character:Raven
```

### Setting Skills

```
# One at a time
/skill_set character:Raven skill:Firearms dots:3

# Quick template
/skill_template character:Raven template:Balanced

# Multiple skills
/skill_bulk character:Raven skill1:Firearms dots1:3 skill2:Stealth dots2:4
```

---

## Need More Details?

Each command category page provides:

- Detailed parameter descriptions
- Usage examples
- Tips and best practices
- Common mistakes to avoid
- Related commands

Browse the command categories above or use `/help` in Discord for interactive guidance!

---

## Next Steps

- **[Character Commands](character.md)** - Creating and managing characters
- **[Dice Commands](dice.md)** - Rolling dice with H5E mechanics
- **[Development Commands](development.md)** - Character progression
- **[Hunter Mechanics](hunter.md)** - Edge, Desperation, and more
