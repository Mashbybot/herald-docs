# Creating Your First Character

Let's create your first Hunter character step-by-step!

---

## The Quick Way

Want to jump right in? Use this single command:

```
/create name:Raven
```

Done! Herald creates a basic character with:
- All attributes set to 1
- All skills set to 0
- Default Health (3) and Willpower (3)
- No Edge or Desperation

You can customize everything later!

---

## The Detailed Way

Want more control from the start? Include attributes in your creation:

```
/create name:Raven strength:2 dexterity:4 stamina:3 charisma:3 manipulation:2 composure:3 intelligence:3 wits:3 resolve:2
```

!!! tip "Attribute Distribution"
    In H5E, new Hunters typically have:
    
    - **Total of 12 dots** across all 9 attributes
    - No attribute higher than 5
    - Minimum of 1 in each attribute (Herald's default)

---

## Step-by-Step Character Creation

### 1. Choose a Name

Pick a name for your Hunter. This is what you'll use to reference them in commands:

```
/create name:Raven
```

!!! info "Character Names"
    - Use quotes for multi-word names: `name:"Sarah Connor"`
    - Names are case-insensitive for commands
    - Each character name must be unique to you

### 2. Set Attributes

Herald uses the 9 core H5E attributes:

#### Physical
- **Strength** - Raw physical power
- **Dexterity** - Agility and coordination
- **Stamina** - Endurance and toughness

#### Social
- **Charisma** - Charm and force of personality
- **Manipulation** - Subtlety and persuasion
- **Composure** - Self-control and poise

#### Mental
- **Intelligence** - Reasoning and memory
- **Wits** - Quick thinking and awareness
- **Resolve** - Determination and focus

**Example:**
```
/create name:Raven strength:2 dexterity:4 stamina:3 charisma:3 manipulation:2 composure:3 intelligence:3 wits:3 resolve:2
```

### 3. View Your Character

Check out your new character:

```
/sheet character:Raven
```

Herald displays your complete character sheet with:
- All attributes
- Derived stats (Health, Willpower)
- Empty skills (ready to fill in)
- Hunter traits (Creed, Edge, etc.)

---

## Setting Up Skills

Now let's add skills to your character!

### Option 1: Skill Template (Fastest)

Apply a pre-built skill distribution:

```
/skill_template character:Raven template:Balanced
```

**Available Templates:**

- **Balanced** (7/5/3/1) - Well-rounded Hunter
  - 1 skill at 4 dots
  - 3 skills at 3 dots
  - 4 skills at 2 dots
  - 4 skills at 1 dot
  
- **Specialist** (9/5/1/0) - Focused expert
  - 1 skill at 5 dots
  - 2 skills at 4 dots
  - 3 skills at 3 dots
  - 3 skills at 2 dots
  
- **Jack-of-all-trades** (5/5/5/0) - Broad competence
  - 8 skills at 2 dots
  - 4 skills at 1 dot

!!! tip "Skill Points"
    H5E characters typically start with 11 skill dots in their primary category, 7 in secondary, and 4 in tertiary.

### Option 2: Individual Skills

Set skills one at a time for complete control:

```
/skill_set character:Raven skill:Firearms dots:3
/skill_set character:Raven skill:Stealth dots:4
/skill_set character:Raven skill:Investigation dots:2
```

### Option 3: Bulk Setting

Set multiple skills at once:

```
/skill_bulk character:Raven skill1:Firearms dots1:3 skill2:Stealth dots2:4 skill3:Investigation dots3:2
```

---

## Adding Specialties

Give your character specialties for bonus dice in specific situations:

```
/specialty character:Raven skill:Firearms specialty:Pistols
/specialty character:Raven skill:Stealth specialty:Urban
```

When you roll with a specialty, you get +1 die if the situation matches!

---

## Setting Hunter Traits

### Choose Your Creed

Every Hunter has a Creed that defines their philosophy:

```
/creed character:Raven creed:Avenger
```

**Available Creeds:**
- Avenger
- Defender
- Innocent
- Judge
- Martyr
- Redeemer
- Visionary

### Set Your Drives

Define what motivates your Hunter:

```
# Long-term goal
/ambition character:Raven ambition:"Rid the city of vampires"

# Short-term goal  
/desire character:Raven desire:"Find the creature that killed my sister"

# Hunting motivation
/drive character:Raven drive:"Protect the innocent from supernatural predators"
```

### Set Edge

Edge represents supernatural insight and power:

```
/edge character:Raven edge:2
```

!!! info "Edge Rating"
    Most starting Hunters have Edge 1-3. Edge adds dice to rolls and has special properties.

---

## Equipment & Notes

### Add Equipment

Track your Hunter's gear:

```
/equipment character:Raven equipment:"Glock 17, tactical vest, flashlight, silver knife, rosary"
```

### Add Notes

Keep notes about your character:

```
/notes character:Raven notes:"Former detective. Sister killed by vampire. Joined the hunt 6 months ago. Has a cat named Midnight."
```

---

## Your Character is Ready!

🎉 Congratulations! You now have a complete Hunter character.

### Quick Test Roll

Try rolling some dice with your new character:

```
/roll_char character:Raven attribute:Dexterity skill:Firearms difficulty:2
```

Herald will:
1. Look up Raven's Dexterity and Firearms ratings
2. Roll the combined pool
3. Check for successes against difficulty 2
4. Display clean, readable results

---

## Example Character: Raven

Here's a complete character creation sequence:

```
# Create with attributes
/create name:Raven strength:2 dexterity:4 stamina:3 charisma:3 manipulation:2 composure:3 intelligence:3 wits:3 resolve:2

# Apply skill template
/skill_template character:Raven template:Balanced

# Add key skills manually
/skill_set character:Raven skill:Firearms dots:4
/skill_set character:Raven skill:Stealth dots:3
/skill_set character:Raven skill:Investigation dots:3

# Add specialties
/specialty character:Raven skill:Firearms specialty:Pistols
/specialty character:Raven skill:Stealth specialty:Urban

# Set Creed and drives
/creed character:Raven creed:Avenger
/ambition character:Raven ambition:"Rid the city of vampires"
/desire character:Raven desire:"Find the creature that killed my sister"
/drive character:Raven drive:"Protect the innocent"

# Set Edge
/edge character:Raven edge:2

# Add equipment
/equipment character:Raven equipment:"Glock 17, tactical vest, flashlight, silver knife"

# Add notes
/notes character:Raven notes:"Former detective turned Hunter after her sister was killed by a vampire."

# View the completed sheet
/sheet character:Raven
```

---

## Next Steps

Now that you have a character:

- **[Learn to Roll Dice](basic-rolling.md)** - Master H5E mechanics
- **[Character Management](character-management.md)** - Organize multiple characters
- **[Hunter Mechanics](hunter-mechanics.md)** - Edge, Desperation, and more
- **[Experience System](experience.md)** - Improve your Hunter over time

---

!!! question "Need Help?"
    - Type `/help topic:Character Creation` in Discord
    - Check the [FAQ](../support/faq.md)
    - Join our [Support Server](https://discord.gg/9bEZk6ARG9)
