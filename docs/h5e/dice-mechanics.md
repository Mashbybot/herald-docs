# Dice Mechanics

Hunter: The Reckoning 5E uses a **d10 dice pool system** where you roll multiple ten-sided dice and count successes. Herald implements these mechanics faithfully, adding visual feedback and automation to make rolling smooth and clear.

---

## Core Dice Rolling

### The Basic System

```
1. Calculate dice pool: Attribute + Skill + Modifiers
2. Roll that many d10s
3. Count successes (6+ on each die)
4. Check for criticals (pairs of 10s)
5. Compare to difficulty
```

### Success Threshold

Each die result has a specific outcome:

- **1-5** = Failure (no success)
- **6-9** = Success (counts as 1 success)
- **10** = Success (counts as 1 success, can form critical pairs)

### Critical Successes

**Pairs of 10s** create critical successes:

- Each **pair of 10s** adds **2 additional successes**
- The 10s themselves still count as regular successes
- Multiple pairs can occur in large dice pools

**Example:**
```
Roll 6 dice: [10, 10, 8, 7, 6, 2]
Regular successes: 5 (10, 10, 8, 7, 6)
Critical pair: 1 pair of 10s = +2 successes
Total: 7 successes
```

---

## Rolling in Herald

### Basic Roll Command

The `/roll` command handles all dice rolling:

```
/roll pool:6 difficulty:2 comment:Breaking down the door
```

**Parameters:**
- `pool` (required) - Total number of dice to roll (1-20 typical, 100 max)
- `difficulty` (optional) - Target successes needed (0-6)
- `desperate` (optional) - Add Desperation dice (true/false)
- `comment` (optional) - Describe what you're rolling for

### Difficulty Levels

Herald uses standardized difficulty ratings:

| Difficulty | Target Successes | Description |
|-----------|-----------------|-------------|
| **0** | 0 | Automatic (no roll needed, but can check for crits) |
| **1** | 1 | Simple task |
| **2** | 2 | Standard task |
| **3** | 3 | Hard task |
| **4** | 4 | Extreme task |
| **5** | 5 | Nearly impossible |
| **6** | 6 | Legendary feat |

**Example:**
```
# Simple task (need 1 success)
/roll pool:5 difficulty:1 comment:Picking a simple lock

# Standard task (need 2 successes)
/roll pool:6 difficulty:2 comment:Investigating the crime scene

# Extreme task (need 4 successes)
/roll pool:8 difficulty:4 comment:Hacking a military server
```

---

## Understanding Roll Results

### Success vs. Failure

- **Success:** Total successes ≥ Difficulty
- **Failure:** Total successes < Difficulty
- **Margin:** The difference between successes and difficulty

**Example Success:**
```
Pool: 6 dice
Difficulty: 2
Result: [10, 9, 7, 6, 4, 2]
Successes: 4 (10, 9, 7, 6)
Outcome: SUCCESS with margin 2 (4 - 2 = 2)
```

**Example Failure:**
```
Pool: 5 dice
Difficulty: 3
Result: [7, 5, 4, 3, 1]
Successes: 1 (only the 7)
Outcome: FAILURE with margin -2 (1 - 3 = -2)
```

### Critical Success

When you roll pairs of 10s and succeed:

```
Pool: 8 dice
Difficulty: 3
Result: [10, 10, 10, 10, 8, 6, 4, 2]
Regular successes: 6 (four 10s, one 8, one 6)
Critical pairs: 2 pairs = +4 successes
Total: 10 successes
Outcome: CRITICAL SUCCESS with margin 7
```

!!! success "Critical Success Benefits"
    - Exceptional outcome
    - Maximum effect
    - May grant additional benefits (Storyteller discretion)
    - Impressive display of skill

---

## Visual Dice Display

Herald shows your rolls using emoji dice (or Unicode fallback):

### Regular Dice

- ⭐ **Critical 10** - Part of a pair
- 🎯 **Success** - 6-9
- ⚫ **Failure** - 1-5
- 💥 **Botch 1** - Failure on a 1

### Dice Sorting

Results are sorted for easy reading:
```
10s first → 6-9 → 1-5
⭐⭐🎯🎯⚫⚫
```

### Result Embed

Herald displays results in a colored embed:

- **Green** - Success
- **Gold** - Critical success
- **Gray** - Failure
- **Red/Orange** - Desperation warnings

---

## Desperation Dice

Desperation is the Hunter-specific mechanic that lets you push beyond normal limits at a cost.

### Using Desperation

```
/roll pool:5 desperate:true difficulty:2 comment:Must succeed!
```

**What Happens:**
1. Your **Desperation rating** (0-10) is added as extra dice
2. These dice are visually distinct (orange/gold emoji)
3. They can help you succeed...
4. ...but they come with risks

### Desperation Dice Display

- ✨ **Desperation Critical 10**
- 🟡 **Desperation Success** - 6-9
- 🟠 **Desperation Failure** - 2-5
- 🔥 **Desperation Botch 1**

**Example:**
```
Character Desperation: 3
Regular pool: 5 dice
Desperate roll: 5 regular + 3 Desperation = 8 total dice

Display:
Regular: 🎯🎯⚫⚫⚫
Desperation: ✨🟡🔥
```

### Messy Criticals

When Desperation dice contribute to a critical (pair of 10s):

!!! warning "Messy Critical"
    - You succeed brilliantly
    - But your Desperation shows
    - Supernatural traces left behind
    - Collateral damage or complications
    - Witnesses see something unusual

**Example:**
```
Roll: [10 regular, 10 Desperation, 8, 7, 6]
Result: Critical success (pair of 10s)
Warning: MESSY CRITICAL - One of the 10s was Desperation
```

### Overreach & Despair

Rolling **1s on Desperation dice** triggers consequences:

#### If You Succeed:
Choose one:

1. **Accept Overreach**
   - Keep your success
   - Gain Danger equal to number of Desperation 1s
   - Supernatural threat increases

2. **Enter Despair**
   - Reject the success (it becomes a failure)
   - Your Drive becomes unusable
   - Cannot use Desperation until Redeemed

#### If You Fail:
**Automatic Despair** - No choice

- The roll fails
- You enter Despair state
- Must complete Redemption to recover

**Example:**
```
Roll with Desperation: [8, 7, 6] + [1, 1] (Desperation)
Successes: 3 regular
Desperation 1s: 2
Outcome: Success, but...
Choice: Accept success + gain 2 Danger, OR enter Despair
```

---

## Advanced Rolling

### Modifiers and Bonuses

While Herald doesn't auto-calculate modifiers, you add them to your pool:

**Positive Modifiers:**
- Specialties: +2 dice (when applicable)
- Equipment bonuses: Variable
- Situational advantages: +1 to +3 dice
- Teamwork bonuses: +1 per helper

**Negative Modifiers:**
- Injury penalties: -1 to -3 dice
- Environmental penalties: -1 to -3 dice
- Danger rating: Adds to difficulty

**Example:**
```
Base pool: Dexterity (3) + Firearms (4) = 7 dice
Specialty "Pistols" applies: +2 dice
Taking cover: +1 die
Wounded: -2 dice
Final pool: 7 + 2 + 1 - 2 = 8 dice

/roll pool:8 difficulty:2 comment:Shooting from cover while wounded
```

### Danger Effects

Your character's **Danger rating** (0-10) adds to difficulty:

```
Character Danger: 3
Base difficulty: 2
Effective difficulty: 2 + 3 = 5

/roll pool:7 difficulty:5 comment:Acting while under supernatural threat
```

!!! danger "High Danger"
    - Danger 7+: All rolls become extremely difficult
    - Supernatural forces are closing in
    - Consider removing Danger (Storyteller action)

---

## Roll Outcomes

### Exceptional Success

Rolling **significantly above** the difficulty (margin of 3+):

- Task completed with style
- Additional benefits
- Impressive to witnesses
- May unlock new opportunities

**Example:**
```
Difficulty: 2
Result: 6 successes
Margin: 4 (exceptional)
Outcome: You don't just pick the lock - you do it silently,
         quickly, and without leaving any tool marks
```

### Marginal Success

Rolling **exactly** the difficulty or 1 above:

- Task completed adequately
- No extra benefits
- Job done but nothing special

**Example:**
```
Difficulty: 3
Result: 3 successes
Margin: 0 (marginal)
Outcome: You pick the lock, but it takes time and makes noise
```

### Marginal Failure

Rolling **1-2 below** the difficulty:

- Task fails but not catastrophically
- Partial information gained
- Can try again with penalty
- Minor consequences

**Example:**
```
Difficulty: 3
Result: 1 success
Margin: -2 (marginal failure)
Outcome: You can't pick the lock, but you know it's a
         high-security model that needs special tools
```

### Critical Failure

Rolling **zero successes** (no 6+ results):

- Complete failure
- Possible complications
- Storyteller may add consequences
- Retrying may be difficult or impossible

**Example:**
```
Difficulty: 2
Result: [5, 4, 3, 2, 1] = 0 successes
Outcome: You break your lockpick in the mechanism,
         and the lock is now jammed
```

---

## Contested Rolls

When two characters oppose each other:

### The Process

1. Both characters roll their relevant pools
2. Compare total successes
3. Higher successes wins
4. Margin = Winner's successes - Loser's successes

**Example:**
```
Hunter tries to sneak (Dexterity + Stealth):
/roll pool:6 difficulty:0 comment:Sneaking past guard
Result: 4 successes

Storyteller rolls guard's perception separately
Guard (Wits + Awareness): 3 successes

Outcome: Hunter wins by margin 1 (barely)
```

### Ties

If both get the same successes:

- Defender wins (status quo)
- Or both get partial success
- Or highest single die wins
- Storyteller decides

---

## Common Rolling Scenarios

### Combat Rolls

**Attacking:**
```
Dexterity + Firearms (shooting)
Dexterity + Brawl (punching)
Strength + Melee (swinging weapon)

/roll pool:7 difficulty:2 comment:Shooting at vampire
```

**Defending:**
```
Dexterity + Athletics (dodge)
Wits + Awareness (spot ambush)

/roll pool:6 difficulty:3 comment:Dodging attack
```

### Investigation Rolls

**Finding Clues:**
```
Intelligence + Investigation
Wits + Awareness
Intelligence + Occult (supernatural clues)

/roll pool:6 difficulty:2 comment:Searching the victim's apartment
```

**Research:**
```
Intelligence + Academics
Intelligence + Occult
Intelligence + Technology (digital research)

/roll pool:5 difficulty:3 comment:Researching vampire history
```

### Social Rolls

**Persuasion:**
```
Charisma + Persuasion (honest convincing)
Manipulation + Subterfuge (lying)
Charisma + Performance (acting)

/roll pool:6 difficulty:2 comment:Convincing cop to share info
```

**Intimidation:**
```
Strength + Intimidation (physical threat)
Manipulation + Intimidation (subtle menace)

/roll pool:5 difficulty:3 comment:Scaring suspect into talking
```

---

## Tips for Effective Rolling

### Building Bigger Pools

1. **Raise attributes and skills** - Core investment
2. **Get specialties** - +2 when applicable
3. **Use equipment** - Proper tools matter
4. **Get help** - Teamwork bonuses
5. **Use Desperation** - When you must succeed

### Managing Risk

1. **Save Desperation for critical moments**
2. **Watch your Desperation rating** - 7+ is dangerous
3. **Avoid Despair** - Lose access to Drive
4. **Accept small failures** - Don't risk Despair on minor tasks
5. **Manage Danger** - High Danger makes everything harder

### Reading the Dice

Herald's visual display helps you quickly understand:

- **All 10s together** - Critical potential
- **Many 6-9** - Solid success
- **Many 1-5** - Likely failure
- **Orange dice** - Desperation (watch for 1s and 10s)

---

## Roll Examples

### Example 1: Simple Success

```
Task: Climb a fence
Pool: Dexterity (3) + Athletics (2) = 5 dice
Difficulty: 1 (simple)
Command: /roll pool:5 difficulty:1 comment:Climbing fence

Result: [8, 7, 6, 4, 2]
Successes: 3 (8, 7, 6)
Outcome: SUCCESS with margin 2

You easily vault the fence.
```

### Example 2: Critical Success

```
Task: Hack a security system
Pool: Intelligence (4) + Technology (4) = 8 dice
Difficulty: 3 (hard)
Command: /roll pool:8 difficulty:3 comment:Hacking security

Result: [10, 10, 9, 8, 7, 5, 3, 2]
Successes: 5 (10, 10, 9, 8, 7)
Criticals: 1 pair = +2 successes
Total: 7 successes
Outcome: CRITICAL SUCCESS with margin 4

You not only breach the system, you gain admin access
and can monitor all cameras without detection.
```

### Example 3: Desperate Success with Overreach

```
Task: Must hit the vampire before it escapes
Pool: Dexterity (3) + Firearms (3) = 6 dice
Desperation: 4
Difficulty: 3 (it's moving fast)
Command: /roll pool:6 desperate:true difficulty:3 comment:Last shot!

Result: [9, 7, 6] + [8, 6, 1, 1] (Desperation)
Regular successes: 3 (9, 7, 6)
Desperation successes: 2 (8, 6)
Desperation 1s: 2
Total: 5 successes
Outcome: SUCCESS with Overreach warning

You hit! But you rolled 2 Desperation 1s.
Choice: Accept success + gain 2 Danger, OR enter Despair
You choose: Accept Overreach, Danger increases from 2 to 4.
```

### Example 4: Messy Critical

```
Task: Break through locked door
Pool: Strength (3) + Athletics (2) = 5 dice
Desperation: 3
Difficulty: 2
Command: /roll pool:5 desperate:true difficulty:2 comment:Breach!

Result: [10, 8, 4] + [10, 7, 3] (Desperation)
Regular successes: 2 (10, 8)
Desperation successes: 2 (10, 7)
Critical pair: Regular 10 + Desperation 10 = +2
Total: 6 successes
Outcome: MESSY CRITICAL

You smash through the door with supernatural strength.
The door doesn't just open - it explodes off its hinges.
Everyone inside sees your eyes glow orange for a moment.
Definitely not human.
```

### Example 5: Automatic Despair

```
Task: Resist vampire's mental control
Pool: Resolve (2) + Composure (2) = 4 dice
Desperation: 5 (already high)
Difficulty: 4 (vampire is powerful)
Command: /roll pool:4 desperate:true difficulty:4 comment:Resist!

Result: [5, 4] + [3, 2, 1, 1, 1] (Desperation)
Regular successes: 0
Desperation successes: 0
Desperation 1s: 3
Total: 0 successes
Outcome: FAILURE + AUTOMATIC DESPAIR

You fail to resist and enter Despair.
Your Drive is lost. You cannot use Desperation.
You must complete your Redemption to recover.
```

---

## Quick Reference

### Success Counting
- **1-5:** No success
- **6-9:** 1 success each
- **10:** 1 success each (can form critical pairs)
- **Pair of 10s:** +2 additional successes

### Difficulty Scale
0 = Automatic | 1 = Simple | 2 = Standard | 3 = Hard
4 = Extreme | 5 = Nearly Impossible | 6 = Legendary

### Desperation Rules
- ✅ Adds your Desperation rating as extra dice
- ⚠️ Rolling 10s + success = Messy Critical
- ⚠️ Rolling 1s + success = Choose Overreach or Despair
- ❌ Rolling 1s + failure = Automatic Despair

### Danger Effects
- Adds to difficulty on all rolls
- 7+ Danger = Extreme threat level

---

## Next Steps

- **[Desperation](desperation.md)** - Master the risk/reward system
- **[Edge](edge.md)** - Learn supernatural advantages
- **[Attributes & Skills](attributes-skills.md)** - Build bigger dice pools
- **[Basic Rolling Guide](../guides/basic-rolling.md)** - See more examples

Or try the [Quick Start Guide](../guides/quickstart.md) to start playing!

---

🔸 **Roll the dice. Count the successes. Face the consequences.**
