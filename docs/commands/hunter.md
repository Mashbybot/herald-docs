# Hunter Commands

Hunter-specific commands manage your character's supernatural abilities, identity, and condition. These commands handle Desperation, Edges, Creeds, Drives, and damage tracking.

---

## Damage & Healing Commands

### `/damage`

Apply damage to Health or Willpower.

**Usage:**
```
/damage track:TRACK amount:X damage_type:TYPE
```

**Parameters:**
- `track` (required): health, willpower
- `amount` (required): Damage amount (1-10)
- `damage_type` (required): superficial, aggravated

**Examples:**
```
/damage track:health amount:3 damage_type:superficial
/damage track:willpower amount:2 damage_type:aggravated
```

**Damage Types:**
- **Superficial (⛛)** - Fills empty track spaces
- **Aggravated (🔻)** - Converts superficial to aggravated, reduces capacity

---

### `/heal`

Heal damage from Health or Willpower.

**Usage:**
```
/heal track:TRACK heal_type:TYPE [amount:X]
```

**Parameters:**
- `track` (required): health, willpower
- `heal_type` (required): all, superficial, aggravated
- `amount` (optional): Required for superficial/aggravated

**Examples:**
```
/heal track:health heal_type:all
/heal track:willpower heal_type:superficial amount:2
/heal track:health heal_type:aggravated amount:1
```

---

## Hunter Identity Commands

### `/desperation`

Manage Desperation rating.

**Usage:**
```
/desperation action:ACTION [amount:X]
```

**Actions:** view, set, add, subtract

**Examples:**
```
/desperation action:view
/desperation action:set amount:5
```

See [H5E Desperation](../h5e/desperation.md) for complete mechanics.

---

### `/creed`

Set your Hunter Creed.

**Usage:**
```
/creed action:ACTION
```

**Actions:**
- `view` - Show current Creed
- `set` - Interactive selection of Creed

**Creeds:**
- Entrepreneurial 🔨 (Building & resources)
- Faithful ✝️ (Direct confrontation)
- Inquisitive 🔍 (Investigation & knowledge)
- Martial ⚔️ (Physical combat)
- Underground 🎭 (Stealth & subterfuge)

See [H5E Creeds](../h5e/creeds.md) for complete details.

---

### `/drive`

Set your Drive and Redemption.

**Usage:**
```
/drive action:ACTION
```

**Actions:**
- `view` - Show current Drive
- `set` - Interactive selection

**Drives:**
- Curiosity 🔍, Vengeance ⚔️, Oath 🤝, Greed 💰, Pride 👑, Envy 💚, Atonement 🕊️

Each Drive has an associated Redemption path for recovering from Despair.

See [H5E Creeds](../h5e/creeds.md) for Drive mechanics.

---

### `/ambition`

Set long-term goal.

**Usage:**
```
/ambition ambition:"Your long-term goal"
```

**Benefit:** Recovers 1 Aggravated Willpower when progress made.

**Examples:**
```
/ambition ambition:"Destroy the vampire court"
/ambition ambition:"Build a Hunter safe house network"
```

---

### `/desire`

Set short-term goal.

**Usage:**
```
/desire desire:"Your short-term goal"
```

**Benefit:** Recovers 1 Superficial Willpower when accomplished.

**Examples:**
```
/desire desire:"Find the vampire haven location"
/desire desire:"Acquire better weapons"
```

---

## Edge & Perks Commands

### `/edge`

Manage Hunter Edges.

**Usage:**
```
/edge action:ACTION
```

**Actions:**
- `view` - Show all your Edges
- `add` - Interactive selection from 17 Edges
- `remove` - Remove an Edge

**Edge Categories:**
- **Assets:** Arsenal, Fleet, Ordnance, Library, Experimental Medicine
- **Aptitudes:** Improvised Gear, Global Access, Drone Jockey, Beast Whisperer, Turncoat
- **Endowments:** Sense the Unnatural, Repel the Unnatural, Thwart the Unnatural, Artifact, Cleanse the Unnatural, Great Destiny, Unnatural Changes

**Examples:**
```
/edge action:view
/edge action:add (shows interactive menu)
/edge action:remove
```

See [H5E Edge](../h5e/edge.md) for complete Edge descriptions.

---

### `/perks`

Manage Edge Perks.

**Usage:**
```
/perks action:ACTION [edge_name:NAME] [perk_name:NAME]
```

**Actions:**
- `view` - Show all Perks (optionally filtered by Edge)
- `add` - Add Perk to Edge (autocomplete shows only your Edges)
- `remove` - Remove Perk

**Autocomplete Features:**
- Shows only Edges you currently have
- Shows only Perks available for selected Edge
- Filters out Perks you already possess

**Examples:**
```
/perks action:view
/perks action:view edge_name:Arsenal
/perks action:add edge_name:Arsenal perk_name:Exotics
/perks action:remove edge_name:Arsenal perk_name:Exotics
```

See [H5E Edge](../h5e/edge.md) for complete Perk lists.

---

## Despair Commands

### `/despair`

Enter Despair state.

**Usage:**
```
/despair
```

**Effects:**
- Cannot use Desperation dice
- Drive becomes unusable
- Must complete Redemption to recover
- Visual indicator on character sheet

**When to Use:**
- After automatic Despair (failed roll + Desperation 1s)
- When choosing Despair over Overreach
- Storyteller-directed Despair

See [H5E Desperation](../h5e/desperation.md) for Despair mechanics.

---

### `/redemption`

Exit Despair state after completing Redemption.

**Usage:**
```
/redemption
```

**Requirements:**
- Must have completed your Redemption path
- Storyteller confirms completion
- Then use this command to restore Drive

**Example:**
```
(Character has Drive: Vengeance)
(Successfully hurts their quarry - completes Redemption)
Storyteller: "That counts as Redemption."
/redemption
(Despair removed, Drive restored)
```

See [H5E Creeds](../h5e/creeds.md) for Redemption paths.

---

## Quick Reference

### Damage & Healing
```
/damage track:health amount:3 damage_type:superficial
/damage track:willpower amount:2 damage_type:aggravated
/heal track:health heal_type:all
/heal track:willpower heal_type:superficial amount:2
```

### Identity
```
/desperation action:view
/creed action:set
/drive action:set
/ambition ambition:"Long-term goal"
/desire desire:"Short-term goal"
```

### Edges & Perks
```
/edge action:view
/edge action:add
/perks action:view edge_name:Arsenal
/perks action:add edge_name:Arsenal perk_name:Exotics
```

### Despair
```
/despair
/redemption (after completing Redemption path)
```

---

## Related Documentation

- **[H5E Desperation](../h5e/desperation.md)** - Complete Desperation mechanics
- **[H5E Creeds](../h5e/creeds.md)** - Creeds, Drives, and Redemption
- **[H5E Edge](../h5e/edge.md)** - All Edges and Perks

Or return to [Command Reference Overview](index.md).

---

🔸 **Manage your Hunter. Track your condition. Face Despair.**
