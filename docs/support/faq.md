# Frequently Asked Questions

Common questions about Herald and how to use it.

---

## General Questions

### What is Herald?

Herald is a Discord bot specifically designed for Hunter: The Reckoning 5th Edition. It handles character management, dice rolling with H5E mechanics, Edge and Desperation tracking, and character progression.

### Is Herald free?

Yes! Herald is completely free to use. There are no premium tiers or paid features.

### How do I add Herald to my server?

See the [Adding Herald guide](../guides/adding-herald.md) for step-by-step instructions.

### What permissions does Herald need?

Herald needs:
- **Send Messages** (required)
- **Embed Links** (required)
- **Use External Emoji** (recommended for dice displays)

### Can I use Herald for other World of Darkness games?

Herald is built specifically for Hunter: The Reckoning 5E. While some features might work for other games, it's optimized for H5E mechanics (Edge, Desperation, etc.).

---

## Character Management

### How many characters can I have?

There's no hard limit! You can create as many characters as you need across different servers.

### Are my characters private?

Character data is stored per-server. Your character "Raven" on Server A is separate from "Raven" on Server B.

### Can I transfer characters between servers?

Not currently. Each server maintains its own character database.

### I deleted my character by accident! Can I get it back?

Unfortunately, character deletion is permanent and cannot be undone. Always use the confirmation button carefully!

### Can I rename my character?

Yes! Use `/rename old_name:Raven new_name:Corvus` to rename a character.

---

## Dice Rolling

### Why are my dice showing as text instead of emojis?

Herald uses custom emojis for dice. If you see text, either:
1. Herald doesn't have the **Use External Emoji** permission
2. Your Discord settings have website previews disabled

Herald automatically falls back to text mode if emojis aren't available.

### What do the different dice symbols mean?

- 🎲 with red numbers = Desperation dice
- 🎲 with gray numbers = Regular dice
- **10** = Critical (2 successes)
- **6-9** = Success (1 success)
- **1-5** = Failure

### What's a "Messy Critical"?

A messy critical happens when **Desperation dice** roll 10s. You get the successes, but something goes wrong. Your Storyteller will describe the complication.

### How does difficulty work?

Difficulty is the **number of successes** you need. It's not the target number for dice - Herald uses the H5E system where 6+ is always a success.

### Can I roll without a character?

Yes! Use `/roll attribute:3 skill:2` to roll manually without character stats.

---

## Edge & Desperation

### What is Edge?

Edge represents a Hunter's supernatural insight and power. It adds dice to your rolls and has special properties in H5E.

### When should I use Desperation dice?

Desperation dice are typically used when:
- You're in grave danger
- You're desperate to succeed
- Your Storyteller calls for it
- You have a Desperation rating

### Do Desperation dice replace regular dice?

No! Desperation dice are **added** to your pool. They're shown separately because they can cause messy criticals.

### How do I track Desperation changes?

Use `/desperation character:Raven desperation:3` to update your Desperation rating.

---

## Skills & Experience

### How do skill templates work?

Skill templates apply H5E-standard skill distributions:
- **Balanced** - Well-rounded (7/5/3/1)
- **Specialist** - Focused expert (9/5/1/0)
- **Jack-of-all-trades** - Broad competence (5/5/5/0)

### Can I mix templates and manual skills?

Yes! Apply a template for a quick start, then use `/skill_set` to customize specific skills.

### How does XP spending work?

Use `/spend_xp` to improve attributes or skills. Herald automatically:
- Deducts the XP cost
- Updates the trait
- Recalculates derived stats
- Logs the transaction

### What are specialties?

Specialties are areas of expertise within skills. When your specialty applies, you get +1 die to rolls.

Example: `Firearms (Pistols)` gives +1 die when using pistols.

---

## Commands

### Why aren't slash commands showing up?

If commands aren't appearing:
1. Wait a few minutes - Discord can be slow to sync
2. Check Herald has **Use Application Commands** permission
3. Ensure the `@everyone` role can use slash commands
4. Try restarting Discord
5. Type the command anyway - it might work!

### Can I use text commands instead of slash commands?

No, Herald only uses Discord's slash command system. This provides better autocomplete and clearer parameter names.

### Do I need to type full character names?

No! Herald supports autocomplete. Start typing and it will suggest your characters.

---

## Troubleshooting

### Herald isn't responding to commands

Check:
1. Herald is online (green status)
2. Herald has permissions in the channel
3. You're using slash commands (start with `/`)
4. Commands are synced (may take a few minutes after adding Herald)

### I'm getting "Character not found" errors

Make sure:
1. Character name is spelled correctly (case doesn't matter)
2. Character was created on **this server**
3. You own the character (you created it)

Use `/characters` to list all your characters on the server.

### Dice rolls look wrong

Herald follows H5E rules exactly:
- 6-9 = 1 success
- 10 = 2 successes (critical)
- 1-5 = no success

If you think there's a bug, report it in our [Support Server](https://discord.gg/9bEZk6ARG9).

### My character sheet is cut off

Discord has limits on embed size. If your character has extensive equipment or notes, consider shortening them or splitting across multiple fields.

---

## Server Administration

### Can I restrict who can use Herald?

Yes! Use Discord's slash command permissions in **Server Settings** → **Integrations** → **Herald** to control who can use commands.

### Can I limit Herald to specific channels?

Yes! You can:
1. Remove Herald's permissions from unwanted channels
2. Use Discord's command channel overrides
3. Set up a dedicated #herald-rolls channel

### Does Herald log anything?

Herald logs:
- XP transactions (viewable with `/xp_log`)
- Character creation/deletion (local to each server)

Herald does NOT log:
- Roll results
- Private character data
- User messages

---

## Getting Help

### Where can I report bugs?

- Join our [Support Discord](https://discord.gg/9bEZk6ARG9)
- Post in the #bug-reports channel
- Include screenshots if possible

### Can I suggest features?

Absolutely! Feature requests are welcome:
- Post in the #suggestions channel on our Discord
- Describe what you want and why it would help

### Is there a roadmap?

Check our [Support Discord](https://discord.gg/9bEZk6ARG9) for announcements about upcoming features.

### How can I contribute?

Herald is open source! Visit our [GitHub repository](https://github.com/yourusername/herald) to:
- Report issues
- Submit pull requests
- Improve documentation
- Help other users

---

## Still Have Questions?

- **[Join our Support Server](https://discord.gg/9bEZk6ARG9)** - Get help from the community
- **[Check Common Issues](common-issues.md)** - Solutions to frequent problems
- **[Read the Guides](../guides/quickstart.md)** - Detailed tutorials

---

*Can't find your answer? Ask in our Discord server - we're here to help!*
