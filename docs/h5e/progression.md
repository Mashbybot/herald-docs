# Character Progression

Hunters advance through experience, becoming more skilled and powerful over time. This page covers Experience Points (XP), costs for improvements, and how to advance your character in Herald.

---

## Experience Points (XP)

### What is XP?

**Experience Points** represent your character's growth through gameplay. You earn XP from:

- Completing sessions (typically 1-3 XP per session)
- Accomplishing major goals
- Good roleplaying (Storyteller discretion)
- Overcoming challenges
- Character development moments

### XP Tracking

Herald tracks three XP values:

- **Total Earned** - All XP you've ever received
- **Spent** - XP used for improvements
- **Available** - Total - Spent (what you can spend now)

---

## Managing XP in Herald

### Viewing Your XP

```
/xp action:view
```

Displays:
- Total XP earned
- XP spent
- Available XP
- Recent XP history
- Spending guide with costs

### Adding XP (Storyteller)

```
/xp action:add amount:3 reason:"Completed vampire nest mission"
```

Adds XP to your total. Reason is optional but helpful for tracking.

### Spending XP

When you improve something (attributes, skills, etc.), XP is automatically deducted.

**Example:**
```
# You have 12 available XP
# Want to raise Firearms from 2 to 3

/skill_set skill:Firearms dots:3

# Cost: New rating × 2 = 3 × 2 = 6 XP
# Herald automatically spends 6 XP
# You now have 6 available XP
```

### Setting XP Directly (Storyteller)

```
/xp action:set amount:50
```

Sets your total earned XP to a specific value.

### Spending XP Manually

```
/xp action:spend amount:5 reason:"Purchased new Edge perk"
```

Manually record XP spent (useful for things not tracked automatically).

---

## Advancement Costs

### Attributes

**Cost:** New Rating × 4 XP

Attributes range from 1-5 and can never be 0.

| Improvement | New Rating | XP Cost |
|-------------|------------|---------|
| 1 → 2 | 2 | 8 XP |
| 2 → 3 | 3 | 12 XP |
| 3 → 4 | 4 | 16 XP |
| 4 → 5 | 5 | 20 XP |

**Example:**
```
# Raising Dexterity from 3 to 4
/attributes attribute:Dexterity dots:4
# Cost: 4 × 4 = 16 XP
```

**Note:** Raising Stamina, Resolve, or Composure also updates Health/Willpower automatically.

---

### Skills

**Cost:** New Rating × 2 XP

Skills range from 0-5.

| Improvement | New Rating | XP Cost |
|-------------|------------|---------|
| 0 → 1 | 1 | 2 XP |
| 1 → 2 | 2 | 4 XP |
| 2 → 3 | 3 | 6 XP |
| 3 → 4 | 4 | 8 XP |
| 4 → 5 | 5 | 10 XP |

**Example:**
```
# Raising Investigation from 2 to 3
/skill_set skill:Investigation dots:3
# Cost: 3 × 2 = 6 XP
```

**Tip:** Skills are cheaper than attributes. Invest in skills first for immediate power.

---

### Specialties

**Cost:** 3 XP each

Specialties provide bonus dice when applicable.

**Requirements:**
- Skill must have at least 1 dot
- Maximum specialties = skill dots (minimum 1)

**Example:**
```
# Adding "Pistols" specialty to Firearms 3
/specialty action:add skill:Firearms specialty:Pistols
# Cost: 3 XP
```

**Herald automatically tracks the cost** and prevents adding more specialties than allowed.

---

### Edges

**Cost:** Variable (Storyteller discretion)

Edges represent major supernatural advantages. Costs typically range from:

- **Assets** (Arsenal, Fleet, etc.): 10-15 XP
- **Aptitudes** (Improvised Gear, etc.): 10-15 XP
- **Endowments** (Sense the Unnatural, etc.): 15-20 XP

**Acquiring Edges:**
1. Discuss with Storyteller (must fit narrative)
2. Pay XP cost (tracked manually via `/xp spend`)
3. Add Edge to character (`/edge action:add`)

**Example:**
```
# Adding Sense the Unnatural (15 XP)
/xp action:spend amount:15 reason:"Purchased Sense the Unnatural Edge"
/edge action:add
(Select Sense the Unnatural)
```

---

### Edge Perks

**Cost:** Variable (3-10 XP, Storyteller discretion)

Perks enhance existing Edges with specialized abilities.

**Requirements:**
- Must have the Edge that the Perk belongs to
- Perk must make narrative sense

**Example:**
```
# Adding "Exotics" perk to Arsenal Edge (5 XP)
/xp action:spend amount:5 reason:"Purchased Arsenal: Exotics perk"
/perks action:add edge_name:Arsenal perk_name:Exotics
```

---

## Advancement Strategy

### Early Game (0-30 XP earned)

**Focus:** Core competencies

**Priorities:**
1. **Primary skills to 3 dots** - Your main abilities
2. **Add specialties** - Cheap power boost
3. **Round out skill gaps** - Get 1 dot in important skills
4. **Consider one Edge** - Major capability addition

**Example Build:**
```
Start: Firearms 2, Investigation 2, Stealth 1
Spend 10 XP:
- Firearms 2→3 (6 XP)
- Add specialty "Pistols" to Firearms (3 XP)
- Stealth 1→2 (4 XP total, spend 1 more)
```

### Mid Game (30-60 XP earned)

**Focus:** Excellence and versatility

**Priorities:**
1. **Primary skills to 4 dots** - Become expert
2. **Raise key attribute** - Expensive but valuable
3. **Add second Edge** - Expand capabilities
4. **More specialties** - Expertise in your focus areas

**Example Build:**
```
Raise Dexterity 3→4 (16 XP)
Firearms 3→4 (8 XP)
Add Sense the Unnatural Edge (15 XP)
Total: 39 XP
```

### Late Game (60+ XP earned)

**Focus:** Mastery and legendary abilities

**Priorities:**
1. **Skills to 5 dots** - Master level
2. **Attributes to 4-5** - Peak human capability
3. **Multiple Edges with Perks** - Supernatural powerhouse
4. **Complete specialty coverage** - Bonuses everywhere

**Example Build:**
```
Firearms 4→5 (10 XP)
Intelligence 3→4 (16 XP)
Add Library Edge (15 XP)
Add 3 Library Perks (15 XP)
Total: 56 XP
```

---

## XP Earning Rates

### Typical XP Awards

**Per Session:**
- Standard session: 1-2 XP
- Exceptional session: 3 XP
- Major milestone: 4-5 XP

**Special Awards:**
- Completing character Ambition: 3-5 XP
- Major story arc resolution: 2-3 XP
- Exceptional roleplaying: 1-2 XP
- Character development moment: 1 XP

### Campaign Progression

**Short Campaign (10 sessions):**
- Total XP: 15-30 XP
- Characters advance from competent to skilled

**Medium Campaign (25 sessions):**
- Total XP: 35-60 XP
- Characters become experts in their fields

**Long Campaign (50+ sessions):**
- Total XP: 70-150+ XP
- Characters achieve mastery and legend status

---

## Improvement Guidelines

### What Can You Improve?

**Anytime (with XP):**
- Skills (practice makes perfect)
- Specialties (focused training)

**Requires Narrative Justification:**
- Attributes (major life changes)
- Edges (supernatural events)
- Perks (using Edge creatively)

### Narrative Justification

Herald mechanics are tied to story. When improving:

**Skills:**
- "I've been practicing at the range" (Firearms)
- "I've been researching vampires every night" (Occult)
- "I've been following suspects" (Stealth)

**Attributes:**
- "Months of physical training" (Strength, Dexterity, Stamina)
- "Therapy and meditation" (Composure, Resolve)
- "Studying and reading constantly" (Intelligence)

**Edges:**
- "After that experience with the artifact, I can sense them now" (Sense the Unnatural)
- "My contacts came through with weapons" (Arsenal)
- "I've been experimenting with improvising gear" (Improvised Gear)

Work with your Storyteller to ensure improvements make sense.

---

## XP Spending Tips

### Efficiency

**Most Bang for Buck:**
1. **Specialties** (3 XP) - Cheap, immediate bonus
2. **Skills 0→1** (2 XP) - Remove untrained penalty
3. **Skills to 3** - Sweet spot of capability
4. **Edges** - Major new abilities

**Expensive But Worth It:**
1. **Key attributes to 4** - Foundation for everything
2. **Primary skills to 5** - Mastery in your specialty
3. **Multiple Edges** - Versatility and power

### Balanced vs. Specialized

**Balanced Character:**
- Spread XP across multiple skills
- Cover more situations
- More versatile in changing circumstances

**Example:**
```
30 XP spread:
Firearms 2→3 (6 XP)
Investigation 2→3 (6 XP)
Athletics 1→2 (4 XP)
Stealth 1→2 (4 XP)
Add 3 specialties (9 XP)
```

**Specialized Character:**
- Focus XP on one area
- Become the best at one thing
- Rely on team for other needs

**Example:**
```
30 XP focused:
Firearms 2→4 (4+8=14 XP)
Dexterity 3→4 (16 XP)
```

### Long-Term Planning

**100 XP Character Example:**

```
Starting Build:
Dexterity 3, Wits 3
Firearms 2, Investigation 2, Stealth 2

50 XP Spent:
- Dexterity 3→4 (16 XP)
- Firearms 2→4 (4+8=12 XP)
- Investigation 2→4 (4+8=12 XP)
- Add 3 specialties (9 XP)

Result at 50 XP:
Dexterity 4, Firearms 4, Investigation 4
With 3 specialties providing bonuses

Next 50 XP:
- Wits 3→4 (16 XP)
- Firearms 4→5 (10 XP)
- Add Sense the Unnatural (15 XP)
- Add 3 Perks to Sense (9 XP)

Result at 100 XP:
Master investigator and marksman with supernatural senses
```

---

## XP Log

Herald automatically logs all XP transactions:

```
/xp action:view
```

**Example Log:**
```
🔸 Experience Points for Sarah Martinez

Total Earned: 45 XP
Spent: 28 XP
Available: 17 XP

Recent History:
[2026-01-15] +3 XP: Completed vampire nest mission
[2026-01-14] -6 XP: Raised Investigation to 3
[2026-01-10] +2 XP: Session XP
[2026-01-08] -16 XP: Raised Dexterity to 4
```

This helps track your character's growth over time.

---

## Quick Reference

### XP Costs

- **Attributes:** New rating × 4 XP (8/12/16/20 XP)
- **Skills:** New rating × 2 XP (2/4/6/8/10 XP)
- **Specialties:** 3 XP each
- **Edges:** 10-20 XP (Storyteller discretion)
- **Perks:** 3-10 XP (Storyteller discretion)

### Herald Commands

```
/xp action:view                          # View XP and history
/xp action:add amount:X reason:"..."     # Add XP (Storyteller)
/xp action:spend amount:X reason:"..."   # Manually spend XP
/xp action:set amount:X                  # Set total XP (Storyteller)

/attributes attribute:Name dots:X        # Raise attribute (auto-spends XP)
/skill_set skill:Name dots:X             # Raise skill (auto-spends XP)
/specialty action:add skill:S specialty:N # Add specialty (auto-spends XP)

# Edges and Perks (manual XP spending required):
/xp action:spend amount:15 reason:"Purchased Edge"
/edge action:add                         # Then add the Edge
/perks action:add edge_name:E perk_name:P # Then add the Perk
```

### Typical Session Awards

- **Standard session:** 1-2 XP
- **Exceptional session:** 3 XP
- **Major milestone:** 4-5 XP
- **Special achievement:** +1 XP bonus

---

## Next Steps

- **[Attributes & Skills](attributes-skills.md)** - See what you can improve
- **[Edge](edge.md)** - Plan which Edges to acquire
- **[Dice Mechanics](dice-mechanics.md)** - Understand how improvements help rolls
- **[Creeds](creeds.md)** - Align progression with your character concept

Or return to the [H5E Overview](overview.md)!

---

🔸 **Grow stronger. Master your craft. Become legendary.**
