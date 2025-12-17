# Richi Multipurpose Bot

A feature-rich Discord multipurpose bot built with Python and discord.py.

## Features

### User Moderation
- `/mute` - Timeout a user (supports seconds, minutes, hours, days)
- `/unmute` - Remove timeout from a user
- `/ban` - Ban a user from the server
- `/kick` - Kick a user from the server
- `/warn` - Warn a user
- `/removewarn` - Remove warnings from a user
- `/clearwarns` - Clear all warnings from a user
- `/hackban` - Ban a user by ID (even if not in server)
- `/nickset` - Set a nickname for a user

### Channel Moderation
- `/slowmode` - Set channel slowmode
- `/lock` - Lock a channel
- `/unlock` - Unlock a channel
- `/purge any` - Purge any messages
- `/purge humans` - Purge human messages only
- `/purge bots` - Purge bot messages only
- `/nuke` - Delete and clone the channel

### Role Management
- `/role give` - Give a role to a user
- `/role remove` - Remove a role from a user
- `/role create` - Create a new role
- `/role delete` - Delete a role
- `/role rename` - Rename a role
- `/role list` - List all server roles

### Information Commands
- `/serverinfo` - Display detailed server information
- `/userinfo` - Display user information
- `/channelinfo` - Display channel information
- `/roleinfo` - Display detailed role information
- `/userlogo` - Display user's avatar
- `/serverlogo` - Display server's icon
- `/userbanner` - Display user's banner
- `/serverbanner` - Display server's banner
- `/ping` - Check bot latency

### Voice Moderation
- `/vcmute` - Mute a user in voice channel
- `/vcunmute` - Unmute a user in voice channel
- `/vcdeafen` - Deafen a user in voice channel
- `/vcundeafen` - Undeafen a user in voice channel
- `/vckick` - Disconnect a user from voice channel
- `/vcmove` - Move a user to another voice channel

### Giveaway System
- `/giveaway start` - Start a new giveaway
- `/giveaway end` - End a giveaway early
- `/giveaway reroll` - Reroll giveaway winners
- `/giveaway list` - List active giveaways

### Automod System
- `/automod enable/disable` - Toggle automod
- `/automod antilinks` - Toggle anti-links
- `/automod antiinvites` - Toggle anti-invites
- `/automod addword` - Add a blocked word
- `/automod removeword` - Remove a blocked word
- `/automod blockedwords` - List blocked words
- `/automod whitelist_channel` - Whitelist a channel
- `/automod whitelist_role` - Whitelist a role
- `/automod settings` - View automod settings

### Messaging Commands
- `/say` - Make the bot send a text message
- `/esay` - Make the bot send an embed message (no timestamp)
- `/announce` - Create a fully customized announcement embed

### Welcome System
- `/greet setup` - Set up a welcome message (simple text or embed)
- `/greet channel` - Set the welcome channel
- `/greet test` - Send a test welcome message
- `/greet config` - View current welcome configuration
- `/greet autodelete` - Set auto-delete duration for welcome messages
- `/greet reset` - Reset and delete welcome configuration

**Welcome Message Variables:**
- `{user}` - Mentions the user
- `{user_name}` - Username
- `{user_avatar}` - Avatar URL
- `{user_id}` - User ID
- `{user_nick}` - Display name
- `{user_joindate}` - Join date
- `{user_createdate}` - Account creation date
- `{server_name}` - Server name
- `{server_id}` - Server ID
- `{server_membercount}` - Total member count
- `{server_icon}` - Server icon URL

### Other Features
- `/help` - Interactive help menu with category selection
- Rotating custom presence
- SQLite database for persistent storage
- Global bot support (works across multiple servers)
- Clean, minimal embed designs

## Configuration

Edit `settings.json` to customize:
- `bot_token` - Your Discord bot token
- `bot_name` - Bot display name
- `embed_color` - Default embed color (hex)
- `presence_messages` - Rotating status messages
- `auto_delete_delay` - Default auto-delete delay in seconds
- `database_paths` - Custom database file locations

## Setup

1. Create a Discord bot application at https://discord.com/developers/applications
2. Copy the bot token
3. Add the token to `settings.json` under `bot_token` (or set `DISCORD_BOT_TOKEN` environment variable)
4. Run `python bot.py`

## Required Permissions

The bot requires the following permissions:
- Manage Channels
- Manage Roles
- Kick Members
- Ban Members
- Moderate Members
- Manage Messages
- Read Message History
- Send Messages
- Embed Links
- Move Members (Voice)
- Mute Members (Voice)
- Deafen Members (Voice)

## Project Structure

```
/
├── bot.py              # Main entry point
├── settings.json       # Configuration file
├── README.md           # This file
├── replit.md           # Project documentation
├── app/
│   ├── core/
│   │   ├── config.py   # Configuration loader
│   │   └── embeds.py   # Embed factory
│   ├── db/
│   │   ├── base.py     # Database base class
│   │   ├── moderation.py
│   │   ├── giveaway.py
│   │   ├── automod.py
│   │   └── welcome.py
│   ├── cogs/
│   │   ├── moderation.py
│   │   ├── channel.py
│   │   ├── roles.py
│   │   ├── info.py
│   │   ├── voice.py
│   │   ├── giveaway.py
│   │   ├── automod.py
│   │   ├── utility.py
│   │   ├── messaging.py
│   │   └── welcome.py
│   └── views/
│       └── help_menu.py
└── data/
    ├── moderation.db
    ├── giveaway.db
    ├── automod.db
    └── welcome.db
```

## Credits

<p>
  <a href="https://discord.com/users/snakke.lol">
    <img src="https://img.shields.io/badge/DEVOLOPER-snakke.lol-5865F2?style=for-the-badge&logo=discord&logoColor=white"/>
  </a>
</p>

<p>
  <a href="https://discord.gg/CVRHgrR2CT">
    <img src="https://img.shields.io/badge/SKYLINE_STORE-Join-2ECC71?style=for-the-badge&logo=discord&logoColor=white"/>
  </a>
</p>

## 🛠️ Tech Stack

<p align="center">
  <a href="https://www.python.org">
    <img src="https://img.shields.io/badge/PYTHON-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  </a>
  <br/>
  <a href="https://discordpy.readthedocs.io">
    <img src="https://img.shields.io/badge/DISCORD.PY-Library-5865F2?style=for-the-badge&logo=discord&logoColor=white"/>
  </a>
  <br/>
  <a href="https://www.sqlite.org">
    <img src="https://img.shields.io/badge/SQLITE-Database-003B57?style=for-the-badge&logo=sqlite&logoColor=white"/>
  </a>
</p>
