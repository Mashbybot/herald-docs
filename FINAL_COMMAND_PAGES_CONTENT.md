# Remaining Command Pages - Complete Content

This document contains the full content for the final 3 command reference pages. Copy each section to its respective file.

---

## FILE: docs/commands/hunter.md

```markdown
# Hunter Commands

Hunter-specific commands manage your character's supernatural abilities, identity, and condition. These commands handle Desperation, Edges, Creeds, Drives, and damage tracking.

---

## Damage & Healing Commands

### `/damage`

Apply damage to Health or Willpower.

**Usage:**
```
/damage track:TRACK amount:X damage_type:TYPE
```

**Parameters:**
- `track` (required): health, willpower
- `amount` (required): Damage amount (1-10)
- `damage_type` (required): superficial, aggravated

**Examples:**
```
/damage track:health amount:3 damage_type:superficial
/damage track:willpower amount:2 damage_type:aggravated
```

**Damage Types:**
- **Superficial (⛛)** - Fills empty track spaces
- **Aggravated (🔻)** - Converts superficial to aggravated, reduces capacity

---

### `/heal`

Heal damage from Health or Willpower.

**Usage:**
```
/heal track:TRACK heal_type:TYPE [amount:X]
```

**Parameters:**
- `track` (required): health, willpower
- `heal_type` (required): all, superficial, aggravated
- `amount` (optional): Required for superficial/aggravated

**Examples:**
```
/heal track:health heal_type:all
/heal track:willpower heal_type:superficial amount:2
/heal track:health heal_type:aggravated amount:1
```

---

## Hunter Identity Commands

### `/desperation`

Manage Desperation rating.

**Usage:**
```
/desperation action:ACTION [amount:X]
```

**Actions:** view, set, add, subtract

**Examples:**
```
/desperation action:view
/desperation action:set amount:5
```

---

### `/creed`

Set your Hunter Creed.

**Usage:**
```
/creed action:ACTION
```

**Actions:**
- `view` - Show current Creed
- `set` - Interactive selection of Creed

**Creeds:**
- Entrepreneurial 🔨, Faithful ✝️, Inquisitive 🔍, Martial ⚔️, Underground 🎭

---

### `/drive`

Set your Drive and Redemption.

**Usage:**
```
/drive action:ACTION
```

**Actions:**
- `view` - Show current Drive
- `set` - Interactive selection

**Drives:**
- Curiosity, Vengeance, Oath, Greed, Pride, Envy, Atonement

---

### `/ambition`

Set long-term goal.

**Usage:**
```
/ambition ambition:"Your long-term goal"
```

Recovers 1 Aggravated Willpower when progress made.

---

### `/desire`

Set short-term goal.

**Usage:**
```
/desire desire:"Your short-term goal"
```

Recovers 1 Superficial Willpower when accomplished.

---

## Edge & Perks Commands

### `/edge`

Manage Hunter Edges.

**Usage:**
```
/edge action:ACTION [edge_name:NAME]
```

**Actions:**
- `view` - Show all Edges
- `add` - Interactive selection (17 Edges)
- `remove` - Remove an Edge

**Examples:**
```
/edge action:view
/edge action:add
/edge action:remove
```

---

### `/perks`

Manage Edge Perks.

**Usage:**
```
/perks action:ACTION [edge_name:NAME] [perk_name:NAME]
```

**Actions:**
- `view` - Show all Perks
- `add` - Add Perk to Edge (autocomplete)
- `remove` - Remove Perk

**Examples:**
```
/perks action:view
/perks action:view edge_name:Arsenal
/perks action:add edge_name:Arsenal perk_name:Exotics
/perks action:remove edge_name:Arsenal perk_name:Exotics
```

---

## Despair Commands

### `/despair`

Enter Despair state.

**Usage:**
```
/despair
```

Marks character as in Despair. Cannot use Desperation, Drive unusable.

---

### `/redemption`

Exit Despair state after completing Redemption.

**Usage:**
```
/redemption
```

Use after Storyteller confirms you've completed your Redemption path.

---

🔸 **Manage your Hunter. Track your condition. Face Despair.**
```

---

## FILE: docs/commands/development.md

```markdown
# Development Commands

Development commands handle character progression: improving attributes, raising skills, adding specialties, and managing experience points.

---

## `/attributes`

Set attribute ratings.

**Usage:**
```
/attributes attribute:NAME dots:X
```

**Parameters:**
- `attribute` (required): strength, dexterity, stamina, charisma, manipulation, composure, intelligence, wits, resolve
- `dots` (required): 1-5

**Auto-Calculations:**
- Stamina change → Health = Stamina + 3
- Composure/Resolve change → Willpower = Resolve + Composure

**Examples:**
```
/attributes attribute:Dexterity dots:4
/attributes attribute:Strength dots:3
```

**XP Cost:**
New rating × 4 XP (automatically deducted if XP available)

---

## `/skill_set`

Set skill dots.

**Usage:**
```
/skill_set skill:NAME dots:X
```

**Parameters:**
- `skill` (required): Dropdown with all 27 skills
- `dots` (required): 0-5

**Skills:**
- **Physical:** Athletics, Brawl, Craft, Driving, Firearms, Larceny, Melee, Stealth, Survival
- **Social:** Animal Ken, Etiquette, Insight, Intimidation, Leadership, Performance, Persuasion, Streetwise, Subterfuge
- **Mental:** Academics, Awareness, Finance, Investigation, Medicine, Occult, Politics, Science, Technology

**Examples:**
```
/skill_set skill:Firearms dots:3
/skill_set skill:Investigation dots:4
```

**XP Cost:**
New rating × 2 XP (automatically deducted)

---

## `/specialty`

Manage skill specialties.

**Usage:**
```
/specialty action:ACTION [skill:NAME] [specialty:NAME]
```

**Actions:**
- `view` - Show all specialties
- `add` - Add specialty to skill
- `remove` - Remove specialty

**Requirements:**
- Skill must have 1+ dots
- Max specialties = skill dots (minimum 1)

**Examples:**
```
/specialty action:view
/specialty action:add skill:Firearms specialty:Pistols
/specialty action:remove skill:Firearms specialty:Pistols
```

**XP Cost:**
3 XP each (automatically deducted)

---

## `/xp`

Manage experience points.

**Usage:**
```
/xp action:ACTION [amount:X] [reason:"text"]
```

**Actions:**
- `view` - Show XP totals and history
- `add` - Add XP (Storyteller)
- `spend` - Manually spend XP
- `set` - Set total XP (Storyteller)

**Examples:**
```
/xp action:view
/xp action:add amount:3 reason:"Session XP"
/xp action:spend amount:15 reason:"Purchased Edge"
/xp action:set amount:50
```

**XP Tracking:**
- Total Earned
- Spent
- Available = Total - Spent
- Full transaction log

**Costs:**
- Attributes: New rating × 4 XP
- Skills: New rating × 2 XP
- Specialties: 3 XP each
- Edges/Perks: Variable (manual tracking)

---

## `/help`

Get help with Herald commands.

**Usage:**
```
/help [topic:TOPIC]
```

**Topics:**
- `start` - Getting started guide
- `management` - Character management
- `rolling` - Dice rolling
- `progression` - Skills & XP
- `mechanics` - Hunter mechanics
- `commands` - All commands list

**Example:**
```
/help topic:start
/help topic:rolling
```

---

🔸 **Improve your Hunter. Spend your XP. Grow stronger.**
```

---

## FILE: docs/commands/utility.md

```markdown
# Utility Commands

Utility commands provide help, information, and support resources.

---

## `/help`

Get comprehensive help with Herald commands and systems.

**Usage:**
```
/help [topic:TOPIC]
```

**Available Topics:**

### `start` - Getting Started
Quick start guide for new users:
- Creating your first character
- Basic commands
- Rolling dice
- Next steps

### `management` - Character Management
Character creation and management:
- `/create` command
- Switching characters
- Viewing character sheets
- Deleting characters

### `rolling` - Dice Rolling
H5E dice mechanics:
- Basic rolling
- Difficulty levels
- Desperation dice
- Critical successes
- Failure handling

### `progression` - Skills & XP
Character development:
- Raising attributes
- Improving skills
- Adding specialties
- Managing XP

### `mechanics` - Hunter Mechanics
Hunter-specific systems:
- Desperation and Despair
- Edges and Perks
- Creeds and Drives
- Damage tracking

### `commands` - All Commands
Complete command list with syntax.

**Examples:**
```
/help
/help topic:start
/help topic:rolling
/help topic:mechanics
```

---

## `/about`

Display bot information.

**Shows:**
- Bot name and version
- Feature list
- GitHub repository link
- Documentation website
- Support Discord server
- Credits

**Usage:**
```
/about
```

---

## Additional Resources

### Documentation Website
Complete Herald documentation with:
- Full H5E mechanics guide
- Detailed command reference
- Character creation tutorials
- Advanced gameplay guides

### Support Discord
Get help from:
- Bot developers
- Experienced users
- Community Storytellers
- Fellow Hunters

### GitHub Repository
Access to:
- Source code
- Issue tracker
- Feature requests
- Contributing guidelines

---

🔸 **Get help. Find resources. Join the community.**
```

---

## Quick Implementation Instructions

1. Copy content for `hunter.md` to `/home/user/herald-docs/docs/commands/hunter.md`
2. Copy content for `development.md` to `/home/user/herald-docs/docs/commands/development.md`
3. Copy content for `utility.md` to `/home/user/herald-docs/docs/commands/utility.md`
4. Commit all changes
5. Push to remote

All content is complete and ready to use!
