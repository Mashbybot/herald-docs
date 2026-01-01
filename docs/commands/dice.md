# Dice Commands

Dice commands handle all rolling mechanics in Herald, implementing the full H5E dice pool system with Desperation, Danger, and difficulty tracking.

---

## `/roll`

Roll dice using Hunter: The Reckoning 5E mechanics.

### Usage

```
/roll pool:X [difficulty:Y] [desperate:true/false] [comment:"text"]
```

### Parameters

- **`pool`** (required) - Number of dice to roll (1-100, typically 1-20)
- **`difficulty`** (optional) - Target successes needed (0-6, default: 0)
  - 0 = Automatic
  - 1 = Simple
  - 2 = Standard
  - 3 = Hard
  - 4 = Extreme
  - 5 = Nearly Impossible
  - 6 = Legendary
- **`desperate`** (optional) - Add Desperation dice (true/false, default: false)
- **`comment`** (optional) - Description of the roll

### H5E Dice Mechanics

**Success Counting:**
- 1-5 = Failure
- 6-9 = Success (1 success each)
- 10 = Success (1 success, can form critical pairs)
- **Pair of 10s** = Critical (+2 additional successes)

**Desperation Dice:**
When `desperate:true`:
- Adds your Desperation rating as extra dice (orange colored)
- Visually distinct from regular dice
- Subject to Overreach and Despair consequences

### Examples

**Basic roll:**
```
/roll pool:5 difficulty:2 comment:Pick a lock
```
Rolls 5 dice, need 2+ successes.

**Desperate roll:**
```
/roll pool:6 desperate:true difficulty:3 comment:Must hit the vampire!
```
Rolls 6 regular dice + Desperation dice, need 3+ successes.

**Simple difficulty check:**
```
/roll pool:7 difficulty:1 comment:Spot the ambush
```
Roll 7 dice, only need 1 success.

**No difficulty (check for crits):**
```
/roll pool:8 comment:Damage roll
```
Just count successes, no target difficulty.

### Visual Output

Herald displays rolls with emoji dice:

**Regular Dice:**
- ⭐ Critical 10 (part of pair)
- 🎯 Success (6-9)
- ⚫ Failure (1-5)
- 💥 Botch 1

**Desperation Dice:**
- ✨ Critical 10
- 🟡 Success (6-9)
- 🟠 Failure (2-5)
- 🔥 Botch 1

**Sorted Display:**
```
Regular: ⭐⭐🎯🎯⚫
Desperation: ✨🟡🔥

Successes: 6 (includes +2 from critical pair)
```

### Result Embeds

**Success (Green):**
```
🎯 Success - Breaking down the door
Pool: 6 dice | Difficulty: 2
Result: 4 successes (margin +2)
```

**Critical Success (Gold):**
```
⭐ Critical Success!
Pool: 8 dice | Difficulty: 3
Result: 7 successes (margin +4)
Critical pairs: 1
```

**Failure (Gray):**
```
💔 Failure - Picking the lock
Pool: 5 dice | Difficulty: 3
Result: 1 success (margin -2)
```

**Messy Critical (Orange warning):**
```
⚠️ MESSY CRITICAL
Desperation dice contributed to critical!
Supernatural traces left behind.
Witnesses see something unnatural.
```

**Overreach Warning (Red/Orange):**
```
⚠️ OVERREACH
Rolled 2 ones on Desperation dice!
Choose: Accept success + gain 2 Danger
     OR Enter Despair
```

**Automatic Despair (Dark Red):**
```
💀 AUTOMATIC DESPAIR
Failed roll with Desperation ones!
Drive lost. Must complete Redemption.
```

### Desperation Consequences

**When using `desperate:true`:**

**Messy Critical:**
- If Desperation dice form/contribute to critical pair
- Success, but supernatural power shows
- Complications ensue

**Overreach (Success + Desperation 1s):**
- Choose: Keep success + gain Danger = number of 1s
- Or: Enter Despair (reject success)

**Automatic Despair (Failure + Desperation 1s):**
- Automatically enter Despair
- Drive lost
- Must use `/redemption` after completing Redemption

### Advanced Usage

**With Danger:**
Your Danger rating adds to difficulty:
```
Character Danger: 3
/roll pool:7 difficulty:2

Effective difficulty: 2 + 3 = 5
(Herald doesn't auto-add, adjust manually)
```

**With Specialties:**
Add +2 dice when specialty applies:
```
Firearms 3 + Specialty "Pistols" = 5 dice (when using pistols)
/roll pool:5 difficulty:2 comment:Shooting with my specialty
```

**Contested Rolls:**
Both sides roll separately, compare successes:
```
Hunter: /roll pool:6 difficulty:0 comment:Sneaking
Storyteller rolls guard separately
Higher successes wins
```

### Tips

- **Always add comments** - Helps track what you're rolling
- **Check Desperation** - Use `/desperation action:view` first
- **Calculate pools** - Attribute + Skill + Modifiers
- **Watch for Danger** - High Danger = much harder rolls
- **Save Desperation** - Only use when you must succeed

---

## `/danger`

View or manage your character's Danger rating.

### Usage

```
/danger action:ACTION [amount:X]
```

### Parameters

- **`action`** (required) - view, set, add, subtract, reset
- **`amount`** (optional) - Amount for set/add/subtract actions

### Actions

**View Danger:**
```
/danger action:view
```
Shows current Danger rating and visual bar.

**Set Danger:**
```
/danger action:set amount:5
```
Sets Danger to exact value (0-10).

**Add Danger:**
```
/danger action:add amount:2
```
Increases Danger by amount (from Overreach).

**Subtract Danger:**
```
/danger action:subtract amount:1
```
Decreases Danger by amount (resolving threats).

**Reset Danger:**
```
/danger action:reset
```
Sets Danger to 0 (after resolving major threats).

### What is Danger?

**Danger** (0-10) represents supernatural threats building around you:
- Gained through Overreach (accepting Desperation 1s)
- Adds to difficulty of all rolls
- Represents monsters closing in
- Should be resolved through story

### Danger Effects

**Mechanical:**
- **Adds to difficulty on all rolls**
- Danger 3 + Difficulty 2 = Effective Difficulty 5

**Narrative:**
- Monsters are tracking you
- Supernatural forces converging
- Time running out
- Threats escalating

**High Danger (7+):**
- All tasks extremely difficult
- Major story consequences imminent
- Should be addressed urgently
- Storyteller may force confrontation

### Visual Display

```
Danger: 🟥🟥🟥🟥🟥▪️▪️▪️▪️▪️ 5/10
```
- 🟥 Filled squares (current Danger)
- ▪️ Empty squares (remaining capacity)

### Managing Danger

**Gaining Danger:**
1. Roll with Desperation
2. Get success + Desperation 1s
3. Choose Overreach over Despair
4. Danger increases by number of 1s

**Reducing Danger:**
1. Confront the threat directly
2. Resolve supernatural situation
3. Complete story arc
4. Storyteller discretion

**Typical Reset Points:**
- After defeating major enemy
- Resolving the hunt
- End of story arc
- Escaping to safety

### Examples

**After Overreach:**
```
(Rolled success with 3 Desperation 1s, accepted Overreach)
/danger action:add amount:3
Danger increased from 2 to 5
```

**After Resolving Threat:**
```
(Destroyed the vampire's haven, broke its hold)
/danger action:reset
Danger reduced to 0
```

**Partial Resolution:**
```
(Escaped the area but threat remains)
/danger action:subtract amount:2
Danger decreased from 5 to 3
```

### Strategy

**Low Danger (0-3):**
- Safe to use Desperation
- Minor threats manageable
- Continue hunting normally

**Moderate Danger (4-6):**
- Be cautious with Desperation
- Threats building up
- Consider addressing soon

**High Danger (7-9):**
- Avoid Desperation if possible
- Major threats imminent
- Must resolve soon

**Critical Danger (10):**
- Maximum threat level
- All rolls extremely difficult
- Immediate story confrontation
- Resolution critical

---

## Quick Command Reference

```bash
# Basic roll
/roll pool:X difficulty:Y comment:"description"

# Desperate roll
/roll pool:X desperate:true difficulty:Y

# View Danger
/danger action:view

# Modify Danger
/danger action:set amount:X
/danger action:add amount:X
/danger action:subtract amount:X
/danger action:reset
```

## Common Workflows

**Standard Roll:**
```
1. Calculate pool (Attribute + Skill + Modifiers)
2. Determine difficulty (Storyteller sets)
3. /roll pool:X difficulty:Y comment:"what you're doing"
4. Herald shows results
5. Storyteller narrates outcome
```

**Desperate Roll:**
```
1. Check Desperation: /desperation action:view
2. Decide if risk is worth it
3. /roll pool:X desperate:true difficulty:Y
4. Watch for Overreach/Despair warnings
5. Make choice if needed
6. Update Danger if accepting Overreach
```

**Managing Danger:**
```
1. After Overreach: /danger action:add amount:X
2. Check periodically: /danger action:view
3. Resolve through story (confront threat)
4. After resolution: /danger action:reset or subtract
```

---

## Related Commands

- **[H5E Dice Mechanics](../h5e/dice-mechanics.md)** - Full dice system explanation
- **[H5E Desperation](../h5e/desperation.md)** - Desperation system details
- **[Basic Rolling Guide](../guides/basic-rolling.md)** - Rolling examples and tips

Or return to [Command Reference Overview](index.md).

---

🔸 **Roll the dice. Face the consequences. Hunt the night.**
