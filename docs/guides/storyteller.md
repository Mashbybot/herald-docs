# Storyteller Guide

A comprehensive guide for running Hunter: The Reckoning 5th Edition games using Herald.

This guide covers campaign management, XP awards, handling Desperation and Despair, and getting the most out of Herald's features.

---

## Table of Contents

1. [Setting Up Your Chronicle](#setting-up-your-chronicle)
2. [Managing Characters](#managing-characters)
3. [Awarding Experience](#awarding-experience)
4. [Setting Difficulties](#setting-difficulties)
5. [Handling Desperation and Despair](#handling-desperation-and-despair)
6. [Campaign Pacing](#campaign-pacing)
7. [Storyteller Tools](#storyteller-tools)

---

## Setting Up Your Chronicle

### Before the First Session

**1. Establish the setting:**
- Where does the chronicle take place?
- What supernatural threats exist?
- What's the initial hook?

**2. Set player expectations:**
- Tone (horror, action, investigation)
- Power level (starting characters)
- Campaign length (short arc or ongoing)
- Session frequency

**3. Coordinate character creation:**
- Allow players to use `/create` and build characters
- Review characters with `/sheet character:PlayerName`
- Ensure diverse party composition
- Approve Edges and starting builds

**4. Establish the cell:**
- How did the Hunters meet?
- What binds them together?
- Do they have a Safehouse?
- What resources do they share?

### Session Zero

**Character introductions:**
- Each player presents their Hunter
- Discuss Creeds and Drives
- Identify potential conflicts
- Find common ground

**Establish boundaries:**
- Content warnings and safety tools
- Roleplay vs. roll-play expectations
- House rules (if any)
- Communication preferences

**Set the stage:**
- Introduce the initial threat
- Establish the first lead
- End with a hook for Session 1

---

## Managing Characters

### Viewing Player Characters

**View any character:**
```
/sheet character:PlayerName
```

**What to check:**
- Attribute and skill distribution
- Health and Willpower
- Desperation and Danger levels
- Edges and Perks
- XP totals

### Character Approval

**Review for:**
- **Balance:** No min-maxing that breaks the game
- **Concept fit:** Matches the chronicle tone
- **Party composition:** Fills a needed role
- **Legality:** Follows H5E character creation rules

**Common issues:**
- All combat, no social/investigation
- Dump stats (Attributes at 1)
- Concept doesn't fit the setting
- Duplicate roles (three snipers)

### Tracking Multiple Characters

**Best practices:**
- Keep a list of all player characters
- Note key NPCs and relationships
- Track cell resources (Safehouses, Contacts, etc.)
- Monitor overall party Desperation levels

---

## Awarding Experience

### XP Recommendations

**Per Session (3-5 hours):**
- **Attendance:** 1-2 XP (just for showing up)
- **Accomplishments:** 1-3 XP (based on success)
- **Roleplay:** 0-1 XP (exceptional character work)
- **Chronicle advancement:** 1-2 XP (moving story forward)

**Total:** 3-5 XP per session average

**Per Story Arc (3-6 sessions):**
- **Bonus:** 2-5 XP for completing major arc
- **Awards for character growth**
- **Bonus for exceptional play**

### Awarding XP with Herald

**Grant XP to a player:**
```
/xp action:add amount:4 reason:Session 3 - Defeated the vampire nest
```

**Track why XP was awarded:**
- Use descriptive reason text
- Helps players understand rewards
- Creates XP history

**Set total XP (campaign start):**
```
/xp action:set amount:20
```
(Use when starting mid-campaign)

### XP Philosophy

**Reward behavior you want to see:**
- Good roleplay (1 XP bonus)
- Teamwork and cooperation (1 XP bonus)
- Creative problem-solving (1 XP bonus)
- Advancing personal storylines (1 XP bonus)
- Facing Desperation choices (1 XP bonus)

**Don't punish:**
- Character deaths (rebuild with same XP)
- Failed rolls (failure is part of the story)
- Entering Despair (it's a feature, not a bug)

### Milestone vs. Session XP

**Session XP (recommended):**
- Award 3-5 XP every session
- Steady progression
- Predictable advancement

**Milestone XP:**
- Award larger chunks (10-15 XP) at story milestones
- Slower progression
- More dramatic improvements

**Hybrid:**
- 2-3 XP per session
- 5-10 XP bonus at arc completion
- Balanced approach

---

## Setting Difficulties

### Standard Difficulties

**Difficulty 1:** Trivial
- Shooting an unaware, stationary target
- Persuading someone who already trusts you
- Finding obvious clues

**Difficulty 2:** Standard
- Most routine tasks
- Combat against equal opponents
- Social interaction with neutral NPCs
- Basic investigation

**Difficulty 3:** Challenging
- Difficult tasks requiring skill
- Combat against superior foes
- Persuading hostile NPCs
- Finding hidden clues

**Difficulty 4:** Hard
- Expert-level tasks
- Combat against overwhelming foes
- Swaying fanatical opposition
- Uncovering deeply buried secrets

**Difficulty 5+:** Extreme
- Near-impossible tasks
- Reserved for climactic moments
- May require Desperation to succeed

### Modifying Difficulty

**Lower difficulty when:**
- Player has excellent roleplay
- Creative approach
- Using appropriate tools/resources
- Specialty applies
- Edge provides advantage

**Raise difficulty when:**
- Poor conditions (darkness, weather)
- Time pressure
- Inadequate tools
- Opposition is alert
- Multiple complications

**Example:**
- Base: Lockpicking a door = Difficulty 2
- + Professional lock = +1 difficulty
- + Proper tools = -1 difficulty
- + Taking time = -1 difficulty
- Final: Difficulty 1

### Contested Rolls

**When NPCs oppose players:**

**Option 1: Static difficulty**
- Set difficulty based on NPC capability
- Vampire (Stealth 4) = Difficulty 4 to spot
- Fast and simple

**Option 2: Opposed rolls**
- Both roll, compare successes
- More dynamic
- Slower but more engaging

**Example (opposed):**
```
Player: /roll pool:5 difficulty:0 comment:Sneaking past the guard
NPC: Storyteller rolls Wits 2 + Awareness 3 = 5 dice
Compare successes: Player 3 vs. NPC 2 = Player wins
```

---

## Handling Desperation and Despair

### When Players Use Desperation

**They roll with `desperate:true`:**
```
/roll pool:7 difficulty:3 desperate:true comment:Must succeed!
```

**Herald adds their Desperation rating as extra dice**

**Watch for Desperation dice showing 1s:**

**Success + Desperation 1s = Overreach:**
Player chooses:
1. Keep success + gain Danger equal to number of 1s
2. Reject success + enter Despair

**Failure + Desperation 1s = Automatic Despair:**
No choice - they enter Despair immediately

### Tracking Danger

**When Overreach occurs:**
```
/danger amount:+2
```
(Add number of Desperation 1s rolled)

**Danger effects:**
- Raises difficulty on future rolls
- Increases risk of Despair
- Represents cosmic consequences

**Reducing Danger:**
- Downtime and rest (-1 per session)
- Completing Redemption
- Storyteller discretion

### Handling Despair

**When a Hunter enters Despair:**

1. **Mark Despair:**
```
/despair
```
(Herald automatically loses their Drive)

2. **Narrate the moment:**
- Describe their loss of control
- Show the darkness consuming them
- Make it memorable and impactful

3. **Immediate consequences:**
- Drive is lost (no longer motivates them)
- May act out violently or withdraw
- Scene becomes about their struggle

4. **Plan Redemption:**
- Work with player to define Redemption path
- Usually related to their Drive
- Should take 1-3 sessions

**Redemption examples:**

**Vengeance Drive:**
- Redemption: Hurt your quarry
- Must damage/defeat the one they hunt

**Virtue Drive:**
- Redemption: Uphold your moral code in the face of darkness
- Must resist temptation, do the right thing

**Curiosity Drive:**
- Redemption: Uncover a significant truth
- Must learn important information

**When Redemption is complete:**
```
/redemption
```
(Herald restores their Drive)

### Desperation Strategy Guidance

**Encourage Desperation use:**
- Make some challenges require it
- Reward players who embrace the risk
- Don't punish Despair (it's part of the story)

**Don't overuse:**
- Not every roll needs Desperation
- Routine tasks shouldn't require it
- Let players conserve for critical moments

**Make it meaningful:**
- Desperation dice should matter
- Narrate the supernatural push
- Show the cost visually

---

## Campaign Pacing

### Session Structure

**Opening (15-30 minutes):**
- Recap last session
- Check character status (`/sheet`)
- Set the scene

**Investigation/Exploration (60-90 minutes):**
- Players pursue leads
- Roll Investigation, Awareness, Social skills
- Uncover information

**Confrontation (30-60 minutes):**
- Combat or major social encounter
- Use Desperation
- High stakes

**Resolution (15-30 minutes):**
- Deal with consequences
- Award XP
- Set up next session

### Story Arc Pacing

**Arc 1 (Sessions 1-4):** Introduction
- Meet the cell
- First supernatural threat
- Learn the basics
- **XP:** 12-20 total

**Arc 2 (Sessions 5-8):** Rising Action
- Deeper conspiracy
- Personal stakes
- First major Desperation/Despair moments
- **XP:** 24-40 total

**Arc 3 (Sessions 9-12):** Climax
- Major threat revealed
- Cell works together
- High Desperation use
- **XP:** 36-60 total

**Arc 4+ (Sessions 13+):** Ongoing
- New threats
- Character advancement
- Edge acquisition
- **XP:** 60+ total

### Advancement Milestones

**Novice (0-20 XP):**
- Learning the ropes
- Basic character builds
- First Edge only

**Experienced (21-50 XP):**
- Competent Hunters
- Second Edge or multiple Perks
- Specialized builds emerging

**Veteran (51-100 XP):**
- Expert Hunters
- Multiple Edges and Perks
- Highly optimized

**Elite (101+ XP):**
- Master Hunters
- Maximum capabilities
- Legendary

---

## Storyteller Tools

### Managing NPCs

**Track key NPCs:**
- Name and role
- Relationship to cell
- Secrets and motivations
- Contact information (if using Contacts Edge)

**NPC stat blocks:**
- Use simplified stats (don't need full sheets)
- Key attribute + skill pools
- Special abilities
- Health/damage capacity

**Example NPC:**
```
Detective Sarah Mills
- Investigation pool: 6 dice (Int 3 + Investigation 3)
- Awareness pool: 5 dice (Wits 2 + Awareness 3)
- Persuasion pool: 5 dice (Cha 3 + Persuasion 2)
- Health: 5
- Note: Secretly knows about vampires, doesn't trust the cell yet
```

### Tracking Threats

**Supernatural enemies:**
- Creature type (vampire, werewolf, ghost, etc.)
- Power level (weak minion vs. ancient master)
- Goals and motivations
- Weaknesses and vulnerabilities

**Combat stats:**
- Attack pools
- Defense pools
- Damage dealt
- Special abilities

**Example Threat:**
```
Vampire Elder - Marcus Vane
- Attack pool: 8 dice (Dex 4 + Brawl 4)
- Dodge pool: 7 dice (Dex 4 + Athletics 3)
- Damage: Strength 5 + 2 (claws) = 7 lethal
- Special: Mesmerism (Manipulation 5 + Persuasion 4 = 9 dice)
- Health: 10
- Weaknesses: Sunlight, stake to heart, fire
```

### Session Prep

**Minimal prep:**
- Key NPC stats
- Main threat stats
- 3-5 clues/leads
- Potential complications

**Don't overprepare:**
- Players will surprise you
- Herald handles mechanics
- Focus on story, not stats

### Handling Edge Perks

**Asset Edges (Arsenal, Contacts, etc.):**
- Work with players on what they can access
- Set reasonable limits
- Require in-game justification

**Aptitude Edges (Fleet, Inspire, etc.):**
- Describe supernatural effects narratively
- Provide mechanical benefits as stated
- Make them feel special

**Endowment Edges (Artifact, Third Eye, etc.):**
- Emphasize mystical/supernatural nature
- Create story around their use
- Tie to larger mysteries

---

## Common Storyteller Scenarios

### "Can I use Desperation?"

**Answer: "Yes, but..." **
- Remind them of the risk
- Check their current Danger
- Let them decide
- Never forbid it (part of the game)

### "I'm in Despair, now what?"

**Guide them to Redemption:**
- Define clear path based on Drive
- Make it achievable in 1-3 sessions
- Don't make it trivial
- Roleplay the struggle

### "Can I buy this Edge/Perk?"

**Consider:**
- Does it fit their character concept?
- Can they justify it in-story?
- Do they have the XP? (10-20 XP typical)
- Does it break game balance?

**Answer:** Usually yes if they can justify it

### "How much XP for...?"

**Reference costs:**
- Attributes: new rating × 4 XP
- Skills: new rating × 2 XP
- Specialties: 3 XP
- Edges: 10-20 XP (your discretion)
- Perks: 5-10 XP (your discretion)

---

## Troubleshooting

### Players not using Desperation

**Solutions:**
- Make some challenges require it
- Show NPCs using similar power
- Reward Desperation use with bonus XP
- Make consequences interesting, not just punishment

### Too much combat

**Solutions:**
- Add investigation scenes
- Introduce social challenges
- Make combat consequences severe
- Reward non-combat solutions

### Party not working together

**Solutions:**
- Create threats that require teamwork
- Reward cooperation with bonus XP
- Use cell-based Edges (Safehouse, Contacts)
- Emphasize shared goals

### One player dominates

**Solutions:**
- Create scenes targeting other characters
- Spotlight quiet players
- Use Drives and Ambitions to engage everyone
- Talk to the player privately

---

## Quick Reference

### XP Awards
```
/xp action:add amount:4 reason:Session 3 - Completed investigation
```

### Difficulties
- 1: Trivial
- 2: Standard (most tasks)
- 3: Challenging
- 4: Hard
- 5+: Extreme

### Desperation Results
- **Success + 1s:** Overreach (choose: keep success + Danger, or Despair)
- **Failure + 1s:** Automatic Despair

### Managing Danger
```
/danger amount:+2    # Increase
/danger amount:-1    # Decrease
```

---

## Related Documentation

- **[Getting Started](getting-started.md)** - Player introduction
- **[Playing Guide](playing.md)** - Session gameplay
- **[Desperation Mechanics](../h5e/desperation.md)** - Full Desperation rules
- **[Progression](../h5e/progression.md)** - XP and advancement
- **[H5E Overview](../h5e/overview.md)** - Complete system guide

---

🔸 **Guide your Hunters. Shape their story. Master the Hunt.**
