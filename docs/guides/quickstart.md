# Quick Start Guide

Get up and running with Herald in under 5 minutes!

---

## 1. Add Herald to Your Server

Click the link below to invite Herald to your Discord server:

**[Invite Herald](https://discord.com/oauth2/authorize?client_id=1388202365198270595)** *(Update this link with your actual bot invite URL)*

!!! tip "Required Permissions"
    Herald needs these permissions to work properly:
    
    - **Send Messages** - To respond to commands
    - **Embed Links** - To display character sheets and dice results
    - **Use External Emoji** - To show dice results (optional but recommended)
    - **Use Slash Commands** - Required for all commands

---

## 2. Create Your First Character

Once Herald is in your server, create a character:

```
/create name:Raven
```

That's it! Herald creates a character with default attributes (all set to 1). You can customize it later.

!!! success "Character Created!"
    Herald will confirm your character was created and show you the character sheet.

---

## 3. View Your Character Sheet

Check out your character anytime:

```
/sheet character:Raven
```

Herald displays:
- All attributes (Physical, Social, Mental)
- Derived stats (Health, Willpower)
- Skills and specialties
- Hunter-specific traits (Edge, Desperation, Creed, etc.)
- Equipment and notes

---

## 4. Roll Some Dice

### Basic Manual Roll

Roll dice manually without a character:

```
/roll attribute:3 skill:2 difficulty:2
```

This rolls 5 dice (3 + 2) and checks if you meet difficulty 2.

### Character-Based Roll

Roll using your character's stats:

```
/roll_char character:Raven attribute:Dexterity skill:Stealth difficulty:2
```

Herald automatically looks up Raven's Dexterity and Stealth ratings and rolls them!

---

## 5. Set Up Your Character

### Add Attributes

Set your character's attributes:

```
/create name:Raven strength:2 dexterity:4 stamina:3 charisma:3 manipulation:2 composure:3 intelligence:3 wits:3 resolve:2
```

Or update them later with character progression commands.

### Add Skills

Set individual skills:

```
/skill_set character:Raven skill:Firearms dots:3
/skill_set character:Raven skill:Stealth dots:4
```

Or use a skill template for quick setup:

```
/skill_template character:Raven template:Balanced
```

### Add Specialties

Give your character specialties for bonus dice:

```
/specialty character:Raven skill:Firearms specialty:Pistols
```

---

## 6. Manage Hunter Mechanics

### Set Your Creed

Choose your Hunter's Creed:

```
/creed character:Raven creed:Avenger
```

### Track Edge

Set your Edge rating (adds dice to rolls):

```
/edge character:Raven edge:3
```

### Track Desperation

When things get dangerous, track Desperation:

```
/desperation character:Raven desperation:2
```

---

## 🎉 You're Ready to Hunt!

That's all you need to get started! Herald handles the rest.

### What's Next?

- **[Character Creation Guide](character-creation.md)** - Detailed character building
- **[Dice Rolling Guide](dice-rolling.md)** - Master H5E dice mechanics
- **[Command Reference](../commands/index.md)** - All available commands
- **[Hunter Mechanics](hunter-mechanics.md)** - Edge, Desperation, and more

---

## Quick Reference Card

| Action | Command |
|--------|---------|
| Create character | `/create name:"Name"` |
| View sheet | `/sheet character:Name` |
| Roll with character | `/roll_char character:Name attribute:Attr skill:Skill` |
| Manual roll | `/roll attribute:# skill:#` |
| Set skill | `/skill_set character:Name skill:Skill dots:#` |
| Add specialty | `/specialty character:Name skill:Skill specialty:Name` |
| Set Edge | `/edge character:Name edge:#` |
| Get help | `/help` |

---

!!! question "Need More Help?"
    - Type `/help` in Discord for in-bot assistance
    - Visit our [FAQ](../support/faq.md)
    - Join the [Support Discord](https://discord.gg/9bEZk6ARG9)
