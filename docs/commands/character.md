# Character Commands

Character commands handle creating, viewing, switching, and deleting your Hunter characters. These are the core commands you'll use to manage your character data in Herald.

---

## `/create`

Create a new Hunter character sheet.

### Usage

```
/create name:CharacterName [attributes...] [goals...]
```

### Required Parameters

- **`name`** - Character name (2-32 characters, must be unique per user)

### Optional Attribute Parameters

All attributes default to 1 if not specified:

**Physical:**
- **`strength`** - 1-5 (default: 1)
- **`dexterity`** - 1-5 (default: 1)
- **`stamina`** - 1-5 (default: 1)

**Social:**
- **`charisma`** - 1-5 (default: 1)
- **`manipulation`** - 1-5 (default: 1)
- **`composure`** - 1-5 (default: 1)

**Mental:**
- **`intelligence`** - 1-5 (default: 1)
- **`wits`** - 1-5 (default: 1)
- **`resolve`** - 1-5 (default: 1)

### Optional Goal Parameters

- **`ambition`** - Long-term goal (max 200 characters)
- **`desire`** - Short-term goal (max 200 characters)
- **`drive`** - Reason for hunting (max 200 characters)

### Automatic Calculations

Herald automatically sets:
- **Health** = Stamina + 3
- **Willpower** = Resolve + Composure
- **All skills** = 0 (set later with `/skill_set`)
- **Desperation** = 0
- **Danger** = 0
- **Experience** = 0

### Examples

**Minimal creation:**
```
/create name:Sarah Martinez
```
Creates character with all attributes at 1, Health 4, Willpower 2.

**Full creation:**
```
/create name:Marcus Kane
        strength:3 dexterity:3 stamina:2
        charisma:2 manipulation:3 composure:3
        intelligence:2 wits:3 resolve:2
        ambition:"Destroy the vampire court"
        desire:"Find their haven"
```
Creates complete character with custom attributes and goals.

**Balanced hunter:**
```
/create name:Elena Vasquez
        strength:2 dexterity:3 stamina:3
        charisma:3 manipulation:2 composure:2
        intelligence:2 wits:3 resolve:2
```

### Notes

- Character names must be unique per user
- You can create multiple characters
- The new character is automatically set as your active character
- All skills start at 0 - use `/skill_set` to add dots
- See [First Character Guide](../guides/first-character.md) for creation walkthrough

### Common Errors

- **"Name already exists"** - You already have a character with that name
- **"Name too short/long"** - Must be 2-32 characters
- **"Invalid attribute value"** - Attributes must be 1-5

---

## `/character`

View and switch between your characters.

### Usage

```
/character
```

### Parameters

None - this command is interactive.

### Behavior

1. Displays all your characters as buttons
2. Shows which character is currently active (green button)
3. Click a button to set that character as active
4. Inactive characters appear as gray buttons

### Example Display

```
🔸 Your Characters

[✓ Sarah Martinez] (green - currently active)
[Marcus Kane] (gray - inactive)
[Elena Vasquez] (gray - inactive)
```

### The Active Character System

Your **active character** is used automatically in all commands:
- `/sheet` shows active character
- `/roll` uses active character's stats
- `/skill_set` modifies active character
- All commands operate on active character by default

**Why this matters:**
- No need to specify character name in every command
- Quick switching between characters
- Seamless multi-character gameplay

### Switching Characters

Simply click the button for the character you want to make active. Herald confirms the switch and all subsequent commands use that character.

### Use Cases

**Multiple games:**
```
- Sarah (Monday night game)
- Marcus (Wednesday game)
- Elena (Weekend oneshot)
```

**Character concepts:**
```
- Main character
- Backup character
- Experimental build
```

**Different campaigns:**
```
- Street-level hunter
- Corporate infiltrator
- Occult researcher
```

---

## `/sheet`

Display your active character's complete sheet.

### Usage

```
/sheet
```

### Parameters

None - displays active character.

### Display Sections

The character sheet shows:

**1. Header**
```
🔸 Hunter Dossier: Character Name
```

**2. Identity & Goals**
- Creed (if set)
- Drive & Redemption (if set)
- Desire (short-term goal)
- Ambition (long-term goal)

**3. Condition Tracks**
- **Health:** Visual bar with damage types
  - 🔶 Undamaged | ⛛ Superficial | 🔻 Aggravated | ▪️ Empty
  - Shows current/max (e.g., "5/8")
- **Willpower:** Visual bar with damage types
  - 🔷 Undamaged | ⛛ Superficial | 🔻 Aggravated | ▪️ Empty
  - Shows current/max
- **Desperation:** Yellow squares (0-10)
  - 🟨 Filled | ▪️ Empty
  - Shows rating/max
- **Danger:** Red squares (0-10)
  - 🟥 Filled | ▪️ Empty
  - Shows rating/max

**4. Despair Status** (if applicable)
- 💀 Warning that character is in Despair
- Cannot use Desperation dice
- Must complete Redemption

**5. Attributes**
Displayed in three columns:

**Physical:**
- Strength ●●○○○ 2
- Dexterity ●●●○○ 3
- Stamina ●●○○○ 2

**Social:**
- Charisma ●●●○○ 3
- Manipulation ●●○○○ 2
- Composure ●●●○○ 3

**Mental:**
- Intelligence ●●○○○ 2
- Wits ●●●○○ 3
- Resolve ●●○○○ 2

**6. Trained Skills**
Only shows skills with 1+ dots:
```
Physical Skills:
Athletics ●●●○○ 3
Firearms ●●○○○ 2

Mental Skills:
Investigation ●●●○○ 3
Occult ●●○○○ 2
```

**7. Edges** (if any)
Lists all Edges the character has.

**8. Perks** (if any)
Lists all Edge Perks, grouped by Edge.

**9. Footer**
- Tips for using the character
- Links to relevant commands

### Example Output

```
🔸 Hunter Dossier: Sarah Martinez

Creed: Martial ⚔️
Drive: Vengeance (Redemption: Hurt your quarry)
Desire: Find the vampire haven
Ambition: Destroy the vampire court

Health: 🔶🔶🔶⛛⛛▪️ 3/5
Willpower: 🔷🔷🔷🔷🔷 5/5
Desperation: 🟨🟨🟨▪️▪️▪️▪️▪️▪️▪️ 3/10
Danger: 🟥🟥▪️▪️▪️▪️▪️▪️▪️▪️ 2/10

--- Attributes ---
Physical:               Social:                Mental:
Strength ●●○○○ 2       Charisma ●●○○○ 2      Intelligence ●●○○○ 2
Dexterity ●●●○○ 3      Manipulation ●●○○○ 2   Wits ●●●○○ 3
Stamina ●●○○○ 2        Composure ●●●○○ 3      Resolve ●●○○○ 2

--- Trained Skills ---
Physical Skills:
Athletics ●●●○○ 3
Firearms ●●●○○ 3 [Pistols, Rifles]
Stealth ●●○○○ 2

Mental Skills:
Investigation ●●●○○ 3
Occult ●●○○○ 2

--- Edges ---
Arsenal, Sense the Unnatural

--- Perks ---
Arsenal: Exotics, Untraceable
Sense the Unnatural: Creature Specialization, Range
```

### Use Cases

- Quick reference during play
- Showing your character to others
- Planning improvements
- Verifying stats before rolls

---

## `/delete`

Delete your active character.

### Usage

```
/delete
```

### Parameters

None - deletes active character.

### Behavior

1. Shows confirmation dialog with character name
2. Requires clicking "Confirm Delete" button
3. Timeout after 30 seconds (auto-cancels)
4. Permanently removes character and ALL associated data

### Confirmation Dialog

```
⚠️ Delete Character: Sarah Martinez

This will permanently delete this character and all associated data.
This action cannot be undone.

[Confirm Delete] [Cancel]
```

### What Gets Deleted

Permanently removes:
- Character sheet
- All skills
- All Edges and Perks
- All specialties
- XP log history
- Everything associated with the character

### After Deletion

- If you have other characters, one becomes active automatically
- If this was your only character, you'll need to `/create` a new one
- No way to recover deleted characters

### Safety Features

- **Confirmation required** - Can't accidentally delete
- **30-second timeout** - Dialog expires if no action
- **Clear warnings** - Multiple reminders about permanence

### Use Cases

- Removing old/unused characters
- Starting fresh with new concept
- Cleaning up test characters

!!! danger "Warning"
    Deletion is permanent. There is no undo. Make sure you want to delete before confirming.

---

## `/about`

Display information about Herald bot.

### Usage

```
/about
```

### Parameters

None.

### Display Information

Shows:
- Bot name and version
- Description of Herald's purpose
- Link to GitHub repository
- Link to documentation website
- Discord support server (if configured)
- Credits and attribution

### Example Output

```
🔸 Herald - Hunter: The Reckoning 5E Bot

A Discord bot for managing Hunter: The Reckoning 5th Edition
characters and dice mechanics.

Features:
✓ Complete H5E character management
✓ Full dice rolling with Desperation mechanics
✓ Edge and Perk tracking
✓ Experience and progression system
✓ Active character system for easy multi-character play

GitHub: https://github.com/Mashbybot/herald
Documentation: https://herald-docs.example.com
Support: discord.gg/herald-support

Built by Mashbybot
Inspired by Inconnu (Vampire: The Masquerade bot by Tiltowait)

🔸 What are we Hunting?
```

### Use Cases

- Getting bot information
- Finding documentation link
- Joining support server
- Checking version
- Sharing bot details with others

---

## Quick Command Reference

### Character Management Commands

```bash
# Create new character
/create name:"Name" strength:3 dexterity:3 ...

# Switch characters (interactive)
/character

# View character sheet
/sheet

# Delete active character (with confirmation)
/delete

# Bot information
/about
```

### Command Flow

**Starting Fresh:**
```
1. /create name:"Your Character"
2. /skill_set skill:Firearms dots:3
3. /creed action:set
4. /drive action:set
5. /sheet (verify)
```

**Multiple Characters:**
```
1. /create name:"Character 1"
   (set up character 1)
2. /create name:"Character 2"
   (set up character 2)
3. /character (switch between them)
4. /sheet (view current)
```

**Daily Usage:**
```
1. /character (switch if needed)
2. /sheet (check stats)
3. /roll pool:X (play!)
```

---

## Common Workflows

### Creating Your First Character

```
Step 1: Create
/create name:"Sarah Martinez"
        strength:2 dexterity:3 stamina:3
        charisma:3 manipulation:2 composure:2
        intelligence:2 wits:3 resolve:2

Step 2: Add skills
/skill_set skill:Firearms dots:3
/skill_set skill:Athletics dots:2
/skill_set skill:Investigation dots:3

Step 3: Add specialties
/specialty action:add skill:Firearms specialty:Pistols

Step 4: Set identity
/creed action:set (select Martial)
/drive action:set (select Vengeance)
/ambition ambition:"Destroy the vampire court"
/desire desire:"Find their haven"

Step 5: Check sheet
/sheet
```

### Managing Multiple Characters

```
Monday game (Sarah):
/character (select Sarah)
/sheet
(play session)

Wednesday game (Marcus):
/character (select Marcus)
/sheet
(play session)

Weekend (new character):
/create name:"Test Character" ...
```

### Cleaning Up Old Characters

```
/character (select old character)
/sheet (verify it's the right one)
/delete (confirm deletion)
/character (select your main character)
```

---

## Tips & Best Practices

### Character Creation

- **Plan before creating** - Know your concept
- **Use descriptive names** - Easy to identify
- **Set goals early** - Ambition and Desire provide recovery
- **Don't min-max** - Balanced characters are more fun

### Active Character

- **Check before important actions** - Make sure right character is active
- **Name characters clearly** - Easy to distinguish
- **Use `/sheet` frequently** - Verify active character

### Organization

- **Limit characters** - 2-3 active characters max
- **Delete unused** - Keep list clean
- **Consistent naming** - Easy to remember

### Safety

- **Double-check before `/delete`** - No undo
- **Export important characters** - (Future feature)
- **Keep notes externally** - Backup important details

---

## Related Commands

- **[Development Commands](development.md)** - `/attributes`, `/skill_set`, `/specialty`, `/xp`
- **[Hunter Commands](hunter.md)** - `/creed`, `/drive`, `/edge`, `/perks`
- **[Dice Commands](dice.md)** - `/roll`, `/danger`

Or return to [Command Reference Overview](index.md).

---

🔸 **Create your Hunter. Begin your chronicle.**
