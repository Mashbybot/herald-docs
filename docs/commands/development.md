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

## Quick Reference

### Development Commands
```
/attributes attribute:Dexterity dots:4   # Raise attribute
/skill_set skill:Firearms dots:3         # Raise skill
/specialty action:add skill:F specialty:P # Add specialty
/xp action:view                          # Check XP
```

### XP Costs
- **Attributes:** New rating × 4 XP (8/12/16/20 XP)
- **Skills:** New rating × 2 XP (2/4/6/8/10 XP)
- **Specialties:** 3 XP each

### Related Documentation

- **[Progression](../h5e/progression.md)** - Complete XP and advancement guide
- **[Attributes & Skills](../h5e/attributes-skills.md)** - Full attribute and skill details
- **[Command Reference Overview](index.md)** - All commands

---

🔸 **Improve your Hunter. Spend your XP. Grow stronger.**
