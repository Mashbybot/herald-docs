# Getting Started with Herald

Welcome to Herald, your complete Hunter: The Reckoning 5th Edition companion for Discord.

This guide walks you through your first character and your first game session. In 10 minutes, you'll be ready to Hunt.

---

## What is Herald?

Herald is a Discord bot that handles everything you need to play H5E:

### Character Management
- Create Hunters with full attributes, skills, and specialties
- Track Edges, Perks, and supernatural abilities
- Manage Desperation and Despair
- Switch between multiple characters

### Dice Rolling
- Complete H5E d10 pool mechanics
- Automatic success counting with critical pairs
- Desperation dice with Overreach consequences
- Danger tracking and difficulty management

### Progression
- Experience point tracking
- Attribute and skill advancement
- Specialty management
- Full transaction history

### Game Support
- Damage and healing tracking
- Creed and Drive management
- Redemption mechanics
- Character sheet display

---

## Quick Start: Your First 5 Minutes

Let's create a character and make your first roll.

### 1. Create Your Character

Open Discord and type:

```
/create name:Alex Hunter
```

Herald creates a basic character with:
- All attributes at 1 (minimum)
- No skills yet
- Default Health (4) and Willpower (2)
- Zero Desperation

**You see:**
```
✅ Character created: Alex Hunter
Use /sheet to view your character
Use /character to switch characters
```

### 2. View Your Character Sheet

```
/sheet
```

Herald displays your complete character sheet:
- Attributes (all 1s for now)
- Skills (none yet)
- Health (4) and Willpower (2)
- Desperation (0)
- No Edges or Perks yet

### 3. Make Your First Roll

Let's test your luck:

```
/roll pool:5 difficulty:2 comment:My first roll!
```

**What happens:**
- Herald rolls 5 ten-sided dice
- Counts successes (6+ on each die)
- Compares to difficulty (2 successes needed)
- Displays the result with visual dice

**You might see:**
```
🎲 Alex Hunter - My first roll!
Pool: 5 | Difficulty: 2

Dice: [7] [3] [9] [2] [6]
Successes: 3 (7, 9, 6)

✅ SUCCESS (3 successes, needed 2)
Margin: 1
```

**Congratulations!** You just made your first H5E roll.

---

## Your First Real Character

Now let's build a proper Hunter.

### Step 1: Plan Your Character

Before touching Herald, answer these questions:

**Who are you?**
- Name and background
- Why do you Hunt?
- What's your specialty?

**What's your Creed?**
- **Defender** - Protect the innocent
- **Innocent** - Stumbled into the truth
- **Redeemer** - Save the monsters
- **Avenger** - Punish the guilty
- **Zealot** - Destroy all darkness

**What's your Drive?**
- Ambition, Competition, Curiosity, Rebellion, Vengeance, Vice, Virtue

**Example Concept:**
*"Detective Maria Santos, Defender, Drive: Justice (Virtue). She protects her neighborhood from supernatural threats."*

### Step 2: Set Your Attributes

You have **9 dots** to distribute across **9 attributes** (minimum 1 each):

**Prioritize one category:**
- Physical (Strength, Dexterity, Stamina): 4 dots
- Social (Charisma, Manipulation, Composure): 3 dots
- Mental (Intelligence, Wits, Resolve): 2 dots

**Detective Maria Santos example:**
```
/attributes attribute:Strength dots:2
/attributes attribute:Dexterity dots:3
/attributes attribute:Stamina dots:2

/attributes attribute:Charisma dots:2
/attributes attribute:Manipulation dots:2
/attributes attribute:Composure dots:3

/attributes attribute:Intelligence dots:3
/attributes attribute:Wits dots:3
/attributes attribute:Resolve dots:2
```

**Auto-calculations:**
- **Health** = Stamina + 3 = 5
- **Willpower** = Resolve + Composure = 5

### Step 3: Set Your Skills

You have **11 dots** to distribute across **27 skills**:

**Prioritize one category:**
- Physical skills: 7 dots
- Social skills: 4 dots
- Mental skills: 0 dots

**Or:**
- Physical: 4 dots
- Social: 7 dots
- Mental: 0 dots

**Or:**
- Any other combination totaling 11 dots

**Detective Maria example (Social/Mental focus):**
```
/skill_set skill:Firearms dots:3
/skill_set skill:Athletics dots:2
/skill_set skill:Brawl dots:1

/skill_set skill:Insight dots:3
/skill_set skill:Intimidation dots:2
/skill_set skill:Persuasion dots:2

/skill_set skill:Investigation dots:4
/skill_set skill:Awareness dots:3
/skill_set skill:Medicine dots:2
```

### Step 4: Add Specialties

Pick **3 specialties** for skills you have dots in:

```
/specialty action:add skill:Investigation specialty:Crime Scenes
/specialty action:add skill:Firearms specialty:Pistols
/specialty action:add skill:Insight specialty:Reading Lies
```

**When you use these:**
- Roll with the skill as normal
- On success, reroll any 1s (once)
- Potentially turn failures into successes

### Step 5: Set Your Identity

```
/creed creed:Defender
/drive drive:Virtue
/ambition ambition:Protect the neighborhood from all threats
/desire desire:Find and stop the vampire killing locals
```

**These define:**
- Your philosophical approach (Creed)
- What motivates you (Drive)
- Your long-term goal (Ambition)
- Your immediate focus (Desire)

### Step 6: Choose Your Starting Edge

Every Hunter gets **one Edge** to start:

```
/edge edge:Senses
```

**Senses** is great for investigators - it enhances perception and awareness.

**Other good starter Edges:**
- **Arsenal** - For combat-focused Hunters
- **Contacts** - For social/investigative Hunters
- **Library** - For research-focused Hunters
- **Fleet** - For fast/athletic Hunters

### Step 7: View Your Complete Sheet

```
/sheet
```

You now see a complete Hunter ready for the first session!

---

## Understanding the Basics

### Rolling Dice

**The Formula:**
```
Attribute + Skill + Modifiers = Dice Pool
```

**Example: Shooting a Vampire**
```
Dexterity (3) + Firearms (3) = 6 dice
/roll pool:6 difficulty:2 comment:Shooting the vampire
```

**Success Counting:**
- 1-5 = Failure
- 6-9 = One success each
- 10 = One success (can form critical pairs)
- **Pair of 10s** = Critical (+2 additional successes)

### When to Roll

**Combat Actions:**
- Attack: Dexterity + Firearms (shooting) or Strength/Dexterity + Brawl/Melee (close combat)
- Defend: Dexterity + Athletics (dodge)
- Soak damage: Stamina + Resolve

**Social Actions:**
- Persuade: Manipulation + Persuasion
- Intimidate: Strength or Manipulation + Intimidation
- Lie: Manipulation + Subterfuge
- Detect lies: Wits + Insight

**Mental Actions:**
- Investigate: Intelligence + Investigation
- Research: Intelligence + Academics or Occult
- Notice: Wits + Awareness
- Remember: Intelligence + relevant skill

### Using Desperation

**What is Desperation?**
- Your connection to supernatural power (0-10 rating)
- Adds extra dice when you need them
- Risks Overreach and Despair

**How to use it:**
```
/roll pool:5 difficulty:3 desperate:true comment:Must succeed!
```

If Desperation = 3, you roll **8 dice total** (5 + 3 orange Desperation dice).

**The Risk:**
- Roll 1s on Desperation dice? Enter Overreach or Despair
- Success + Desperation 1s = Choose to keep success and gain Danger, or enter Despair
- Failure + Desperation 1s = Automatic Despair

**When to use Desperation:**
- Life-or-death situations
- Critical story moments
- When failure is unacceptable

**When NOT to use Desperation:**
- Routine tasks
- Low-stakes situations
- When already at high Danger

### Taking Damage

**When you get hurt:**
```
/damage amount:3 type:lethal
```

**Damage types:**
- **Superficial** - Bruises, minor cuts (heals quickly)
- **Lethal** - Serious wounds (heals slowly)

**Tracking:**
- Superficial fills from left
- Lethal fills from right
- When they meet in the middle, you're incapacitated

**Healing:**
```
/heal amount:2 type:superficial
```

### Managing Your Character

**Switch characters:**
```
/character name:Different Character
```

**View any character:**
```
/sheet character:Maria Santos
```

**Delete a character:**
```
/delete character:Old Character
```

**Get help:**
```
/help topic:start
```

---

## Your First Session

### Before the Session

1. **Coordinate with your Storyteller:**
   - Confirm character concept fits the chronicle
   - Understand the setting and tone
   - Learn about other Hunters in the cell

2. **Review your character:**
   ```
   /sheet
   ```
   - Know your dice pools
   - Understand your Edge and Perks
   - Remember your Creed and Drive

3. **Prepare common rolls:**
   - Your best combat pool
   - Your best social pool
   - Your best investigation pool

### During the Session

**Investigation Scene:**
```
/roll pool:7 difficulty:2 comment:Investigating the crime scene
```
(Intelligence 3 + Investigation 4)

**Social Scene:**
```
/roll pool:5 difficulty:2 comment:Persuading the witness to talk
```
(Manipulation 2 + Persuasion 3)

**Combat Scene:**
```
/roll pool:6 difficulty:2 comment:Shooting the ghoul
```
(Dexterity 3 + Firearms 3)

**Desperate Moment:**
```
/roll pool:6 difficulty:4 desperate:true comment:Must hit the vampire leader!
```
(Uses your Desperation rating as extra dice)

### After the Session

**Receive XP:**
```
/xp action:view
```

Your Storyteller awards XP with:
```
/xp action:add amount:3 reason:Session XP
```

**Spend XP:**
```
/skill_set skill:Firearms dots:4
```
(Costs 8 XP: new rating 4 × 2)

**Plan progression:**
- Save for attributes (expensive: new rating × 4 XP)
- Raise key skills (cheaper: new rating × 2 XP)
- Add specialties (cheap: 3 XP each)
- Buy new Edges or Perks (varies, ask Storyteller)

---

## Common Questions

### "What attributes should I prioritize?"

**Combat-focused:** Dexterity (attack) and Stamina (survive)
**Social-focused:** Charisma/Manipulation (influence) and Composure (resist)
**Investigation-focused:** Intelligence (analyze) and Wits (notice)

**Everyone needs:** At least 2 in their primary attributes.

### "What skills are most important?"

**Universal:**
- Athletics (dodge, chase, climb)
- Awareness (notice threats)
- Insight (read people)

**Combat:**
- Firearms (ranged)
- Brawl or Melee (close combat)

**Investigation:**
- Investigation (find clues)
- Occult (understand monsters)

**Social:**
- Persuasion (convince)
- Intimidation (threaten)
- Subterfuge (deceive)

### "How does Desperation work again?"

1. You have a Desperation rating (0-10)
2. When rolling with `desperate:true`, add that many extra dice
3. If those extra dice show 1s, you risk Overreach or Despair
4. Desperation increases when you use Edges or face darkness
5. It's power with a price

### "What's the difference between Creed and Drive?"

- **Creed** = Your philosophy (how you Hunt)
- **Drive** = Your motivation (why you Hunt)
- Both can be lost if you enter Despair
- Both can be regained through Redemption

### "How do I know what to roll?"

Ask your Storyteller: "What do I roll for this?"

**Common formula:**
- Physical task: Physical attribute + Physical skill
- Social task: Social attribute + Social skill
- Mental task: Mental attribute + Mental skill

---

## Next Steps

### Learn More About:

**Character Creation:**
- **[Character Creation Guide](character-creation.md)** - Deep dive into building optimized Hunters
- **[Attributes & Skills](../h5e/attributes-skills.md)** - Complete attribute and skill reference

**Game Mechanics:**
- **[Dice Mechanics](../h5e/dice-mechanics.md)** - Full dice rolling rules
- **[Desperation](../h5e/desperation.md)** - Master the risk/reward system
- **[Edges](../h5e/edge.md)** - All 17 Edges and their Perks

**Playing the Game:**
- **[Playing Guide](playing.md)** - Session-by-session gameplay
- **[Command Reference](../commands/index.md)** - All Herald commands

**For Storytellers:**
- **[Storyteller Guide](storyteller.md)** - Running games with Herald

**Advanced Topics:**
- **[Advanced Guide](advanced.md)** - Optimization and tactics
- **[Progression](../h5e/progression.md)** - XP and character advancement

---

## Practice Exercise

**Try creating this character:**

**Name:** Jack Morrison
**Creed:** Avenger
**Drive:** Vengeance
**Concept:** Ex-soldier hunting the creatures that killed his squad

**Attributes (9 dots):**
- Physical: Str 3, Dex 3, Sta 3 (9 total, distributed from base 1s)
- Social: Cha 1, Man 2, Com 2
- Mental: Int 2, Wit 3, Res 2

**Skills (11 dots):**
- Firearms 4, Athletics 3, Brawl 2, Intimidation 2

**Specialties (3):**
- Firearms (Rifles)
- Athletics (Running)
- Intimidation (Threats)

**Edge:** Arsenal

**Commands to create Jack:**
```
/create name:Jack Morrison
/attributes attribute:Strength dots:3
/attributes attribute:Dexterity dots:3
/attributes attribute:Stamina dots:3
/attributes attribute:Manipulation dots:2
/attributes attribute:Composure dots:2
/attributes attribute:Intelligence dots:2
/attributes attribute:Wits dots:3
/attributes attribute:Resolve dots:2
/skill_set skill:Firearms dots:4
/skill_set skill:Athletics dots:3
/skill_set skill:Brawl dots:2
/skill_set skill:Intimidation dots:2
/specialty action:add skill:Firearms specialty:Rifles
/specialty action:add skill:Athletics specialty:Running
/specialty action:add skill:Intimidation specialty:Threats
/creed creed:Avenger
/drive drive:Vengeance
/edge edge:Arsenal
/sheet
```

---

🔸 **Join the Hunt. Your story begins now.**
