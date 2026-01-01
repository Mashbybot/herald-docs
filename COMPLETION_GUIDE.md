# Herald Documentation Completion Guide

**Status:** 12 of 33 pages complete (~36%)
**Last Updated:** 2026-01-01
**Branch:** `claude/complete-docs-website-Unvc9`

This guide provides a comprehensive roadmap for completing the remaining Herald documentation pages.

---

## Table of Contents

1. [Completed Work Summary](#completed-work-summary)
2. [Remaining Pages Overview](#remaining-pages-overview)
3. [Content Structure Guidelines](#content-structure-guidelines)
4. [Phase-by-Phase Completion Plan](#phase-by-phase-completion-plan)
5. [Page Templates](#page-templates)
6. [Writing Style Guide](#writing-style-guide)
7. [Testing Checklist](#testing-checklist)

---

## Completed Work Summary

### ✅ Phase 1: Core H5E Mechanics (7/7 pages - COMPLETE)

**docs/h5e/overview.md** (321 lines)
- Complete H5E introduction
- System overview and key concepts
- Herald's role in the ecosystem
- Quick start guidance

**docs/h5e/attributes-skills.md** (1022 lines)
- All 9 attributes with descriptions
- All 27 skills organized by category
- Dice pool formula and examples
- Herald commands for each

**docs/h5e/dice-mechanics.md** (636 lines)
- D10 pool mechanics
- Success/failure counting
- Critical pairs and botches
- Desperation dice integration

**docs/h5e/edge.md** (720 lines)
- All 17 Edges organized into Assets/Aptitudes/Endowments
- Complete Perk lists for each Edge
- Herald command examples
- Cross-references to related systems

**docs/h5e/desperation.md** (544 lines)
- Desperation/Despair/Danger mechanics
- Overreach choice system
- 5 detailed scenario walkthroughs
- Recovery mechanics

**docs/h5e/creeds.md** (591 lines)
- 5 Creeds with philosophies
- 7 Drives with Redemption paths
- Ambition/Desire mechanics
- Character identity guidance

**docs/h5e/progression.md** (480 lines)
- Complete XP system
- Advancement costs and formulas
- Strategy guides (early/mid/late game)
- Character optimization tips

### ✅ Phase 2: Command Reference (5/5 pages - COMPLETE)

**docs/commands/character.md** (580 lines)
- `/create` with all parameters
- `/character` switching system
- `/sheet` display formats
- `/delete` with confirmations
- `/about` bot information

**docs/commands/dice.md** (407 lines)
- `/roll` with full parameters
- `/danger` management
- Visual dice display documentation
- Desperation integration

**docs/commands/hunter.md** (327 lines)
- `/damage`, `/heal` tracking
- `/desperation`, `/creed`, `/drive`
- `/ambition`, `/desire` identity
- `/edge`, `/perks` with autocomplete
- `/despair`, `/redemption` recovery

**docs/commands/development.md** (180 lines)
- `/attributes`, `/skill_set`, `/specialty`
- `/xp` management (view/add/spend/set)
- `/help` system overview
- XP cost tables

**docs/commands/utility.md** (137 lines)
- `/help` with all 6 topics
- `/about` bot information
- Resource links (docs, Discord, GitHub)

---

## Remaining Pages Overview

### 🔶 Phase 3: Guides (0/5 pages)

**Priority: HIGH** - These are user-facing tutorials critical for onboarding.

1. **docs/guides/getting-started.md** (placeholder)
   - New user onboarding
   - First character creation walkthrough
   - Basic rolling tutorial
   - ~400-500 lines estimated

2. **docs/guides/character-creation.md** (placeholder)
   - Detailed creation guide
   - Attribute/skill selection strategies
   - Creed and Drive selection
   - Starting Edge recommendations
   - ~600-700 lines estimated

3. **docs/guides/playing.md** (placeholder)
   - Session-by-session gameplay
   - Common command workflows
   - Scene mechanics
   - ~400-500 lines estimated

4. **docs/guides/storyteller.md** (placeholder)
   - Running games with Herald
   - XP awards and progression
   - Managing multiple players
   - Campaign tools
   - ~500-600 lines estimated

5. **docs/guides/advanced.md** (placeholder)
   - Advanced tactics
   - Edge synergies
   - Optimization strategies
   - Multi-character management
   - ~400-500 lines estimated

### 🔶 Phase 4: Edge Deep Dives (0/17 pages)

**Priority: MEDIUM** - Enhance understanding of each Edge.

All 17 Edge pages in `docs/h5e/edges/` need expansion from 3-line placeholders to full guides:

**Assets (6 Edges):**
- arsenal.md, contacts.md, fame.md, library.md, safehouse.md, status.md

**Aptitudes (6 Edges):**
- fleet.md, inspire.md, martyr.md, pickpocket.md, scrounger.md, senses.md

**Endowments (5 Edges):**
- artifact.md, benediction.md, global-access.md, sense-danger.md, third-eye.md

**Structure for Each:**
- Edge description and philosophy (~100 lines)
- All Perks with detailed explanations (~200-300 lines)
- Strategy guide and use cases (~100 lines)
- Herald commands and examples (~50 lines)
- Character build ideas (~50 lines)
- **~500-600 lines each, ~8,500-10,000 lines total**

### 🔶 Phase 5: Reference Pages (0/2 pages)

**Priority: MEDIUM** - Quick lookup resources.

1. **docs/reference/glossary.md** (placeholder)
   - H5E terminology
   - Herald-specific terms
   - Discord bot concepts
   - ~300-400 lines estimated

2. **docs/reference/quickstart.md** (placeholder)
   - Command quick reference
   - Common workflows cheatsheet
   - Dice mechanics summary
   - ~200-300 lines estimated

### 🔶 Phase 6: Additional Pages (0/4 pages)

**Priority: LOW** - Nice to have, not critical.

1. **docs/about/index.md** (placeholder)
   - Project history
   - Development team
   - Technology stack
   - ~200-300 lines estimated

2. **docs/about/contributing.md** (placeholder)
   - How to contribute
   - Code standards
   - Documentation standards
   - ~300-400 lines estimated

3. **docs/about/changelog.md** (placeholder)
   - Version history
   - Feature additions
   - Bug fixes
   - ~Variable, ongoing

4. **docs/index.md** (87 lines - needs enhancement)
   - Currently basic landing page
   - Needs feature showcase
   - Visual examples
   - Better navigation
   - ~200-300 lines target

---

## Content Structure Guidelines

### Standard Page Structure

Every documentation page should follow this structure:

```markdown
# Page Title

Brief 1-2 sentence description of the page's purpose.

---

## Main Content Sections

### Section 1
Content with examples...

### Section 2
Content with examples...

---

## Quick Reference

Summary tables or command lists for quick lookup.

---

## Related Documentation

- **[Related Page 1](../path/page.md)** - Description
- **[Related Page 2](../path/page.md)** - Description

---

🔸 **Herald's signature tagline for this page.**
```

### Key Elements

1. **Clear Hierarchy:** H1 for title, H2 for major sections, H3 for subsections
2. **Examples:** Every command or mechanic needs a practical example
3. **Cross-References:** Link to related pages liberally
4. **Quick Reference:** Summary section at the end
5. **Herald's Voice:** Close with 🔸 diamond and tagline

### Command Documentation Format

When documenting commands, use this structure:

```markdown
### `/command`

Brief description of what the command does.

**Usage:**
```
/command param1:VALUE param2:VALUE
```

**Parameters:**
- `param1` (required): Description with valid values
- `param2` (optional): Description with default value

**Examples:**
```
/command param1:Example1
/command param1:Example2 param2:OptionalValue
```

**Notes:**
- Special behavior or edge cases
- Auto-calculations or side effects
- Permissions or restrictions
```

### H5E Mechanics Format

When documenting game mechanics:

```markdown
## Mechanic Name

### Overview
What it is and why it matters.

### How It Works
Step-by-step explanation with examples.

### Herald Integration
How to use Herald commands for this mechanic.

### Strategy Tips
Practical advice for players.

### Related Systems
Links to connected mechanics.
```

---

## Phase-by-Phase Completion Plan

### Phase 3: Guides (NEXT PRIORITY)

**Estimated Time:** 10-15 hours
**Order of Completion:**

1. **getting-started.md** (Start here - critical for new users)
   - Welcome message and overview
   - "Your First Character" walkthrough
   - "Your First Roll" tutorial
   - Common questions
   - Next steps to other guides

2. **character-creation.md** (Deep dive after getting started)
   - Character concept development
   - Attribute allocation strategies
   - Skill selection guide
   - Creed and Drive selection
   - Starting Edge recommendations
   - Specialty planning
   - Example character builds (3-5 archetypes)

3. **playing.md** (Gameplay workflows)
   - Session preparation
   - Common command workflows
   - Combat sequences
   - Investigation sequences
   - Social encounters
   - Between-session management

4. **storyteller.md** (GM guidance)
   - Setting up campaigns
   - Managing player characters
   - XP awards (session/milestone)
   - Difficulty guidelines
   - Campaign pacing
   - Handling Desperation and Despair

5. **advanced.md** (Optimization and tactics)
   - Edge synergies and combos
   - Desperation management strategies
   - Character optimization paths
   - Multi-character builds
   - Power gaming considerations

### Phase 4: Edge Deep Dives (MEDIUM PRIORITY)

**Estimated Time:** 25-35 hours
**Order of Completion:** Group by category for consistency

**Week 1: Assets (6 pages)**
- Arsenal, Contacts, Fame, Library, Safehouse, Status
- Focus on resource management and social Edges

**Week 2: Aptitudes (6 pages)**
- Fleet, Inspire, Martyr, Pickpocket, Scrounger, Senses
- Focus on active ability Edges

**Week 3: Endowments (5 pages)**
- Artifact, Benediction, Global Access, Sense Danger, Third Eye
- Focus on supernatural/mystical Edges

**Template for Each Edge Page:**

```markdown
# Edge Name 🔸

Brief tagline about what this Edge represents.

---

## Overview

### What is [Edge Name]?
Description and flavor text.

### Who Should Take This Edge?
Character types and playstyles.

### Key Strengths
- Bullet list of advantages

### Limitations
- Bullet list of considerations

---

## Perks

### Perk Name 1
**Effect:** Mechanical description
**Usage:** When and how to use
**Strategy:** Tactical considerations

[Repeat for all Perks]

---

## Strategy Guide

### Early Game (Characters 1-10 XP)
Recommendations for new characters.

### Mid Game (Characters 11-50 XP)
How the Edge scales.

### Late Game (Characters 51+ XP)
Advanced applications.

### Edge Synergies
Works well with: [Other Edges]
Conflicts with: [Problematic combinations]

---

## Character Builds

### Build Archetype 1
- Creed: [X]
- Recommended Attributes: [List]
- Recommended Skills: [List]
- Perk Priority: [Order]
- Playstyle: [Description]

[2-3 build examples]

---

## Herald Commands

```
/edge edge:[Edge Name]
/perks edge:[Edge Name] perk:[Perk Name]
```

**Related Commands:**
- Links to command documentation

---

## Quick Reference

[Table of all Perks with one-line descriptions]

---

## Related Documentation

- **[Edge Overview](../edge.md)** - All Edges
- **[Related Creed](../creeds.md#creed-name)** - Thematic connection
- **[Command: Edges](../../commands/hunter.md#edge)** - Managing Edges

---

🔸 **[Thematic tagline for this Edge]**
```

### Phase 5: Reference Pages (MEDIUM PRIORITY)

**Estimated Time:** 4-6 hours

1. **glossary.md**
   - Alphabetical listing
   - H5E terms (Desperation, Despair, Edge, etc.)
   - Herald terms (Active Character, Pool, etc.)
   - Discord concepts (Slash Commands, Autocomplete, etc.)

2. **quickstart.md**
   - One-page command cheatsheet
   - Dice mechanics summary
   - Common workflows
   - Printable/quick reference format

### Phase 6: Additional Pages (LOW PRIORITY)

**Estimated Time:** 6-8 hours

1. **about/index.md** - Project information
2. **about/contributing.md** - Contribution guidelines
3. **about/changelog.md** - Version history (ongoing)
4. **index.md** - Enhanced landing page

---

## Page Templates

### Getting Started Guide Template

```markdown
# Getting Started with Herald

Welcome to Herald, your complete Hunter: The Reckoning 5th Edition companion for Discord.

---

## What is Herald?

Herald is a Discord bot that handles everything you need to play H5E:
- Character creation and management
- Dice rolling with full H5E mechanics
- Edge and Desperation tracking
- Experience and progression

---

## Quick Start: Your First 5 Minutes

### 1. Create Your Character

Let's create a simple Hunter to get started:

```
/create name:YourName
```

This creates a basic character with default attributes (all 1s). You'll improve them in a moment.

### 2. View Your Character

```
/sheet
```

Herald displays your character sheet with all your stats.

### 3. Make Your First Roll

```
/roll pool:5 difficulty:2 comment:My first roll!
```

You rolled 5 dice and needed 2 successes. Welcome to H5E!

---

## Your First Real Character

Now let's build a proper Hunter...

[Continue with detailed walkthrough]

---

## Next Steps

- **[Character Creation Guide](character-creation.md)** - Build your Hunter
- **[Playing Guide](playing.md)** - Learn gameplay workflows
- **[H5E Overview](../h5e/overview.md)** - Understand the mechanics

---

🔸 **Join the Hunt. Your story begins now.**
```

### Edge Deep Dive Template

```markdown
# Edge Name 🔸

One-line thematic description.

---

## Overview

### What is [Edge]?

[2-3 paragraphs describing the Edge's concept, theme, and role in H5E]

### Who Should Take This Edge?

**Ideal For:**
- Character archetype 1
- Character archetype 2
- Playstyle preference

**Consider Carefully If:**
- Situations where this Edge may not shine

---

## All Perks

### Perk 1 Name

**What It Does:**
Mechanical effect description.

**When To Use:**
Tactical applications and scenarios.

**Strategy Notes:**
- Synergies with other abilities
- Common pitfalls
- Optimization tips

**Herald Commands:**
```
/perks edge:[Edge] perk:[Perk Name]
```

[Repeat for each Perk - typically 5-7 per Edge]

---

## Strategy Guide

### Beginner Strategy
How to use this Edge effectively as a new character.

### Advanced Tactics
High-level play and optimization.

### Edge Synergies
- **Works Great With:** [Other Edges/Creeds/Skills]
- **Conflicts With:** [Problematic combinations]
- **Neutral:** [No special interaction]

---

## Character Builds

### Build 1: [Archetype Name]

**Concept:** Brief description

**Creed:** [Creed Name]
**Drive:** [Drive Name]

**Recommended Starting Stats:**
- Attributes: Str 2, Dex 3, Sta 2, Cha 2, Man 1, Com 3, Int 3, Wit 2, Res 2
- Key Skills: [Skill 3, Skill 2, Skill 2]
- Specialties: [Skill (Specialty)]

**Perk Priority:**
1. First Perk (Why: Immediate value)
2. Second Perk (Why: Synergy)
3. Third Perk (Why: Scaling)

**Playstyle:**
[Description of how this build plays]

[Include 2-3 builds per Edge]

---

## Herald Integration

### Adding This Edge
```
/edge edge:[Edge Name]
```

### Adding Perks
```
/perks edge:[Edge Name] perk:[Perk Name]
```

### Viewing Your Perks
```
/sheet
```
Your Perks are displayed in the character sheet under the Edges section.

---

## Quick Reference

| Perk Name | Effect Summary |
|-----------|----------------|
| Perk 1    | One-line description |
| Perk 2    | One-line description |
| Perk 3    | One-line description |

---

## Related Documentation

- **[Edge System Overview](../edge.md)** - All Edges explained
- **[Perks Command](../../commands/hunter.md#perks)** - Managing Perks
- **[Recommended Creed](../creeds.md#creed-name)** - Thematic fit
- **[Progression Guide](../progression.md)** - When to buy Perks

---

🔸 **[Thematic tagline for this specific Edge]**
```

---

## Writing Style Guide

### Herald's Voice

Herald documentation uses a specific voice:

**Characteristics:**
- **Analytical:** Clear, precise, factual
- **Present-tense:** "Herald tracks your character" not "Herald will track"
- **Active voice:** "You roll dice" not "Dice are rolled"
- **Confident:** Authoritative without being condescending
- **Helpful:** Anticipates questions and provides examples

**Example Comparison:**

❌ **Bad:** "So, like, if you want to roll some dice, you could maybe try using the /roll command, which might help you roll dice for your character if you want."

✅ **Good:** "Use `/roll pool:5 difficulty:2` to roll 5 dice against difficulty 2. Herald counts your successes and displays the result."

### Branding Elements

**🔸 Diamond Symbol**
- Use at the end of every page
- Represents Herald's identity
- Always orange when rendered

**Taglines**
- One sentence, active voice
- Thematic to the page content
- Examples:
  - "Hunt the darkness. Track every detail."
  - "Roll the dice. Face your Desperation."
  - "Build your Hunter. Choose your path."

### Formatting Standards

**Code Blocks:**
- Use triple backticks for multi-line commands
- Use inline `code` for parameters and values
- Always show complete command syntax

**Lists:**
- Use bullets for unordered information
- Use numbers for sequential steps
- Use tables for comparison data

**Emphasis:**
- **Bold** for important terms on first use
- *Italic* for emphasis (sparingly)
- `Code formatting` for commands, parameters, values

**Links:**
- Use descriptive link text: `[Progression Guide](../h5e/progression.md)`
- Not: `Click [here](../h5e/progression.md)`
- Include brief description after link when in lists

### Technical Accuracy

**Always Verify:**
- Command syntax matches actual implementation
- Parameter values are accurate (e.g., 1-5 for attributes)
- XP costs match the system (Attributes: new × 4, Skills: new × 2, Specialties: 3)
- Cross-references point to correct pages
- Examples use valid values

**Common Pitfalls:**
- Don't assume features exist - verify with Herald system docs
- Don't invent commands or parameters
- Don't contradict H5E core rules
- Don't provide outdated information

---

## Testing Checklist

### Before Marking a Page Complete

- [ ] All headings use proper hierarchy (H1 → H2 → H3)
- [ ] Every command example uses valid syntax
- [ ] All cross-reference links work
- [ ] Page includes Quick Reference section
- [ ] Page ends with 🔸 and tagline
- [ ] No placeholder text remains (e.g., "TODO", "[TBD]")
- [ ] Code blocks use proper markdown syntax
- [ ] Tables render correctly
- [ ] Images (if any) have alt text
- [ ] Content matches Herald's voice and style

### Page Length Guidelines

- **Guide pages:** 400-700 lines
- **Edge pages:** 500-600 lines
- **Reference pages:** 200-400 lines
- **Command pages:** 300-600 lines

### Git Workflow

**Committing Work:**

1. Group related pages in commits:
   ```bash
   git add docs/guides/getting-started.md docs/guides/character-creation.md
   git commit -m "Complete Getting Started and Character Creation guides"
   ```

2. Use descriptive commit messages:
   - ✅ "Complete Assets Edge documentation (6 pages)"
   - ❌ "Update docs"

3. Push regularly:
   ```bash
   git push -u origin claude/complete-docs-website-Unvc9
   ```

**Commit Message Format:**
```
Brief summary (50 chars or less)

- Bullet point detail 1
- Bullet point detail 2
- Bullet point detail 3

Addresses [Phase] completion goal.
```

---

## Estimated Timeline

### Full Completion Schedule

| Phase | Pages | Est. Hours | Priority |
|-------|-------|------------|----------|
| Phase 3: Guides | 5 | 10-15 | HIGH |
| Phase 4: Edge Deep Dives | 17 | 25-35 | MEDIUM |
| Phase 5: Reference | 2 | 4-6 | MEDIUM |
| Phase 6: Additional | 4 | 6-8 | LOW |
| **Total** | **28** | **45-64** | - |

### Realistic Schedule Options

**Aggressive (2-3 weeks):**
- 3-4 hours per day
- Complete 2-3 pages per session
- Focus on high-priority first

**Moderate (4-6 weeks):**
- 1-2 hours per day
- Complete 1-2 pages per session
- Balanced approach

**Relaxed (8-10 weeks):**
- 30-60 minutes per day
- Complete 1 page per session
- Sustainable pace

---

## Success Criteria

### Phase 3 Complete When:
- [ ] All 5 guide pages written (400-700 lines each)
- [ ] New users can onboard without external help
- [ ] Character creation is fully documented
- [ ] Storytellers have campaign management guide
- [ ] Advanced tactics documented

### Phase 4 Complete When:
- [ ] All 17 Edge pages expanded (500-600 lines each)
- [ ] Every Perk has detailed explanation
- [ ] Each Edge has 2-3 character build examples
- [ ] Strategy guides cover early/mid/late game
- [ ] Cross-references to related Creeds/Drives

### Phase 5 Complete When:
- [ ] Glossary includes all H5E and Herald terms
- [ ] Quickstart page serves as printable reference
- [ ] Both pages are genuinely useful for quick lookup

### Phase 6 Complete When:
- [ ] About pages explain project history and contributing
- [ ] Changelog tracks all versions
- [ ] Landing page (index.md) is compelling and clear

### 100% Documentation Complete When:
- [ ] All 33 pages have substantial content (no placeholders)
- [ ] All cross-references work
- [ ] All commands documented
- [ ] All H5E mechanics explained
- [ ] All Edges have deep dives
- [ ] Testing checklist passes for every page
- [ ] MkDocs builds without errors
- [ ] Documentation website is fully navigable

---

## Resources

### Reference Materials

**Herald System Documentation:**
- Located in root directory (provided by user)
- Contains all command implementations
- Source of truth for mechanics

**H5E Core Rules:**
- Hunter: The Reckoning 5th Edition rulebook
- Official Renegade Game Studios materials

**Existing Pages:**
- Use completed pages as templates
- Maintain consistency in structure and style
- Reference cross-linking patterns

### Tools

**MkDocs Material:**
- Documentation framework
- Orange/Hunter theme
- Material components

**Git:**
- Version control
- Branch: `claude/complete-docs-website-Unvc9`
- Regular commits and pushes

---

## Contact and Support

### Questions or Issues?

- Reference the Herald system documentation
- Check existing completed pages for patterns
- Verify command syntax against implementation
- Maintain consistency with established style

### Updates to This Guide

This completion guide is a living document. Update it when:
- Completing major phases
- Discovering new patterns or best practices
- Adjusting timeline estimates
- Adding new pages to the scope

---

🔸 **Complete the documentation. Empower every Hunter. Build the knowledge.**

---

**End of Completion Guide**
*Last Updated: 2026-01-01*
*Version: 1.0*
