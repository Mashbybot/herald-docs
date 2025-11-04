# 🔸 Herald the Reckoning

**Discord bot for Hunter: The Reckoning 5th Edition**

*Built by Hunters, for Hunters.*

---

!!! herald "System Status"
    🔸 Protocol established. Hunter: The Reckoning 5th Edition systems active.  
    Dice mechanics integrated. Character archives operational. Hunt coordination ready.

Herald tracks patterns. Manages operations. Aids the hunt.

I am a comprehensive Discord bot designed specifically for Hunter: The Reckoning 5th Edition. Character management, dice mechanics (Edge, Desperation, messy criticals), progression tracking, damage protocols. The Reckoning doesn't wait for official tools. When Hunters need resources, Hunters build them.

---

## Core Systems

### 🔸 Character Protocol
Herald maintains complete Hunter profiles. All attributes tracked. All progressions monitored. The system validates. You hunt.

- Create and manage multiple Hunter characters per user
- Full attribute and skill tracking with automatic validation
- Derived stats calculated (Health, Willpower, Defense)
- Character sheet display with H5E formatting
- Specialties, edges, and perks integrated
- Import/export functionality for chronicle portability

### 🔸 H5E Dice Integration
Edge. Desperation. Messy criticals. Rouses. Complete mechanical fidelity. The Reckoning's rules encoded. Your stories unfold naturally.

- Character-integrated rolls using stored attributes and skills
- Edge system (reroll all 10s once per session)
- Desperation mechanics (escalating consequences)
- Messy critical detection (10s + 1s = complications)
- Difficulty and Danger ratings
- Clean, readable roll results with success calculation

### 🔸 Progression Archives
Sessions logged. Advancement tracked. Chronicles preserved. Herald observes. Herald remembers.

- Experience point (XP) tracking with transaction logs
- Attribute and skill advancement per H5E rules
- Edge and perk acquisition protocols
- Session-based progression tracking
- Character development history maintained
- Creed-based evolution documented

### 🔸 Hunt Coordination
Cell operations. Shared tracking. Unified protocols. The Reckoning requires coordination.

- Multi-character cell management
- Organizational chart tracking (Hunters, cells, compacts)
- Session logging with participant tracking
- Equipment and gear management
- Character notes and journals
- Damage tracking (Health, Willpower, Aggravated)

---

## Ready to Begin?

New to Herald? Protocol initialization sequence:

1. **[Add Herald to Your Server](guides/adding-herald.md)** - Installation protocol
2. **[Create Your First Character](guides/first-character.md)** - Hunter registration
3. **[Roll Some Dice](guides/basic-rolling.md)** - Dice system familiarization
4. **[Explore All Features](guides/character-management.md)** - Complete capability assessment

---

## Documentation Archive

<div class="grid cards" markdown>

-   :material-book-open-page-variant:{ .lg .middle } __Getting Started__

    ---

    New Hunter detected. Initialize with quick setup protocols and foundational tutorials.

    [:octicons-arrow-right-24: Begin Protocol](guides/quickstart.md)

-   :material-dice-multiple:{ .lg .middle } __Operational Guides__

    ---

    Comprehensive analysis covering character creation, dice mechanics, and H5E system integration.

    [:octicons-arrow-right-24: Access Guides](guides/character-creation.md)

-   :material-console:{ .lg .middle } __Command Reference__

    ---

    Complete command inventory with usage examples and parameter specifications.

    [:octicons-arrow-right-24: Query Commands](commands/index.md)

-   :material-account-group:{ .lg .middle } __H5E Integration__

    ---

    Analysis of Herald's implementation of Hunter: The Reckoning 5E mechanics and systems.

    [:octicons-arrow-right-24: Examine H5E](h5e/overview.md)

</div>

---

## 🎯 Example: Quick Roll

**Manual roll** (without character):
```
/roll attribute:3 skill:2 difficulty:2
```

**Character-based roll** (using stored stats):
```
/roll_char character:Raven attribute:Dexterity skill:Firearms difficulty:3
```

**With Edge** (reroll 10s):
```
/roll_char character:Raven attribute:Strength skill:Brawl edge:true
```

**Desperation roll** (escalating consequences):
```
/roll_char character:Raven attribute:Resolve skill:Survival desperation:2
```

Herald calculates successes. Herald tracks patterns. Herald validates results.

---

## 💬 Support & Community

**Need assistance? Query recognized.**

- 💬 [Discord Support Server](https://discord.gg/9bEZk6ARG9) - Real-time support protocols
- 🐛 [Report Issues](https://github.com/Mashbybot/herald/issues) - Bug documentation
- 📖 [Full Documentation](https://mashbybot.github.io/herald-docs/) - Complete system reference
- ⭐ [Star on GitHub](https://github.com/Mashbybot/herald) - Community tracking

---

## 📖 About Hunter: The Reckoning 5E

Hunter: The Reckoning 5th Edition is the latest iteration of the classic World of Darkness game about ordinary people who have glimpsed the supernatural truth and taken up arms against the darkness. The Reckoning calls. Hunters answer.

**Key H5E mechanics Herald implements:**
- **Edge** - Supernatural awareness granting reroll capabilities
- **Desperation** - Growing recklessness with escalating consequences  
- **Conviction** - Moral compass tracking Hunter's code
- **Creeds** - Philosophical approaches to the Hunt
- **Dangers** - Environmental and supernatural complications

Herald was built by active H5E players running their own chronicles. The Reckoning doesn't wait for corporate timelines. When official tools are absent, Hunters build their own.

---

## The Philosophy

**Pattern observed:** When tools are absent, Hunters build them.

Herald exists as proof. Community-driven. Open source. Free forever. Built by Hunters who couldn't wait. We needed character tracking. We needed H5E-specific dice mechanics. We needed something that understood Edge, Desperation, and the weight of Conviction.

So we built it. And we hunt with you.

**Core principles:**
- ✅ **Mechanical accuracy** - Edge, Desperation, and messy crits work correctly
- ✅ **Zero setup** - Add bot, create character, start hunting
- ✅ **Privacy-focused** - Local database, no external data collection
- ✅ **Open source** - Community-driven development
- ✅ **Free forever** - No premium tiers, no paywalls, no subscriptions

---

## Feature Matrix

| System | Status |
|--------|--------|
| Character Creation | 🔸 Active |
| Attribute & Skill Management | 🔸 Active |
| Edge Mechanics | 🔸 Active |
| Desperation System | 🔸 Active |
| Conviction Tracking | 🔸 Active |
| Damage & Health | 🔸 Active |
| XP & Progression | 🔸 Active |
| Multiple Characters | 🔸 Active |
| Character Import/Export | 🔸 Active |
| Session Logging | 🔸 Active |
| Cell Operations | 🔸 Active |
| Messy Critical Detection | 🔸 Active |
| Specialties | 🔸 Active |
| Edges & Perks | 🔸 Active |
| Rouse Checks | 🔸 Active |

---

## Technical Specifications

**Architecture:**
- **Language:** Python 3.11+
- **Framework:** discord.py 2.x (slash commands)
- **Database:** SQLite (local, file-based)
- **Structure:** Modular cogs system
- **Deployment:** Self-hosted or cloud

**Design principles:**
- Beginner-friendly architecture for learning
- Modular expansion for gradual feature addition
- Comprehensive error handling and validation
- Performance-optimized database queries
- Professional-grade logging and monitoring

---

🔸 **What are we Hunting?**

---

*Herald the Reckoning. System active. Protocol established. Ready to hunt.*

---

<div class="grid cards" markdown>

-   **[→ Add Herald to Your Server](guides/adding-herald.md)**
    
    Installation takes under 5 minutes. No configuration required. Just add and hunt.

-   **[→ Create Your First Character](guides/first-character.md)**
    
    Character creation protocol. Default templates available. Customization supported.

-   **[→ Join the Community](https://discord.gg/9bEZk6ARG9)**
    
    Support server active. Community engaged. Questions answered. Hunters collaborate.

-   **[→ View Source Code](https://github.com/Mashbybot/herald)**
    
    Open source. MIT licensed. Community contributions welcome. Fork freely.

</div>
