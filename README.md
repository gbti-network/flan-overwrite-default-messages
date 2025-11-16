# Flan Custom Messages - Mystical Theme

A Minecraft datapack that overrides all Flan land claiming mod messages with a mystical/arcane theme. Transform your server's claim system into a magical ward system with custom terminology and atmospheric messaging.

## You Might Be Looking For This If...

- You want to customize or change Flan's default claim messages
- You're searching "how to change Flan messages" or "Flan custom text"
- You need to override the "Sorry you can't do that here!" message
- You're looking for Flan language file overrides or translations
- You want to rebrand Flan terminology to match your server's theme (RPG, fantasy, medieval, etc.)
- You need to make Flan messages silent or less intrusive
- You're trying to figure out how to edit Flan's claim protection messages
- You want to change "Owner" to something else like "Keeper", "Lord", or custom text
- You're searching for Flan datapack customization or server-side message changes
- You need themed claim messages without requiring players to download resource packs
- You want to change the color or formatting of Flan's chat messages
- You're looking for examples of Flan translation keys and language overrides

## Features

- 🔮 **Complete Message Overhaul**: All 300+ Flan messages replaced with mystical alternatives
- 🎨 **Themed Terminology**:
  - Claims → Wards
  - Owners → Keepers
  - Players → Souls
  - Groups → Circles
  - Permissions → Bindings
  - Menus → Grimoires
- 💜 **Custom Styling**: Purple-colored mystical messages
- 🚀 **Server-Side Only**: No client downloads required
- ⚡ **Instant Updates**: Use `/reload` to apply changes

📖 **[Read the full tutorial: How to Edit Flan Messages](https://gbti.network/minecraft/how-to-edit-flan-text-messages-in-minecraft)**

## Quick Start

### Installation

1. **Download this datapack** (clone or download ZIP)

2. **Upload to your server:**
   ```
   <world-name>/datapacks/flan_custom_messages/
   ```
   Example: `world/datapacks/flan_custom_messages/`

3. **Reload your server:**
   ```
   /reload
   ```
   OR restart the server

4. **Verify it's enabled:**
   ```
   /datapack list
   ```
   You should see: `[file/flan_custom_messages] (enabled)`

### Testing

- Join your server
- Check a claim (hold inspection tool and right-click): "These lands answer to [keeper]"
- Try breaking a block in a protected claim: "A mysterious force prevents you from doing this."

## Version Compatibility

This datapack is compatible with multiple Minecraft versions. The `pack_format` value determines compatibility:

### Supported Versions

| Minecraft Version | Pack Format | Status |
|------------------|-------------|---------|
| 1.21.4 | 57 | ✅ Latest |
| 1.21.2 - 1.21.3 | 48 | ✅ Supported |
| 1.21 - 1.21.1 | 48 | ✅ Current |
| 1.20.5 - 1.20.6 | 41 | ✅ Compatible |
| 1.20.3 - 1.20.4 | 26 | ✅ Compatible |
| 1.20 - 1.20.2 | 15 | ✅ Compatible |

### Updating for Different Versions

**Current Configuration** (in `pack.mcmeta`):
```json
{
  "pack": {
    "pack_format": 48,
    "description": "Custom Flan messages with mystical theme"
  }
}
```

**To change versions:**

1. Edit `pack.mcmeta`
2. Change the `pack_format` number to match your Minecraft version (see table above)
3. Save and upload to your server
4. Run `/reload`

**Example for Minecraft 1.20.5:**
```json
{
  "pack": {
    "pack_format": 41,
    "description": "Custom Flan messages with mystical theme"
  }
}
```

### Flan Mod Compatibility

This datapack works with **all versions of Flan** for the supported Minecraft versions above. The language override system is version-independent - as long as Flan uses the same translation keys, the messages will be replaced.

**Tested with:**
- Flan 1.12.x (Minecraft 1.21.1)
- Flan 1.11.x (Minecraft 1.20.x)
- Flan 1.10.x (Minecraft 1.20.x)

## Example Messages

### Before (Default Flan)
```
Sorry you can't do that here!
Owner: PlayerName
Claim created successfully
You don't have permission
```

### After (Mystical Theme)
```
A mysterious force prevents you from doing this.
Keeper: PlayerName
A new warded territory has awakened.
The weave refuses to let you unmake this ward.
```

### Full Theme Examples
- "No warded ground lies here."
- "These lands answer to %player%"
- "The bond has shifted. New keeper: %player%"
- "A new circle has been formed: %group%"
- "The wards have reshaped themselves."
- "You stand too close to protected ground."
- "Shifted the circle for these souls to %group%"
- "The scriptures have been reread." (config reload)

## Customization

### Changing Message Colors

Edit `data/flan/lang/en_us.json` and add color codes:

**Current (Dark Purple):**
```json
"flan.noPermissionSimple": "§5A mysterious force prevents you from doing this."
```

**Available Colors:**
- `§4` - Dark Red (danger)
- `§5` - Dark Purple (mystical)
- `§6` - Gold (important)
- `§9` - Blue (info)
- `§c` - Red (error)
- `§d` - Light Purple (magic)
- `§e` - Yellow (warning)

**Formatting:**
- `§l` - Bold
- `§o` - Italic
- `§n` - Underline
- `§k` - Obfuscated (scrambled)

**Example combinations:**
```json
"flan.noPermissionSimple": "§d§oA mysterious force prevents you from doing this."
```
(Light purple + italic)

### Editing Messages

1. Edit `data/flan/lang/en_us.json`
2. Find the message key you want to change
3. Update the text
4. Save and upload to server
5. Run `/reload`

**Example:**
```json
{
  "flan.noPermissionSimple": "Your custom message here!",
  "flan.claimCreateSuccess": "Your ward has been established!",
  "flan.noPermission": "The ancient magic blocks your path."
}
```

### Making Messages Silent

To hide specific messages, use a single space:
```json
"flan.noPermissionSimple": " "
```

## File Structure

```
flan_custom_messages/
├── pack.mcmeta                    # Datapack metadata (edit for version compatibility)
├── README.md                      # This file
└── data/
    └── flan/
        └── lang/
            └── en_us.json        # Custom language overrides
```

## Troubleshooting

### Datapack not loading

**Check if enabled:**
```
/datapack list
```

**Enable manually:**
```
/datapack enable "file/flan_custom_messages"
```

**Common issues:**
- Wrong folder location (must be in `<world>/datapacks/`)
- Invalid JSON syntax in `en_us.json`
- Wrong `pack_format` for your Minecraft version
- Forgot to run `/reload`

### Messages still showing default text

1. Verify the datapack is enabled (`/datapack list`)
2. Check `pack.mcmeta` has correct `pack_format` for your version
3. Ensure file structure is correct (see above)
4. Run `/reload` or restart server
5. Check server console for errors

### Color codes not working

Make sure you're using the section symbol `§` not `&` or `%`:
- ✅ Correct: `§5Text`
- ❌ Wrong: `&5Text` or `%5Text`

## Advanced: Multi-Language Support

To add support for other languages, create additional language files:

```
data/flan/lang/
├── en_us.json    # English (US)
├── es_es.json    # Spanish
├── fr_fr.json    # French
└── de_de.json    # German
```

Each file follows the same format with translated messages.

## Technical Details

### How It Works

This datapack uses Minecraft's language override system. When Flan tries to display a message like `"flan.noPermissionSimple"`, Minecraft checks datapacks first before using the mod's default text.

**Priority order:**
1. Datapacks (highest - this datapack)
2. Resource packs
3. Mod default languages (lowest)

This means the datapack affects **all players** on the server without them downloading anything.

### Performance

- **Zero performance impact** - Language files are loaded once at startup
- **Instant updates** - Changes apply with `/reload` command
- **No client-side requirements** - Works for all players automatically

## Contributing

Found a message that could be more mystical? Have a better theme idea? Contributions welcome!

1. Fork this repository
2. Make your changes to `data/flan/lang/en_us.json`
3. Test on your server
4. Submit a pull request

## Credits

- **Flan Mod**: [Flemmli97](https://github.com/Flemmli97/Flan)
- **Theme & Messages**: Custom mystical/arcane theme
- **Datapack Format**: Minecraft/Mojang

## License

This datapack only contains language overrides and does not include any Flan mod code. Feel free to use and modify for your server.

## Join Our Community

🎮 **Want to experience this datapack in action?** Join our exclusive members-only Minecraft SMP server!

➡️ **[Become a Member & Join the SMP](https://gbti.network/members)**

Our private server features custom claims with this mystical theme, a welcoming community, and much more. Limited slots available!

## Stay Connected

Follow us on your favorite platforms for updates, news, and community discussions:
- **[Twitter/X](https://twitter.com/gbti_network)**
- **[GitHub](https://github.com/gbti-network)**
- **[YouTube](https://www.youtube.com/channel/UCh4FjB6r4oWQW-QFiwqv-UA)**
- **[Dev.to](https://dev.to/gbti)**
- **[Daily.dev](https://dly.to/zfCriM6JfRF)**
- **[Discord Community](https://gbti.network)**
- **[Reddit Community](https://www.reddit.com/r/GBTI_network)**

## Support

- **Issues**: [GitHub Issues](https://github.com/gbti-network/flan-overwrite-default-messages/issues)
- **Flan Wiki**: [https://github.com/Flemmli97/Flan/wiki](https://github.com/Flemmli97/Flan/wiki)

---

**Made with ❤️ for mystical Minecraft servers by the GBTI Network team**
