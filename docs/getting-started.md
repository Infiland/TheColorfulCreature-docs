# Getting Started

The Colorful Creature is a difficult platformer with puzzle color mechanics, featuring 350 built-in handcrafted levels made by a single indie developer.

## Development Setup

1. Download the latest version of [GameMaker](https://gamemaker.io/en/download) (2024.11) from:
   - [Official Site](https://gamemaker.io/en/download)
   - [Steam](https://store.steampowered.com/app/1670460/GameMaker/)

2. Clone the repository:
```bash
git clone https://github.com/Infiland/TheColorfulCreature.git
```

3. Setup Steamworks SDK:
   - Download [Steamworks SDK 1.61](https://partner.steamgames.com/?goto=%2Fdownloads%2Flist)
   - Place the SDK folder in: `C:\Users\User\Documents\sdk`
   - Verify the "Steamworks" extension aligns with the SDK path

4. Run the game:
   - Press F5 in GameMaker to test
   - Press F6 for debugging mode

## Contributing

### Making Changes
1. Create your local branch/fork to avoid conflicts
2. Make changes and commit
3. Submit a pull request
4. Wait for Infiland to review and accept the change

### Translations

=== "Game Translations"
    All translations are managed in [this Google sheet](https://docs.google.com/spreadsheets/d/1sO2gPX9AtXJVg1b7byPOB_xi-h8dwmZt5X0aZ08_LOo/edit#gid=0).

    Color coding for translations:
    - ⚪ WHITE - Ready to be translated
    - 🟡 YELLOW - Uncertain translations
    - 🟢 GREEN - Translated and in-game
    - 🔵 BLUE - Changed, needs re-translation

=== "Documentation Translations"
    **WORK IN PROGRESS!**

    To contribute to documentation translations:

    1. Create a new folder in `docs/docs/` with the language code (e.g., `es/` for Spanish)
    2. Copy the English markdown files into the new folder
    3. Translate the content while maintaining the markdown structure
    4. Submit a pull request with your translations

    Currently supported languages:

    - English (default)

### Creating Mods
1. Fork the repository
2. Modify `global.moddedGameDir` in `o_loading` Game Start event
3. Make your desired modifications
4. Contact Infiland for potential Steam Workshop publication

## Community
- [Discord Server](https://discord.com/invite/SSz5THd)
- [Steam Community](https://store.steampowered.com/app/1651680/The_Colorful_Creature/)
- [Reddit](https://www.reddit.com/r/TCC_Game/)
- [Twitter](https://twitter.com/TCC_Game)

## Reporting Issues
1. Go to the [GitHub issues tab](https://github.com/Infiland/TheColorfulCreature/issues)
2. Use prefixes like "Feature:", "Bug:", "Suggestion:", "Documentation:"
3. Provide detailed descriptions
4. Add appropriate labels (e.g., "good first issue", "help wanted")
5. Submit and wait for milestone assignment