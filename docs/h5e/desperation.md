# Desperation

Desperation is the supernatural power that flows through Hunters - and the curse that threatens to consume them. It's the central risk/reward mechanic of Hunter: The Reckoning 5E.

---

## What is Desperation?

**Desperation** represents your character's connection to the supernatural. The more desperate you become, the more power you can access - but the greater the risk of losing yourself.

### The Desperation Rating

Your Desperation is rated from **0 to 10**:

- **0-3** - Low Desperation (safe zone)
- **4-6** - Moderate Desperation (increasing risk)
- **7-9** - High Desperation (dangerous territory)
- **10** - Maximum Desperation (critical)

---

## Using Desperation

### Rolling with Desperation

When you need extra power, you can add Desperation dice to your roll:

```
/roll pool:5 desperate:true difficulty:3 comment:Must succeed!
```

**What Happens:**
1. Add your **Desperation rating** as extra dice
2. These dice are visually distinct (orange/gold)
3. They count toward successes normally
4. But they come with serious risks

**Example:**
```
Regular pool: 5 dice
Desperation rating: 4
Total dice when desperate: 9 dice

This can turn a likely failure into a success...
or trigger Overreach or Despair.
```

### When to Use Desperation

Use Desperation when:

- ✅ The situation is critical
- ✅ Failure means death
- ✅ You need that extra edge
- ✅ The risk is worth the reward

Don't use Desperation when:

- ❌ It's a minor task
- ❌ Failure is acceptable
- ❌ You're already at high Desperation
- ❌ You're in Despair

---

## Desperation Consequences

### Messy Criticals

When **Desperation dice contribute to a critical** (pair of 10s):

!!! warning "Messy Critical Effects"
    - You succeed spectacularly
    - But your supernatural power shows
    - Witnesses see something unnatural
    - You leave supernatural traces
    - Complications arise

**Example:**
```
Regular dice: [10, 8, 6]
Desperation dice: [10, 7, 3]

Critical pair: Regular 10 + Desperation 10
Result: MESSY CRITICAL

You smash through the door with impossible strength.
It doesn't just open - it explodes off its hinges.
Everyone in the room sees your eyes glow orange.
You're definitely not human anymore.
```

### Overreach

Rolling **1s on Desperation dice** while **succeeding** forces a choice:

**Choice 1: Accept Overreach**

- Keep your success
- Gain **Danger** equal to Desperation 1s rolled
- Supernatural threat increases around you

**Choice 2: Enter Despair**

- Reject the success (becomes a failure)
- Your Drive becomes unusable
- Cannot use Desperation until Redeemed

**Example:**
```
Roll with Desperation: [8, 7, 6] + [9, 1, 1]
Regular successes: 3
Desperation successes: 1 (the 9)
Desperation 1s: 2
Total: 4 successes (success!)

But you rolled 2 Desperation 1s...

Option A: Accept success, gain 2 Danger (from 3 to 5)
Option B: Enter Despair, turn success into failure
```

### Automatic Despair

Rolling **1s on Desperation dice** while **failing** = **Automatic Despair**

No choice. You enter Despair immediately.

- The roll fails
- Your Drive is lost
- Cannot use Desperation
- Must complete Redemption to recover

**Example:**
```
Roll with Desperation: [5, 4, 3] + [2, 1, 1, 1]
Regular successes: 0
Desperation successes: 0
Desperation 1s: 3
Result: FAILURE + AUTOMATIC DESPAIR

You fail completely and enter Despair.
Your Drive is gone. You must seek Redemption.
```

---

## Despair State

### What is Despair?

**Despair** is the breaking point where you lose sight of why you hunt. Your Drive fails, and you cannot access your supernatural power.

### Effects of Despair

When in Despair:

- ❌ **Cannot use Desperation dice**
- ❌ **Drive is unusable** (no recovery from pursuing it)
- ❌ **Drive-related abilities don't function**
- 💀 **Visual indicator on character sheet**
- ⚠️ **Must complete Redemption to recover**

### Entering Despair

You enter Despair when:

1. Rolling Desperation 1s on a failed roll (automatic)
2. Choosing Despair over Overreach (voluntary)
3. Storyteller decision (rare, narrative reasons)

**Herald Command:**
```
/despair
```

### Exiting Despair: Redemption

To recover from Despair, you must complete your **Redemption**:

- Curiosity → Uncover new information about quarry
- Vengeance → Hurt your quarry
- Oath → Actively uphold or fulfill oath
- Greed → Acquire resources from enemies
- Pride → Best your quarry in contest
- Envy → Ally with your quarry
- Atonement → Protect someone from quarry

See [Creeds](creeds.md) for Drive and Redemption details.

**Herald Command (after completing Redemption):**
```
/redemption
```

This removes Despair status and restores your Drive.

---

## Managing Your Desperation

### Viewing Desperation

```
/desperation action:view
```

Shows your current Desperation rating and status.

Also displayed on character sheet:
```
🟨🟨🟨🟨▪️▪️▪️▪️▪️▪️ 4/10
(4 Desperation, 6 empty)
```

### Modifying Desperation

**Set Desperation:**
```
/desperation action:set amount:5
```

**Add Desperation:**
```
/desperation action:add amount:2
```

**Subtract Desperation:**
```
/desperation action:subtract amount:1
```

!!! herald "Storyteller Tool"
    These commands are primarily for Storytellers to adjust Desperation based on story events. Desperation typically changes through:

    - Using Desperation dice repeatedly
    - Story-driven increases (exposure to supernatural)
    - Recovery (downtime, therapy, rituals)

---

## Danger System

**Danger** is separate from but related to Desperation. It represents supernatural threats building up around you.

### What is Danger?

- Range: **0 to 10**
- Represents ongoing supernatural threats
- **Adds to difficulty** of all rolls
- Gained through Overreach
- Removed through story resolution

### Danger Effects

```
Character Danger: 3
Base difficulty: 2
Effective difficulty: 2 + 3 = 5
```

**High Danger (7+):**

- All tasks become extremely difficult
- Supernatural forces closing in
- Major story consequences
- Should be resolved narratively

### Managing Danger

**View Danger:**
```
/danger action:view
```

**Set Danger:**
```
/danger action:set amount:4
```

**Add Danger:**
```
/danger action:add amount:2
```

**Subtract Danger:**
```
/danger action:subtract amount:1
```

**Reset Danger:**
```
/danger action:reset
```

Danger typically resets after:

- Confronting the threat
- Resolving the supernatural situation
- Completing a story arc
- Storyteller discretion

---

## Strategic Desperation Use

### When to Risk It

**Good Times to Use Desperation:**

1. **Life or death** - Character or ally will die otherwise
2. **Critical mission** - Failure dooms the hunt
3. **Low Desperation** - You're at 0-3, risk is minimal
4. **Have Redemption ready** - Can recover from Despair quickly
5. **Storyteller approves** - Cool narrative moment

**Bad Times to Use Desperation:**

1. **High Desperation** - Already at 7+, one bad roll = Despair
2. **Minor task** - Not worth the risk
3. **Already in Despair** - Cannot use Desperation
4. **No way to Redeem** - Stuck in Despair with no path out
5. **High Danger** - The difficulty is already extreme

### Managing Risk

#### Low Risk Strategy (Conservative)
- Never use Desperation above 5
- Only use for critical rolls
- Focus on building dice pools naturally
- Avoid Despair at all costs

#### Moderate Risk Strategy (Balanced)
- Use Desperation up to 7
- Risk Overreach, accept Danger
- Have Redemption path ready
- Balance power and caution

#### High Risk Strategy (Aggressive)
- Use Desperation freely
- Accept Despair as part of hunting
- Always have Redemption available
- Live fast, burn bright

---

## Desperation Scenarios

### Scenario 1: The Safe Desperation Roll

```
Desperation: 2 (low)
Pool: 5 dice
Desperate roll: 7 total dice

Roll: [9, 8, 7, 6, 4] + [8, 5]
Result: 5 successes, no Desperation 1s
Outcome: Clean success with extra power, no consequences
```

**Analysis:** Low Desperation means few Desperation dice, reducing chance of rolling 1s.

### Scenario 2: The Messy Critical

```
Desperation: 5 (moderate)
Pool: 4 dice
Desperate roll: 9 total dice

Roll: [10, 7, 6, 4] + [10, 9, 7, 3, 2]
Result: 5 regular successes + 1 Desperation critical = 7 successes
Messy Critical: Desperation die (10) formed the critical pair
Outcome: Spectacular success with supernatural side effects
```

**Analysis:** Success is huge, but everyone knows you're not human anymore.

### Scenario 3: Overreach Choice

```
Desperation: 6 (moderate-high)
Pool: 5 dice
Desperate roll: 11 total dice
Current Danger: 2

Roll: [8, 7, 6, 5, 4] + [9, 6, 5, 3, 1, 1]
Result: 5 successes (success!), but 2 Desperation 1s

Choice:
A) Accept Overreach: Success + Danger increases from 2 to 4
B) Enter Despair: Failure + lose Drive

Decision: Accept Overreach
New Danger: 4
```

**Analysis:** Danger is manageable, worth accepting to keep success.

### Scenario 4: Automatic Despair

```
Desperation: 8 (high - risky)
Pool: 3 dice
Desperate roll: 11 total dice

Roll: [5, 4, 2] + [5, 4, 3, 2, 1, 1, 1, 1]
Result: 0 successes, 4 Desperation 1s
Outcome: AUTOMATIC DESPAIR

Effects:
- Roll fails completely
- Enter Despair immediately
- Drive lost
- Must complete Redemption
```

**Analysis:** This is why you don't use Desperation at high ratings.

### Scenario 5: Recovery from Despair

```
Current state: In Despair
Drive: Vengeance (hurt your quarry)
Redemption: Hurt your quarry

Story: Successfully ambush and wound the vampire that killed your partner

Storyteller: "That definitely counts as hurting your quarry.
             You've completed your Redemption."

Command: /redemption

Result: Despair removed, Drive restored, can use Desperation again
```

**Analysis:** Redemption provides narrative and mechanical recovery.

---

## Desperation & Story

### Narrative Meaning

Desperation isn't just a mechanic - it represents:

- **Psychological state** - How close to breaking you are
- **Supernatural corruption** - How much the power has changed you
- **Thematic tension** - The cost of fighting monsters
- **Character arc** - Your journey into darkness or redemption

### Desperation Progression

**Early Chronicle (Desperation 0-3):**
- You're a normal person who hunts
- Desperation is a emergency tool
- You can still have a normal life

**Mid Chronicle (Desperation 4-7):**
- Hunting is consuming you
- You use Desperation regularly
- Normal life is slipping away
- Risk of Despair is real

**Late Chronicle (Desperation 8-10):**
- You're more monster than human
- Every roll risks Despair
- Redemption is your only anchor
- One bad roll from breaking

### Roleplaying Desperation

**Low Desperation (0-3):**
- Mostly normal behavior
- Occasional supernatural insight
- Can pass for human

**Moderate Desperation (4-6):**
- Frequently withdrawn or intense
- Eyes sometimes glow faintly
- People sense something "off"

**High Desperation (7-9):**
- Obsessive hunting behavior
- Visible supernatural changes
- Alienated from normal society

**Maximum Desperation (10):**
- Barely holding on
- Obviously inhuman
- One step from Despair

---

## Quick Reference

### Desperation Rating Scale
- **0-3:** Safe zone
- **4-6:** Moderate risk
- **7-9:** High risk
- **10:** Critical

### Desperation Consequences
- **Desperation 10s in critical:** Messy Critical (success with complications)
- **Desperation 1s + success:** Choose Overreach or Despair
- **Desperation 1s + failure:** Automatic Despair

### Despair Effects
- ❌ Cannot use Desperation
- ❌ Drive unusable
- ⚠️ Must complete Redemption to recover

### Herald Commands

```
/desperation action:view              # Check current rating
/desperation action:set amount:X      # Set Desperation
/desperation action:add amount:X      # Increase Desperation
/desperation action:subtract amount:X # Decrease Desperation

/despair                              # Enter Despair
/redemption                           # Exit Despair (after completing Redemption)

/danger action:view                   # Check Danger
/danger action:set amount:X           # Set Danger
/danger action:add amount:X           # Add Danger
/danger action:subtract amount:X      # Remove Danger
/danger action:reset                  # Reset Danger to 0
```

---

## Next Steps

- **[Dice Mechanics](dice-mechanics.md)** - See how Desperation dice work in detail
- **[Creeds](creeds.md)** - Learn about Drives and Redemption paths
- **[Edge](edge.md)** - Explore other supernatural advantages
- **[Basic Rolling Guide](../guides/basic-rolling.md)** - Practice rolling with Desperation

Or return to the [H5E Overview](overview.md)!

---

🔸 **Power comes at a price. Choose your Desperation wisely.**
