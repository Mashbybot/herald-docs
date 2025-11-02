# Adding Herald to Your Server

Learn how to invite Herald to your Discord server and configure permissions.

---

## Step 1: Invite Herald

Click the invite link below to add Herald to your server:

**[Invite Herald to Your Server](https://discord.com/oauth2/authorize?client_id=1388202365198270595)**

!!! warning "Update Invite Link"
    Server administrators: Update the `YOUR_BOT_ID` in the link above with your actual bot's client ID from the Discord Developer Portal.

---

## Step 2: Select Your Server

1. A Discord authorization page will open
2. Select the server where you want to add Herald from the dropdown
3. Click **Continue**

!!! info "Permissions Required"
    You must have the **Manage Server** permission to add bots to a Discord server.

---

## Step 3: Review Permissions

Herald requests the following permissions:

### Required Permissions

- **Send Messages** - Respond to commands and send results
- **Embed Links** - Display character sheets and dice results in formatted embeds
- **Use Slash Commands** - Access to Discord's slash command system (automatic)

### Recommended Permissions

- **Use External Emoji** - Display custom dice emojis for better-looking rolls
  - *Without this, Herald uses text-based dice results instead*

### Optional Permissions

None! Herald doesn't need any elevated permissions like managing roles, channels, or messages.

---

## Step 4: Authorize

Click **Authorize** to complete the installation.

Herald will join your server and be ready to use immediately!

---

## Verifying the Installation

### Check if Herald is Online

1. Look for Herald in your server's member list
2. Herald should show as **online** (green status)
3. If offline, Herald may be restarting or experiencing issues

### Test a Command

Try a simple command to verify Herald is working:

```
/help
```

If Herald responds with the help menu, everything is working correctly!

---

## Troubleshooting

### Herald Isn't Responding

**Check slash command permissions:**

1. Go to **Server Settings** → **Integrations** → **Herald**
2. Ensure slash commands are enabled
3. Check that the `@everyone` role (or your role) has **Use Application Commands** permission

**Check channel permissions:**

1. Herald needs permission to view and send messages in channels where commands are used
2. Right-click the channel → **Edit Channel** → **Permissions**
3. Ensure Herald's role has **Send Messages** and **View Channel** enabled

### Dice Emojis Not Showing

Herald uses custom emojis to display dice results. If you see text instead of emoji:

**Option 1: Enable External Emoji Permission**
1. Give Herald the **Use External Emoji** permission

**Option 2: Use Text Mode**
- Herald automatically falls back to text-based results
- No configuration needed!

### Commands Not Appearing

If slash commands don't appear when you type `/`:

1. Wait a few minutes - Discord can take time to sync commands
2. Try restarting your Discord client
3. Check that Herald has the **Use Application Commands** permission
4. Try using the command anyway by typing it fully: `/help`

---

## Configuration Options

Herald works out of the box with sensible defaults. However, you may want to:

### Set Up a Commands Channel

Create a dedicated channel for character management and dice rolling:

1. Create a channel like `#herald-rolls` or `#character-sheets`
2. Pin a message with common commands or the bot invite link
3. Herald works in any channel where it has permissions

### Set Up Roles

Consider creating roles for:

- **Storytellers** - Game masters running chronicles
- **Players** - Active players in your games
- **Spectators** - People who can view but not roll

Herald doesn't require special roles, but they can help organize your server!

---

## Next Steps

✅ Herald is now installed and ready to use!

Continue to:

- **[Create Your First Character](first-character.md)** - Make a Hunter
- **[Quick Start Guide](quickstart.md)** - Learn the basics
- **[Command Reference](../commands/index.md)** - See all available commands

---

!!! question "Still Having Issues?"
    Join our [Support Server](https://discord.gg/9bEZk6ARG9) for help from the community and developers!
