# Edge & Perks

Edges are the supernatural advantages that define Hunters. These abilities set you apart from ordinary humans and give you the tools to fight monsters. Each Edge can be enhanced with **Perks** that provide specialized benefits.

---

## What are Edges?

**Edges** are supernatural gifts granted by the Calling. They represent:

- **Resources** - Arsenal, Fleet, Ordnance (physical assets)
- **Skills** - Improvised Gear, Global Access, Drone Jockey (supernatural aptitudes)
- **Powers** - Sense the Unnatural, Repel the Unnatural, Artifact (paranormal abilities)

Every Edge provides a baseline benefit and can be customized with **Perks** that expand its capabilities.

---

## Edge Categories

Herald organizes the 17 Edges into three categories:

### Assets (5 Edges)
Material resources that appear when needed:
- **Arsenal** - Weapons and military equipment
- **Fleet** - Vehicles and transportation
- **Ordnance** - Explosives and munitions
- **Library** - Information and research materials
- **Experimental Medicine** - Medical experiments and enhancements

### Aptitudes (5 Edges)
Supernatural skills and talents:
- **Improvised Gear** - Create temporary tools
- **Global Access** - Digital larceny and hacking
- **Drone Jockey** - Control autonomous drones
- **Beast Whisperer** - Command loyal animals
- **Turncoat** - Double agent abilities

### Endowments (7 Edges)
Direct paranormal powers:
- **Sense the Unnatural** - Detect supernatural presence
- **Repel the Unnatural** - Drive away monsters
- **Thwart the Unnatural** - Resist supernatural powers
- **Artifact** - Wield a supernatural relic
- **Cleanse the Unnatural** - Remove supernatural influence
- **Great Destiny** - Protected by higher purpose
- **Unnatural Changes** - Use your body supernaturally

---

## Managing Edges in Herald

### Adding an Edge

```
/edge action:add
```

Herald displays an interactive menu with all 17 Edges organized by category. Click the button for the Edge you want.

### Viewing Your Edges

```
/edge action:view
```

Shows all Edges your character currently has.

### Removing an Edge

```
/edge action:remove
```

Select from your character's Edges to remove one.

---

## Edge Descriptions

### Assets

#### Arsenal 🔫
**Weapons and military equipment**

You have access to weapons and combat gear beyond what civilians can acquire. When you need a weapon, it appears through mysterious supply chains, old contacts, or inexplicable luck.

**Base Benefit:**
- Access to military-grade weapons
- Weapons appear when needed (margin-based quality)
- Can requisition during scenes

**Herald Commands:**
```
/edge action:add (select Arsenal)
/perks action:view edge_name:Arsenal
/perks action:add edge_name:Arsenal perk_name:Exotics
```

**Available Perks:**
- **Team Requisition** - Provide copies of weapon up to margin
- **Special Features** - Weapon has special features up to margin
- **Exotics** - Procure rare or one-of-a-kind weapons
- **Untraceable** - Weapons never lead back to you
- **Backup Piece** - Once per scene, produce a hidden weapon

---

#### Fleet 🚗
**Vehicles and transportation**

You always have access to appropriate vehicles when you need them. Cars, motorcycles, boats - they appear when the hunt demands.

**Base Benefit:**
- Access to vehicles appropriate to situation
- Vehicles appear when needed (margin-based quality)
- Can change vehicles between scenes

**Herald Commands:**
```
/edge action:add (select Fleet)
/perks action:add edge_name:Fleet perk_name:Performance
```

**Available Perks:**
- **Armor** - Vehicles armored against small firearms
- **Performance** - Superior handling, bonus to pursuit rolls
- **Surveillance** - Vehicle equipped with surveillance tools
- **Untraceable** - Vehicles never lead back to you
- **Hidden Cache** - Secret compartment for Arsenal/Ordnance
- **Wagon Train** - Get replacement vehicle if current is lost

---

#### Ordnance 💣
**Explosives and munitions**

You can acquire explosives, incendiaries, and specialized ammunition. From grenades to C4, you have access to destructive tools.

**Base Benefit:**
- Access to explosives and munitions
- Items appear when needed (margin-based quality/quantity)
- Includes specialized ammunition

**Herald Commands:**
```
/edge action:add (select Ordnance)
/perks action:add edge_name:Ordnance perk_name:Exotics
```

**Available Perks:**
- **Multiple Payloads** - Additional copies up to margin
- **Exotics** - Custom or rare explosive substances
- **Non-lethal Munitions** - Flash grenades, tear gas, rubber bullets
- **Disguised Delivery** - Explosives disguised as mundane objects

---

#### Library 📚
**Information and research materials**

You have access to vast stores of occult knowledge, research databases, and supernatural lore. When you need information, you can find it.

**Base Benefit:**
- Access to occult and supernatural information
- Research bonus based on margin
- Can answer questions about monsters

**Herald Commands:**
```
/edge action:add (select Library)
/perks action:add edge_name:Library perk_name:"Where They Hide"
```

**Available Perks:**
- **Where They Hide** - Bonus to locate monster lairs
- **Who They Are** - Bonus to identify supernatural creatures
- **How to Halt Them** - Bonus to create wards and protection
- **How to Harm Them** - Bonus to exploit weaknesses
- **Binge** - Research time cut in half
- **Friendly Librarian** - 1 automatic success if you wait 1-2 days
- **Group Study** - +1 die per cell member participating
- **Permanent Fixture** - Library usable as safe house
- **How to Silence Them** - Bonus to social combat damage against prey
- **Pattern Analysis** - Narrow down monster behavior patterns
- **Where They Go** - Identify prey's targets and hunting grounds

---

#### Experimental Medicine 💉
**Medical experiments and enhancements**

You have access to experimental medical procedures, performance-enhancing drugs, and cutting-edge treatments. Some are legal. Most aren't.

**Base Benefit:**
- Access to experimental medical treatments
- Temporary physical enhancements
- Accelerated healing (with side effects)

**Herald Commands:**
```
/edge action:add (select "Experimental Medicine")
/perks action:add edge_name:"Experimental Medicine" perk_name:"Phoenix Protocol"
```

**Available Perks:**
- **Improved Resilience** - Armor Value 1 until end of story
- **Phoenix Protocol** - Heal twice as fast, aggravated becomes superficial
- **Monstrous Enhancement** - +2 dots to attribute, gain a weakness
- **Unstable Steroids** - +1 dot to attribute until end of story

---

### Aptitudes

#### Improvised Gear 🔧
**Create temporary tools from available materials**

You can jury-rig equipment from whatever's at hand. Duct tape, paperclips, and determination create functional tools.

**Base Benefit:**
- Create temporary items from available materials
- Items grant 2-dice bonus to relevant skill
- Items last for current scene

**Herald Commands:**
```
/edge action:add (select "Improvised Gear")
/perks action:add edge_name:"Improvised Gear" perk_name:Frugal
```

**Available Perks:**
- **Frugal** - Apply Perk skill bonuses with improvised items
- **Specialization** - 3-dice bonus (instead of 2) for one chosen skill
- **Mass Production** - Create additional items equal to margin
- **Speed Crafting** - Craft in (3 - margin) turns, minimum 1 turn
- **Made to Last** - Items last additional scenes (up to 6 total)

---

#### Global Access 💻
**Digital larceny and hacking**

You can breach digital security, manipulate electronic systems, and access restricted networks. The digital world is your hunting ground.

**Base Benefit:**
- Hack computer systems
- Access restricted databases
- Manipulate digital records

**Herald Commands:**
```
/edge action:add (select "Global Access")
/perks action:add edge_name:"Global Access" perk_name:"Money Trap"
```

**Available Perks:**
- **Watching Big Brother** - Manipulate surveillance footage
- **Money Trap** - Manipulate financial data and transactions
- **All-Access Pass** - Bypass electronic locks and security
- **The Letter of the Law** - Manipulate criminal records
- **Digital Cannon Fodder** - Reduce digital surveillance success by 2
- **Intranet Insertion** - Access air-gapped systems remotely
- **Spoof** - Pin your intrusion on false or real person

---

#### Drone Jockey 🚁
**Control autonomous drones**

You can summon and control advanced drones. These autonomous devices scout, surveil, and support your hunts.

**Base Benefit:**
- Summon and control a drone
- Drone quality based on margin
- Can perform reconnaissance and surveillance

**Herald Commands:**
```
/edge action:add (select "Drone Jockey")
/perks action:add edge_name:"Drone Jockey" perk_name:Armaments
```

**Available Perks:**
- **Autonomous** - Drones run simple patterns independently
- **Variants** - Summon additional drone variant
- **Specialist Skill** - Drone equipped for specific skill use
- **Armaments** - Drone equipped with taser
- **Payload** - Drone can carry large cargo
- **Electronic Shield** - Protection against hacking attempts

---

#### Beast Whisperer 🐕
**Command loyal animal companions**

You have supernatural rapport with animals. They trust you, obey you, and fight alongside you.

**Base Benefit:**
- Command and communicate with animals
- Animals assist you in hunts
- Can summon appropriate animals when needed

**Herald Commands:**
```
/edge action:add (select "Beast Whisperer")
/perks action:add edge_name:"Beast Whisperer" perk_name:Menagerie
```

**Available Perks:**
- **Incorruptible** - Animal immune to supernatural control
- **Complex Commands** - Animal performs complex multi-step tasks
- **Menagerie** - Add another animal type to your pool
- **Incognito** - Animal blends into environments naturally
- **Supernatural Scent** - Trained to detect specific creature types

---

#### Turncoat 🎭
**Double agent abilities**

You can infiltrate supernatural societies, pose as one of them, and betray them from within. You're a master of deception and misdirection.

**Base Benefit:**
- Pose as supernatural creature or ally
- Infiltrate monster organizations
- Gain trust of prey

**Herald Commands:**
```
/edge action:add (select Turncoat)
/perks action:add edge_name:Turncoat perk_name:"Poker Face"
```

**Available Perks:**
- **Deathbed Confession** - Use Turncoat benefits during combat
- **Stick to the Plan** - Cell understands your intent without communication
- **Poker Face** - 2-dice bonus when questioned about loyalties
- **We Come as a Team** - Bring cellmate along (up to margin)

---

### Endowments

#### Sense the Unnatural 👁️
**Detect supernatural presence**

You can sense when something supernatural is near. Your skin crawls, your vision shifts, and you *know* something isn't right.

**Base Benefit:**
- Detect supernatural presence nearby
- Requires object of focus (ritual or item)
- Roll to sense creatures within range

**Herald Commands:**
```
/edge action:add (select "Sense the Unnatural")
/perks action:add edge_name:"Sense the Unnatural" perk_name:"Creature Specialization"
```

**Available Perks:**
- **Creature Specialization** - 2-dice bonus vs specific creature type
- **Precision** - Determine *which* creature in room is supernatural
- **Range** - Extended to city block size area
- **Handfree** - No object of focus needed
- **Horrid Detail** - See through supernatural disguises
- **Network** - Detect supernatural influence and contacts

---

#### Repel the Unnatural 🛡️
**Drive away supernatural creatures**

You can force monsters to flee or keep them at bay. Your presence, backed by faith or will, repels the unnatural.

**Base Benefit:**
- Force supernatural creatures away
- Requires object of focus (holy symbol, charm, etc.)
- Contested roll vs creature's power

**Herald Commands:**
```
/edge action:add (select "Repel the Unnatural")
/perks action:add edge_name:"Repel the Unnatural" perk_name:Ward
```

**Available Perks:**
- **Ward** - Extend protection radius ~2 meters
- **Damage** - Use focus object as melee weapon (10 aggravated damage)
- **Creature Specialization** - 2-dice bonus vs specific creature type
- **Handfree** - No object of focus needed

---

#### Thwart the Unnatural 💎
**Resist supernatural powers**

You can resist and negate supernatural abilities directed at you. Mind control, curses, and paranormal attacks fail against your will.

**Base Benefit:**
- Resist supernatural powers
- Requires object of focus (talisman, ritual, etc.)
- Roll to counter incoming power

**Herald Commands:**
```
/edge action:add (select "Thwart the Unnatural")
/perks action:add edge_name:"Thwart the Unnatural" perk_name:Recognition
```

**Available Perks:**
- **Ward** - Extend protection radius ~2 meters
- **Creature Specialization** - 2-dice bonus vs specific creature type
- **Recognition** - Learn what the resisted power would have done
- **Handfree** - No object of focus needed
- **Redirection** - Redirect resisted ability back at the caster

---

#### Artifact ⚡
**Wield a supernatural relic**

You possess a genuine supernatural artifact. It's unique, powerful, and bonded to you. It might be a cursed blade, a holy relic, or something stranger.

**Base Benefit:**
- Own a supernatural object
- Object provides 1-dice bonus to specific action type
- Object is unique and permanent

**Herald Commands:**
```
/edge action:add (select Artifact)
/perks action:add edge_name:Artifact perk_name:Empower
```

**Available Perks:**
- **Empower** - Once per scene, increase bonus to 3 dice
- **Attraction** - Use as bait for supernatural creatures, 2-dice ambush bonus
- **Detection** - Acts like Sense the Unnatural
- **Shield** - Halve physical damage from supernatural sources
- **Feature Unlocked** - At Danger 5+, reroll failures (treat as crits)

---

#### Cleanse the Unnatural 🔥
**Remove supernatural influence**

You can purge supernatural effects, break enchantments, and free victims from paranormal control. You are a cleanser of corruption.

**Base Benefit:**
- Remove supernatural influence from people or places
- Break curses and enchantments
- Free mind-controlled victims

**Herald Commands:**
```
/edge action:add (select "Cleanse the Unnatural")
/perks action:add edge_name:"Cleanse the Unnatural" perk_name:"Bedside Manner"
```

**Available Perks:**
- **Bedside Manner** - Damage becomes superficial, rounded down
- **Trace the Threads** - Answer questions about controller's location
- **Inflict Stigmata** - +1 aggravated damage to target, -2 difficulty
- **Psychic Backlash** - Controller receives aggravated damage

---

#### Great Destiny ✨
**Protected by higher purpose**

You are marked by fate. A higher power (deity, universe, destiny itself) protects you because you have a role to play. You cannot die until your purpose is fulfilled.

**Base Benefit:**
- Supernatural protection from death
- Reduced damage in critical moments
- Sense of purpose and direction

**Herald Commands:**
```
/edge action:add (select "Great Destiny")
/perks action:add edge_name:"Great Destiny" perk_name:"Divine Protection"
```

**Available Perks:**
- **Divine Protection** - Reduce Health damage by 2
- **Heavenly Resolve** - Reduce social combat damage
- **Sacred Insight** - Once per story, receive supernatural clue about destiny
- **Influence Fate** - Force target to aid your destiny

---

#### Unnatural Changes 🧬
**Use your body in supernatural ways**

Your body has changed. Maybe you were experimented on, cursed, or altered by exposure to the supernatural. Now you can push your physical form beyond human limits.

**Base Benefit:**
- Enhance one physical attribute supernaturally
- Requires activation (difficulty 4)
- Lasts for scene
- Requires object of focus

**Herald Commands:**
```
/edge action:add (select "Unnatural Changes")
/perks action:add edge_name:"Unnatural Changes" perk_name:Breadth
```

**Available Perks:**
- **Breadth** - Select second physical attribute to enhance
- **Maximized Neuropathways** - Activation doesn't use action
- **Neuropathway Practice** - Reduce activation difficulty from 4 to 3
- **Handsfree** - No object of focus needed

---

## Managing Perks

### What are Perks?

**Perks** are specialized abilities within each Edge. They customize and enhance your Edges, making them more powerful or versatile.

### Adding Perks

```
/perks action:add
```

Herald will:
1. Show only Edges you currently have
2. Show only Perks available for selected Edge
3. Filter out Perks you already possess

**Example:**
```
/perks action:add edge_name:Arsenal perk_name:Exotics
```

### Viewing Your Perks

```
/perks action:view
```

Shows all Perks across all your Edges.

**View Perks for Specific Edge:**
```
/perks action:view edge_name:Arsenal
```

### Removing Perks

```
/perks action:remove edge_name:Arsenal perk_name:Exotics
```

---

## Edge Strategy

### Choosing Your First Edge

Consider your character concept:

**Combat Focused:**
- Arsenal (weapons)
- Fleet (mobility)
- Ordnance (explosives)

**Investigation Focused:**
- Library (research)
- Sense the Unnatural (detection)
- Global Access (digital investigation)

**Infiltration Focused:**
- Turncoat (deception)
- Improvised Gear (adaptability)
- Beast Whisperer (scouts)

**Support/Protection:**
- Thwart the Unnatural (protect allies)
- Cleanse the Unnatural (remove curses)
- Great Destiny (stay alive)

### Building Edge Combinations

Edges work well together:

- **Arsenal + Fleet** = Mobile firepower
- **Library + Sense the Unnatural** = Expert monster hunter
- **Global Access + Drone Jockey** = Digital surveillance master
- **Improvised Gear + Arsenal** = Tactical versatility
- **Turncoat + Beast Whisperer** = Master infiltrator

### Investing in Perks

Each Perk makes your Edge more powerful:

1. **Start broad** - Get multiple Edges for versatility
2. **Then specialize** - Add Perks to your most-used Edge
3. **Complement your Creed** - Match Edges to your hunting style
4. **Cover weaknesses** - Use Edges to shore up skill gaps

---

## Edge Limitations

### Objects of Focus

Some Edges require an **object of focus**:
- Sense the Unnatural - Detection item
- Repel the Unnatural - Holy symbol or charm
- Thwart the Unnatural - Protective talisman
- Unnatural Changes - Trigger item

These objects can be lost, destroyed, or taken away, limiting your Edge use.

**Handfree Perk:** Several Edges have a "Handfree" Perk that removes this requirement.

### Margin-Based Quality

Asset Edges (Arsenal, Fleet, Ordnance) provide equipment based on your **margin of success**:

- Margin 0-1: Basic quality
- Margin 2-3: Professional quality
- Margin 4+: Exceptional quality

This means your Edge's effectiveness varies based on how well you roll.

### Storyteller Discretion

Edges are powerful but not unlimited:
- Arsenal can't provide a tank in downtown
- Fleet won't give you a jet aircraft
- Library doesn't know *everything*

Work with your Storyteller to determine reasonable Edge manifestations.

---

## Edge Examples

### Example 1: Arsenal in Action

**Situation:** Need to take down a vampire nest
**Edge:** Arsenal
**Perks:** Exotics, Team Requisition

```
Roll for Arsenal: 5 successes (margin 3)
Result: You requisition silver-loaded hollow point rounds
        (Exotics Perk) and provide copies to your entire
        cell (Team Requisition Perk).
```

### Example 2: Library Research

**Situation:** Researching a mysterious symbol
**Edge:** Library
**Perks:** Who They Are, Binge

```
Roll for Library: 4 successes
Result: With "Who They Are" Perk, you identify the symbol
        as belonging to a specific vampire bloodline.
        With "Binge" Perk, research takes 2 hours instead of 4.
```

### Example 3: Sense the Unnatural

**Situation:** Walking through suspected vampire haven
**Edge:** Sense the Unnatural
**Perks:** Creature Specialization (Vampires), Range

```
Roll with +2 dice (Creature Specialization):
Result: 3 successes
Your sense extends to the entire city block (Range Perk).
You detect 2 vampires in the building, third floor, east side.
```

---

## Quick Reference

### All 17 Edges

**Assets:** Arsenal, Fleet, Ordnance, Library, Experimental Medicine
**Aptitudes:** Improvised Gear, Global Access, Drone Jockey, Beast Whisperer, Turncoat
**Endowments:** Sense the Unnatural, Repel the Unnatural, Thwart the Unnatural, Artifact, Cleanse the Unnatural, Great Destiny, Unnatural Changes

### Herald Commands

```
/edge action:add          # Add new Edge
/edge action:view         # View your Edges
/edge action:remove       # Remove Edge

/perks action:add         # Add Perk to Edge
/perks action:view        # View all Perks
/perks action:remove      # Remove Perk
```

---

## Next Steps

- **[Creeds](creeds.md)** - Choose your hunting philosophy
- **[Desperation](desperation.md)** - Understand the cost of power
- **[Progression](progression.md)** - Learn how to gain new Edges
- **[Hunter Mechanics Guide](../guides/hunter-mechanics.md)** - Advanced Edge tactics

Or return to the [H5E Overview](overview.md)!

---

🔸 **Choose your Edge. Master your power. Hunt the night.**
