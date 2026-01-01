# Playing with Herald

A session-by-session guide to using Herald during Hunter: The Reckoning 5th Edition gameplay.

This guide covers common workflows, scene types, and how to use Herald commands effectively during actual play.

---

## Table of Contents

1. [Before the Session](#before-the-session)
2. [Investigation Scenes](#investigation-scenes)
3. [Social Scenes](#social-scenes)
4. [Combat Scenes](#combat-scenes)
5. [Between Scenes](#between-scenes)
6. [After the Session](#after-the-session)
7. [Common Workflows](#common-workflows)

---

## Before the Session

### Prepare Your Character

**1. Review your sheet:**
```
/sheet
```

Know your:
- Key dice pools (combat, social, investigation)
- Current Health and Willpower
- Desperation rating
- Active Edges and Perks

**2. Check your identity:**
```
/sheet
```

Confirm your:
- Creed and Drive (are you in Despair?)
- Ambition and Desire (what are you pursuing?)
- Current Danger level

**3. Plan your approach:**
- What's the session goal?
- What's your character's personal goal?
- How will you contribute to the cell?

### Coordinate with Your Cell

**Discuss roles:**
- Who handles combat?
- Who leads social interactions?
- Who investigates and researches?
- Who provides support/healing?

**Share information:**
- What did you learn last session?
- What are your current leads?
- What resources do you have?

**Plan tactics:**
- How will you approach the threat?
- What's your backup plan?
- Who takes point in different situations?

---

## Investigation Scenes

### Searching for Clues

**Basic investigation roll:**
```
/roll pool:7 difficulty:2 comment:Searching the crime scene
```
(Intelligence + Investigation)

**Common investigation pools:**
- **Crime scenes:** Intelligence + Investigation
- **Research:** Intelligence + Academics or Occult
- **Tracking:** Wits + Survival
- **Noticing details:** Wits + Awareness
- **Forensics:** Intelligence + Medicine or Science

### Example Investigation Sequence

**Scene:** Investigating a vampire's lair

**1. Initial survey:**
```
/roll pool:5 difficulty:2 comment:Looking around the lair
```
(Wits 3 + Awareness 2)

**2. Detailed search:**
```
/roll pool:7 difficulty:3 comment:Searching for evidence
```
(Intelligence 3 + Investigation 4)

**3. Occult analysis:**
```
/roll pool:6 difficulty:2 comment:Identifying vampire markings
```
(Intelligence 3 + Occult 3)

**4. Following tracks:**
```
/roll pool:4 difficulty:3 comment:Tracking the vampire
```
(Wits 3 + Survival 1)

### When to Use Desperation

**Consider Desperation when:**
- Time is critical (victim still alive)
- Clue is essential to the case
- Failure means the trail goes cold

**Example:**
```
/roll pool:7 difficulty:4 desperate:true comment:MUST find where they went!
```

**Risk:**
- Desperation dice show 1s = Overreach or Despair
- Balance urgency against your Danger level

### Investigation Tips

**Before rolling:**
- Ask the Storyteller what you're looking for
- Clarify the difficulty
- Describe your approach (might reduce difficulty)

**After rolling:**
- Successes reveal information
- Margin of success = depth of information
- Failure doesn't mean nothing happens (Storyteller still narrates)

---

## Social Scenes

### Persuasion and Influence

**Basic persuasion roll:**
```
/roll pool:6 difficulty:2 comment:Convincing the witness to talk
```
(Manipulation + Persuasion)

**Common social pools:**
- **Persuade:** Manipulation + Persuasion
- **Intimidate:** Strength or Manipulation + Intimidation
- **Deceive:** Manipulation + Subterfuge
- **Read someone:** Wits + Insight
- **Lead/inspire:** Charisma + Leadership
- **Perform/disguise:** Charisma + Performance

### Example Social Sequence

**Scene:** Interrogating a suspect who knows about vampires

**1. Read their demeanor:**
```
/roll pool:5 difficulty:2 comment:Sizing up the suspect
```
(Wits 3 + Insight 2)

**2. Build rapport:**
```
/roll pool:6 difficulty:2 comment:Getting them to trust me
```
(Charisma 3 + Persuasion 3)

**3. Ask the hard questions:**
```
/roll pool:6 difficulty:3 comment:Pressing for the truth
```
(Manipulation 2 + Intimidation 4)

**4. Detect lies:**
```
/roll pool:5 difficulty:3 comment:Is he telling the whole truth?
```
(Wits 3 + Insight 2)

### Using Edge Perks

**Contacts:**
- Call in favors for information
- Leverage your network
- Get access to restricted areas

**Fame:**
- Use celebrity status to open doors
- Leverage public influence
- Manipulate media attention

**Status:**
- Exercise authority
- Bypass bureaucracy
- Command respect

### Social Tips

**Roleplay first, roll second:**
- Describe your approach
- Good roleplaying may reduce difficulty
- Bad approach may increase difficulty

**Know when to walk away:**
- Failed Persuasion doesn't mean try again immediately
- Consider different approaches
- Come back with new leverage

---

## Combat Scenes

### Initiative and Turn Order

**Storyteller determines initiative:**
- Usually Wits + Dexterity
- Higher rolls act first

### Attack Rolls

**Ranged attack (Firearms):**
```
/roll pool:7 difficulty:2 comment:Shooting the ghoul
```
(Dexterity 4 + Firearms 3)

**Melee attack:**
```
/roll pool:5 difficulty:2 comment:Swinging the bat at the vampire
```
(Strength 3 + Melee 2)

**Unarmed attack:**
```
/roll pool:6 difficulty:2 comment:Punching the cultist
```
(Strength 3 + Brawl 3)

### Defense Rolls

**Dodge:**
```
/roll pool:5 difficulty:2 comment:Dodging the vampire's claws
```
(Dexterity 3 + Athletics 2)

**Soak damage:**
```
/roll pool:4 difficulty:2 comment:Toughing out the hit
```
(Stamina 2 + Resolve 2)

### Taking Damage

**When hit:**
```
/damage amount:3 type:lethal
```

**Damage types:**
- **Superficial** - Minor wounds, bruises
- **Lethal** - Serious injuries, bleeding

**Tracking:**
- Herald automatically marks your Health track
- Superficial fills from left
- Lethal fills from right
- Incapacitated when they meet

### Healing in Combat

**Quick patch:**
```
/heal amount:2 type:superficial
```

**Medical attention:**
```
/roll pool:7 difficulty:2 comment:Field medicine on wounded ally
```
(Intelligence 3 + Medicine 4)

### Using Desperation in Combat

**Life-or-death moment:**
```
/roll pool:7 difficulty:3 desperate:true comment:Must kill the vampire leader!
```

**When to use:**
- You're about to die
- Ally is about to die
- Critical moment in the fight
- Final strike opportunity

**Risk:**
- Desperation 1s = Overreach or Despair
- In Despair, you lose your Drive
- May enter frenzy or lose control

### Combat Example Sequence

**Round 1:**

**Hunter 1 (You):**
```
/roll pool:7 difficulty:2 comment:Shooting vampire
```
Success! Deal damage.

**Hunter 2 (Ally):**
Attacks with melee weapon.

**Vampire:**
Attacks Hunter 2.
```
/damage amount:4 type:lethal
```

**Round 2:**

**Hunter 1 (You):**
```
/roll pool:7 difficulty:3 desperate:true comment:Finishing shot!
```
Using Desperation for extra dice!

**Hunter 2 (Ally):**
```
/heal amount:2 type:superficial
```
Quick patch between attacks.

**Vampire:**
Flees or dies.

### Combat Tips

**Positioning matters:**
- Describe your tactics
- Cover provides bonuses
- High ground helps
- Flanking may reduce difficulty

**Focus fire:**
- Multiple Hunters attack one threat
- Eliminate enemies quickly
- Protect wounded allies

**Know when to retreat:**
- Low Health = run
- Out of Willpower = run
- High Danger + Desperation = don't use Desperation
- Sometimes survival is victory

---

## Between Scenes

### Managing Resources

**Check your status:**
```
/sheet
```

Review:
- Health (heal if needed)
- Willpower (spend carefully)
- Desperation (rising or stable?)
- Danger (too high = risk Despair)

**Heal between fights:**
```
/heal amount:3 type:superficial
```

**Recover Willpower:**
- Storyteller awards Willpower for good roleplay
- Fulfilling Ambition/Desire
- Pursuing Drive

### Raising Danger

**When Danger increases:**
```
/danger amount:+2
```
(Storyteller tracks this when you Overreach)

**When Danger decreases:**
```
/danger amount:-1
```
(Storyteller may allow this in downtime)

**Monitor carefully:**
- High Danger = risky to use Desperation
- Danger 8+ = extremely dangerous
- Reduce through rest and Redemption

### Planning Next Steps

**Discuss with your cell:**
- What did we learn?
- Where do we go next?
- What resources do we need?
- Who do we need to talk to?

**Use your Edges:**
- **Library:** Research the threat
- **Contacts:** Call for information
- **Arsenal:** Acquire weapons
- **Safehouse:** Plan in safety

---

## After the Session

### Experience Points

**Storyteller awards XP:**
```
/xp action:view
```

**Common XP awards:**
- Session attendance: 1-2 XP
- Accomplishments: 1-3 XP
- Good roleplay: 1 XP
- Advancing the chronicle: 1-2 XP

**Total typical:** 3-5 XP per session

### Spending XP

**Check your XP:**
```
/xp action:view
```

**Raise a skill:**
```
/skill_set skill:Firearms dots:4
```
Cost: 8 XP (new rating 4 × 2)

**Raise an attribute:**
```
/attributes attribute:Dexterity dots:5
```
Cost: 20 XP (new rating 5 × 4)

**Add a specialty:**
```
/specialty action:add skill:Investigation specialty:Forensics
```
Cost: 3 XP

**Save for later:**
- Edges and Perks (10-20 XP)
- Major attribute increases
- Building toward specific builds

### XP Strategy

**Short-term (0-20 XP):**
- Buy specialties (3 XP each)
- Raise key skills to 3-4
- Fill gaps in your skillset

**Mid-term (20-50 XP):**
- Raise primary skills to 4-5
- Increase secondary attributes
- Buy second Edge or Perks

**Long-term (50+ XP):**
- Raise primary attributes to 4-5
- Master your specialty
- Optimize your build

### Session Recap

**Update your notes:**
- NPCs encountered
- Clues discovered
- Threats identified
- Personal character developments

**Adjust Ambition/Desire:**
```
/desire desire:New immediate goal
```

**Plan character progression:**
- What do I want to improve?
- What would help the cell?
- What fits my character concept?

---

## Common Workflows

### Investigation Workflow

1. **Arrive at scene**
2. **/roll Wits + Awareness** (initial survey)
3. **/roll Intelligence + Investigation** (detailed search)
4. **/roll Intelligence + Occult** (identify supernatural elements)
5. **Follow leads** (more rolls as needed)
6. **Report findings to cell**

### Social Encounter Workflow

1. **Approach NPC**
2. **/roll Wits + Insight** (read their mood)
3. **Roleplay opening conversation**
4. **/roll Charisma/Manipulation + Social skill** (persuade, intimidate, etc.)
5. **/roll Wits + Insight** (detect lies if suspicious)
6. **Conclude interaction**

### Combat Workflow

1. **Initiative determined**
2. **Your turn:**
   - Declare action
   - **/roll Dexterity + Combat skill** (attack)
   - Apply damage to enemy
3. **Enemy turn:**
   - **/roll Dexterity + Athletics** (dodge if targeted)
   - **/damage amount:X type:Y** (if hit)
4. **Repeat until combat ends**
5. **After combat:**
   - **/heal** if wounded
   - Check Desperation/Danger
   - Loot/investigate

### Desperation Decision Workflow

1. **Face difficult challenge**
2. **Assess:**
   - How critical is success?
   - What's your current Danger?
   - Can you afford to fail?
3. **Decide:**
   - Use Desperation? `/roll pool:X difficulty:Y desperate:true`
   - Or play it safe? `/roll pool:X difficulty:Y`
4. **If Overreach occurs:**
   - Choose: Keep success + gain Danger
   - Or: Reject success, enter Despair
5. **If Despair:**
   - **/despair** (lose Drive)
   - Plan Redemption path

---

## Quick Reference

### Common Rolls

**Investigation:**
```
/roll pool:7 difficulty:2 comment:Investigating
```
(Intelligence + Investigation)

**Combat (Ranged):**
```
/roll pool:7 difficulty:2 comment:Shooting
```
(Dexterity + Firearms)

**Combat (Melee):**
```
/roll pool:5 difficulty:2 comment:Melee attack
```
(Strength/Dexterity + Melee)

**Social (Persuade):**
```
/roll pool:6 difficulty:2 comment:Persuading
```
(Manipulation + Persuasion)

**Awareness:**
```
/roll pool:5 difficulty:2 comment:Noticing
```
(Wits + Awareness)

### Common Commands

```
/sheet                               # View character
/roll pool:X difficulty:Y            # Basic roll
/roll pool:X difficulty:Y desperate:true  # Desperation roll
/damage amount:X type:Y              # Take damage
/heal amount:X type:Y                # Heal damage
/xp action:view                      # Check XP
```

---

## Related Documentation

- **[Getting Started](getting-started.md)** - New player guide
- **[Character Creation](character-creation.md)** - Building your Hunter
- **[Storyteller Guide](storyteller.md)** - For game masters
- **[Advanced Guide](advanced.md)** - Optimization and tactics
- **[Dice Mechanics](../h5e/dice-mechanics.md)** - Full dice rules
- **[Desperation](../h5e/desperation.md)** - Desperation system
- **[Command Reference](../commands/index.md)** - All commands

---

🔸 **Roll the dice. Face the darkness. Survive the Hunt.**
