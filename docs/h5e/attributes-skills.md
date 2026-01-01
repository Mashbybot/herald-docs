# Attributes & Skills

Attributes and Skills form the foundation of your Hunter character. Together, they determine your dice pools for all actions in Hunter: The Reckoning 5E.

---

## Understanding Attributes & Skills

### The Basic Formula

```
Attribute + Skill + Modifiers = Dice Pool
```

**Example:** To investigate a crime scene:
```
Intelligence (3) + Investigation (2) = 5 dice
/roll pool:5 difficulty:2 comment:Examining the crime scene
```

### Attributes vs. Skills

- **Attributes** - Your raw, innate capabilities (1-5 dots)
- **Skills** - Your trained expertise and knowledge (0-5 dots)
- **Specialties** - Focused areas of exceptional skill (see [Progression](progression.md))

---

## The 9 Attributes

Attributes represent your character's fundamental capabilities. Every character has **9 attributes** across three categories, each rated from **1 to 5 dots**.

!!! herald "Attribute Rating Scale"
    - **1 dot** - Poor (below average)
    - **2 dots** - Average (typical human)
    - **3 dots** - Good (trained professional)
    - **4 dots** - Exceptional (among the best)
    - **5 dots** - Outstanding (peak human performance)

### Physical Attributes

Physical attributes govern your body's capabilities.

#### Strength 💪
**Raw physical power and muscle**

- Lifting heavy objects
- Breaking down doors
- Hand-to-hand combat damage
- Carrying capacity

**Herald Command:**
```
/attributes attribute:Strength dots:3
```

---

#### Dexterity 🤸
**Agility, reflexes, and fine motor control**

- Dodging attacks
- Sleight of hand
- Aiming firearms
- Acrobatics and parkour

**Herald Command:**
```
/attributes attribute:Dexterity dots:3
```

---

#### Stamina 🛡️
**Endurance, resilience, and toughness**

- Resisting disease and poison
- Long-distance running
- Withstanding damage
- Staying conscious when wounded

**Special:** Stamina determines your **Health**
```
Health = Stamina + 3
```

When you increase Stamina, your Health automatically updates in Herald.

**Herald Command:**
```
/attributes attribute:Stamina dots:3
```

---

### Social Attributes

Social attributes govern your interactions with others.

#### Charisma ✨
**Personal magnetism and charm**

- Making good first impressions
- Inspiring others
- Public speaking
- Leading by example

**Herald Command:**
```
/attributes attribute:Charisma dots:3
```

---

#### Manipulation 🎭
**Influence through cunning and persuasion**

- Lying convincingly
- Negotiating deals
- Emotional manipulation
- Getting what you want subtly

**Herald Command:**
```
/attributes attribute:Manipulation dots:3
```

---

#### Composure 😌
**Emotional control and grace under pressure**

- Staying calm in combat
- Resisting intimidation
- Maintaining poker face
- Controlling emotional outbursts

**Special:** Composure contributes to your **Willpower**
```
Willpower = Resolve + Composure
```

When you increase Composure, your Willpower automatically updates in Herald.

**Herald Command:**
```
/attributes attribute:Composure dots:3
```

---

### Mental Attributes

Mental attributes govern your intellectual capabilities.

#### Intelligence 🧠
**Reasoning, memory, and analytical ability**

- Solving puzzles
- Remembering facts
- Analyzing clues
- Academic knowledge

**Herald Command:**
```
/attributes attribute:Intelligence dots:3
```

---

#### Wits 👁️
**Alertness, quick thinking, and instinct**

- Noticing ambushes
- Thinking on your feet
- Initiative in combat
- Spotting lies

**Herald Command:**
```
/attributes attribute:Wits dots:3
```

---

#### Resolve 💎
**Determination, focus, and mental fortitude**

- Resisting mental influence
- Maintaining concentration
- Pushing through pain
- Staying on task

**Special:** Resolve contributes to your **Willpower**
```
Willpower = Resolve + Composure
```

When you increase Resolve, your Willpower automatically updates in Herald.

**Herald Command:**
```
/attributes attribute:Resolve dots:3
```

---

## The 27 Skills

Skills represent trained abilities and learned knowledge. Skills range from **0 to 5 dots**, where 0 means untrained.

!!! herald "Skill Rating Scale"
    - **0 dots** - Untrained (use attribute alone)
    - **1 dot** - Novice (basic understanding)
    - **2 dots** - Practiced (competent professional)
    - **3 dots** - Expert (highly skilled)
    - **4 dots** - Master (among the best in your field)
    - **5 dots** - Legendary (world-class expertise)

### Physical Skills

Physical skills cover athletic and manual capabilities.

#### Athletics 🏃
**Running, jumping, climbing, and general fitness**

**Common Uses:**
- Chasing or fleeing from threats
- Climbing walls or buildings
- Swimming long distances
- Parkour and free running

**Example Roll:**
```
Dexterity + Athletics (to climb a fence)
Stamina + Athletics (to run a marathon)
```

**Herald Command:**
```
/skill_set skill:Athletics dots:3
```

---

#### Brawl 👊
**Unarmed combat and hand-to-hand fighting**

**Common Uses:**
- Punching, kicking, grappling
- Bar fights and street brawls
- Wrestling and submissions
- Disarming opponents

**Example Roll:**
```
Strength + Brawl (to punch)
Dexterity + Brawl (to dodge and counter)
```

**Herald Command:**
```
/skill_set skill:Brawl dots:2
```

---

#### Craft 🔨
**Creating, repairing, and building physical objects**

**Common Uses:**
- Fixing vehicles or equipment
- Building traps or barriers
- Creating improvised weapons
- Repairing damaged items

**Example Roll:**
```
Dexterity + Craft (to repair a car)
Intelligence + Craft (to design a trap)
```

**Herald Command:**
```
/skill_set skill:Craft dots:2
```

---

#### Driving 🚗
**Operating land vehicles**

**Common Uses:**
- High-speed chases
- Evasive maneuvers
- Ramming tactics
- Off-road navigation

**Example Roll:**
```
Dexterity + Driving (to perform a J-turn)
Wits + Driving (to react to obstacles)
```

**Herald Command:**
```
/skill_set skill:Driving dots:2
```

---

#### Firearms 🔫
**Using guns and ranged weapons**

**Common Uses:**
- Shooting pistols, rifles, shotguns
- Sniping from distance
- Maintaining firearms
- Quick-draw techniques

**Example Roll:**
```
Dexterity + Firearms (to shoot accurately)
Wits + Firearms (to quick-draw)
```

**Herald Command:**
```
/skill_set skill:Firearms dots:3
```

---

#### Larceny 🔓
**Criminal skills: lockpicking, pickpocketing, security**

**Common Uses:**
- Picking locks
- Bypassing alarms
- Hotwiring vehicles
- Pickpocketing

**Example Roll:**
```
Dexterity + Larceny (to pick a lock)
Intelligence + Larceny (to plan a heist)
```

**Herald Command:**
```
/skill_set skill:Larceny dots:2
```

---

#### Melee ⚔️
**Armed close combat with weapons**

**Common Uses:**
- Fighting with knives, clubs, swords
- Wielding improvised weapons
- Parrying attacks
- Weapon maintenance

**Example Roll:**
```
Strength + Melee (to strike with a baseball bat)
Dexterity + Melee (to parry with a knife)
```

**Herald Command:**
```
/skill_set skill:Melee dots:3
```

---

#### Stealth 🥷
**Moving unseen and unheard**

**Common Uses:**
- Sneaking past guards
- Hiding from enemies
- Tailing suspects
- Ambush preparation

**Example Roll:**
```
Dexterity + Stealth (to sneak quietly)
Wits + Stealth (to find a hiding spot quickly)
```

**Herald Command:**
```
/skill_set skill:Stealth dots:3
```

---

#### Survival 🏕️
**Wilderness skills and tracking**

**Common Uses:**
- Tracking prey
- Foraging for food
- Building shelter
- Navigation without tools
- Predicting weather

**Example Roll:**
```
Wits + Survival (to track footprints)
Stamina + Survival (to endure harsh conditions)
```

**Herald Command:**
```
/skill_set skill:Survival dots:2
```

---

### Social Skills

Social skills govern interactions with other people.

#### Animal Ken 🐕
**Understanding and influencing animals**

**Common Uses:**
- Calming aggressive animals
- Training pets
- Reading animal behavior
- Commanding attack dogs

**Example Roll:**
```
Charisma + Animal Ken (to calm a guard dog)
Manipulation + Animal Ken (to train an animal)
```

**Herald Command:**
```
/skill_set skill:"Animal Ken" dots:2
```

---

#### Etiquette 🎩
**Social graces and cultural knowledge**

**Common Uses:**
- Navigating high society
- Diplomatic negotiations
- Proper formal behavior
- Avoiding social faux pas

**Example Roll:**
```
Charisma + Etiquette (to impress at a gala)
Intelligence + Etiquette (to know the proper protocol)
```

**Herald Command:**
```
/skill_set skill:Etiquette dots:2
```

---

#### Insight 👁️‍🗨️
**Reading people and detecting lies**

**Common Uses:**
- Spotting lies
- Reading body language
- Understanding motivations
- Sensing hidden emotions

**Example Roll:**
```
Wits + Insight (to detect a lie)
Intelligence + Insight (to understand someone's plan)
```

**Herald Command:**
```
/skill_set skill:Insight dots:3
```

---

#### Intimidation 😠
**Threats, fear, and coercion**

**Common Uses:**
- Threatening suspects
- Extracting information
- Establishing dominance
- Causing fear

**Example Roll:**
```
Strength + Intimidation (to physically threaten)
Manipulation + Intimidation (to subtly unnerve)
```

**Herald Command:**
```
/skill_set skill:Intimidation dots:2
```

---

#### Leadership 📣
**Inspiring and commanding others**

**Common Uses:**
- Leading teams
- Rallying allies in combat
- Organizing group efforts
- Maintaining morale

**Example Roll:**
```
Charisma + Leadership (to inspire courage)
Presence + Leadership (to command respect)
```

**Herald Command:**
```
/skill_set skill:Leadership dots:2
```

---

#### Performance 🎭
**Acting, music, and entertaining**

**Common Uses:**
- Going undercover
- Disguises and impersonation
- Public speaking
- Artistic performance

**Example Roll:**
```
Charisma + Performance (to give a speech)
Manipulation + Performance (to impersonate someone)
```

**Herald Command:**
```
/skill_set skill:Performance dots:2
```

---

#### Persuasion 🗣️
**Honest convincing and negotiation**

**Common Uses:**
- Convincing people
- Negotiating deals
- Making arguments
- Bargaining

**Example Roll:**
```
Charisma + Persuasion (to convince someone)
Manipulation + Persuasion (to negotiate a deal)
```

**Herald Command:**
```
/skill_set skill:Persuasion dots:3
```

---

#### Streetwise 🏙️
**Urban survival and criminal contacts**

**Common Uses:**
- Finding black market goods
- Navigating gang territory
- Gathering street rumors
- Understanding criminal culture

**Example Roll:**
```
Charisma + Streetwise (to get information from contacts)
Wits + Streetwise (to sense danger in bad neighborhoods)
```

**Herald Command:**
```
/skill_set skill:Streetwise dots:2
```

---

#### Subterfuge 🎭
**Deception, lies, and misdirection**

**Common Uses:**
- Lying convincingly
- Creating alibis
- Misdirection and distraction
- Covering tracks

**Example Roll:**
```
Manipulation + Subterfuge (to lie)
Wits + Subterfuge (to improvise a quick lie)
```

**Herald Command:**
```
/skill_set skill:Subterfuge dots:2
```

---

### Mental Skills

Mental skills represent knowledge and intellectual pursuits.

#### Academics 📚
**Scholarly knowledge and research**

**Common Uses:**
- Historical knowledge
- Research and library use
- Understanding ancient texts
- Academic credentials

**Example Roll:**
```
Intelligence + Academics (to research a topic)
Resolve + Academics (to focus on tedious research)
```

**Herald Command:**
```
/skill_set skill:Academics dots:2
```

---

#### Awareness 👀
**Noticing details and staying alert**

**Common Uses:**
- Spotting ambushes
- Noticing clues
- Detecting surveillance
- Staying vigilant

**Example Roll:**
```
Wits + Awareness (to spot danger)
Intelligence + Awareness (to analyze a scene)
```

**Herald Command:**
```
/skill_set skill:Awareness dots:3
```

---

#### Finance 💰
**Money, business, and economics**

**Common Uses:**
- Managing money
- Understanding financial crimes
- Investing wisely
- Tracing money trails

**Example Roll:**
```
Intelligence + Finance (to analyze accounts)
Manipulation + Finance (to negotiate a loan)
```

**Herald Command:**
```
/skill_set skill:Finance dots:2
```

---

#### Investigation 🔍
**Gathering clues and solving mysteries**

**Common Uses:**
- Examining crime scenes
- Following leads
- Connecting evidence
- Forensic analysis

**Example Roll:**
```
Intelligence + Investigation (to analyze evidence)
Wits + Investigation (to spot a vital clue)
```

**Herald Command:**
```
/skill_set skill:Investigation dots:3
```

---

#### Medicine 🏥
**Healthcare and anatomy**

**Common Uses:**
- Treating injuries
- Diagnosing illness
- Performing surgery
- Forensic pathology

**Example Roll:**
```
Intelligence + Medicine (to diagnose)
Dexterity + Medicine (to perform surgery)
```

**Herald Command:**
```
/skill_set skill:Medicine dots:2
```

---

#### Occult 🔮
**Supernatural knowledge and lore**

**Common Uses:**
- Identifying supernatural creatures
- Understanding rituals
- Knowing monster weaknesses
- Occult research

**Example Roll:**
```
Intelligence + Occult (to identify a vampire)
Wits + Occult (to recall a monster's weakness)
```

**Herald Command:**
```
/skill_set skill:Occult dots:3
```

---

#### Politics 🏛️
**Government, law, and bureaucracy**

**Common Uses:**
- Understanding laws
- Navigating bureaucracy
- Political maneuvering
- Knowing officials

**Example Roll:**
```
Intelligence + Politics (to understand regulations)
Manipulation + Politics (to influence an official)
```

**Herald Command:**
```
/skill_set skill:Politics dots:2
```

---

#### Science 🔬
**Natural sciences and research methods**

**Common Uses:**
- Chemistry and biology
- Analyzing substances
- Using lab equipment
- Scientific methodology

**Example Roll:**
```
Intelligence + Science (to analyze a chemical)
Dexterity + Science (to conduct an experiment)
```

**Herald Command:**
```
/skill_set skill:Science dots:2
```

---

#### Technology 💻
**Computers, electronics, and modern tech**

**Common Uses:**
- Hacking computers
- Using surveillance equipment
- Repairing electronics
- Digital forensics

**Example Roll:**
```
Intelligence + Technology (to hack a system)
Wits + Technology (to quickly bypass security)
```

**Herald Command:**
```
/skill_set skill:Technology dots:3
```

---

## Using Attributes & Skills Together

### Common Dice Pools

Here are typical attribute + skill combinations:

| Action | Dice Pool | Example |
|--------|-----------|---------|
| **Climb a wall** | Dexterity + Athletics | 3 + 2 = 5 dice |
| **Punch someone** | Strength + Brawl | 3 + 2 = 5 dice |
| **Shoot a gun** | Dexterity + Firearms | 3 + 3 = 6 dice |
| **Pick a lock** | Dexterity + Larceny | 4 + 2 = 6 dice |
| **Sneak past guards** | Dexterity + Stealth | 3 + 3 = 6 dice |
| **Spot an ambush** | Wits + Awareness | 3 + 3 = 6 dice |
| **Convince someone** | Charisma + Persuasion | 3 + 2 = 5 dice |
| **Lie convincingly** | Manipulation + Subterfuge | 3 + 2 = 5 dice |
| **Research a topic** | Intelligence + Academics | 3 + 2 = 5 dice |
| **Examine evidence** | Intelligence + Investigation | 3 + 3 = 6 dice |

### Attribute-Only Rolls

Sometimes you roll using only an attribute (when no skill applies):

```
/roll pool:3 comment:Raw strength check (Strength only)
```

Examples:
- **Stamina** - Resisting poison
- **Composure** - Staying calm under fire
- **Resolve** - Resisting mental influence

---

## Character Creation Tips

### Balanced Characters

A well-rounded Hunter typically has:
- **One primary attribute** at 3-4 in each category
- **2-3 favored skills** at 3+ dots
- **Several supporting skills** at 1-2 dots
- **Specialties** in your core competencies

**Example Balanced Build:**
```
Physical: Strength 2, Dexterity 3, Stamina 3
Social: Charisma 3, Manipulation 2, Composure 2
Mental: Intelligence 2, Wits 3, Resolve 2

Key Skills: Firearms 3, Awareness 3, Investigation 3
Supporting: Athletics 2, Stealth 2, Occult 2
```

### Specialized Characters

Focus on excelling in one area:

**Combat Specialist:**
```
Physical: Strength 3, Dexterity 4, Stamina 3
Skills: Firearms 4, Athletics 3, Brawl 3, Melee 3
```

**Investigator:**
```
Mental: Intelligence 4, Wits 3, Resolve 2
Skills: Investigation 4, Awareness 3, Occult 3, Academics 2
```

**Social Manipulator:**
```
Social: Charisma 3, Manipulation 4, Composure 3
Skills: Persuasion 3, Subterfuge 3, Insight 3, Streetwise 2
```

---

## Improving Attributes & Skills

You can improve attributes and skills by spending Experience Points (XP):

### Costs

- **Attributes:** New rating × 4 XP
  - 1→2 = 8 XP
  - 2→3 = 12 XP
  - 3→4 = 16 XP
  - 4→5 = 20 XP

- **Skills:** New rating × 2 XP
  - 0→1 = 2 XP
  - 1→2 = 4 XP
  - 2→3 = 6 XP
  - 3→4 = 8 XP
  - 4→5 = 10 XP

- **Specialties:** 3 XP each

See [Progression](progression.md) for complete XP rules.

### Improving in Herald

```
# Check your XP
/xp action:view

# Improve an attribute (costs XP automatically)
/attributes attribute:Dexterity dots:4

# Improve a skill
/skill_set skill:Firearms dots:4

# Add a specialty
/specialty action:add skill:Firearms specialty:Pistols
```

---

## Specialties

Specialties represent focused expertise within a skill. When a specialty applies, you gain bonus dice.

### How Specialties Work

1. You can have **multiple specialties per skill**
2. Maximum specialties per skill = skill dots (minimum 1)
3. Specialties provide mechanical bonuses when applicable
4. Cost: 3 XP each

### Examples

```
Investigation 3 with specialty "Crime Scenes"
When investigating crime scenes, add bonus dice

Firearms 4 with specialties "Pistols" and "Rifles"
When using pistols or rifles specifically, add bonus dice

Occult 3 with specialty "Vampire Lore"
When dealing with vampire-related occult knowledge, add bonus dice
```

### Managing Specialties in Herald

```
# View all specialties
/specialty action:view

# Add a specialty (requires skill to have at least 1 dot)
/specialty action:add skill:Firearms specialty:Shotguns

# Remove a specialty
/specialty action:remove skill:Firearms specialty:Shotguns
```

---

## Quick Reference

### All 9 Attributes

**Physical:** Strength, Dexterity, Stamina
**Social:** Charisma, Manipulation, Composure
**Mental:** Intelligence, Wits, Resolve

**Derived Stats:**
- Health = Stamina + 3
- Willpower = Resolve + Composure

### All 27 Skills

**Physical (9):**
Athletics, Brawl, Craft, Driving, Firearms, Larceny, Melee, Stealth, Survival

**Social (9):**
Animal Ken, Etiquette, Insight, Intimidation, Leadership, Performance, Persuasion, Streetwise, Subterfuge

**Mental (9):**
Academics, Awareness, Finance, Investigation, Medicine, Occult, Politics, Science, Technology

---

## Next Steps

- **[Dice Mechanics](dice-mechanics.md)** - Learn how to roll your dice pools
- **[Progression](progression.md)** - Advance your character with XP
- **[Creeds](creeds.md)** - Choose your hunting philosophy
- **[Edge](edge.md)** - Unlock supernatural advantages

Or return to the [H5E Overview](overview.md) for the big picture!

---

🔸 **Build your Hunter. Define your capabilities.**
