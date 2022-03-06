---
sidebar_position: 2
---

# Environment Variables

Setting environment variables allows you to customise the bot to your liking.

The bot cannot run without specifying the minimum environment variables whilst others merely make the bot more unique, like embed colours.

## Configure environment variables

Create a .env file in the folder you have cloned.

```bash
# Required
DISCORD_API_KEY=Your_Discord_API_Key
MONGODB_URI=MongoDB_URL

# Optional
DEFAULT_GUILD_ID=Default_Guild_Id
BOT_PLAYING=Bot_Playing
BOT_COLOR_HEX=EMBED_COLOR_HEX # Remove the hash from the hex value. E.g. #0067f4 -> 0067f4
```

| Environment Variable | Required | Default                      | Description |
|----------------------|----------|------------------------------|-------------|
| DISCORD_API_KEY      | ✅      | No default; will fail without | This the API key you have retrieved from the Discord Developer Portal. |
| MONGODB_URI          | ✅      | No default; will fail without | To store preferences, Notify uses MongoDB, an online database service. This is the uri you will have generated from that. |
| DEFAULT_GUILD_ID     | ❌      | null                          | **This variable should only be used during development**. It is the ID of the Discord server that you would like to register slash commands with. This is because by default, Discord can take up to an hour to register slash commands. In production, this can be omitted. |
| BOT_PLAYING          | ❌      | bandev.uk/notify              | This is what you would like to show the bot playing. |
| BOT_COLOR_HEX        | ❌      | 0067f4                        | This is the hex value of the colour that you would like all embeds that the bot sends to use. **Make sure you remove the `#` from the hex value.** |
