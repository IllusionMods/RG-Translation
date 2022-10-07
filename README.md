# RG-Translation

English fan translation project for Room Girl. The translations are applied while the game is running and do not require replacing or modifying any game files.

## Prerequisites
- BepInEx 6.0 pre.1. Use [BepInEx_UnityIL2CPP_x64_6.0.0-pre.1.zip](https://github.com/BepInEx/BepInEx/releases/tag/v6.0.0-pre.1)
- XUnity Auto Translator for IL2CPP. Use [XUnity.AutoTranslator-BepInEx-IL2CPP
](https://github.com/bbepis/XUnity.AutoTranslator/releases)

## Installation

1. Ensure you have the prerequisites installed.
2. Go to the "releases" page above and download the latest version. Alternatively, advanced users can get the latest beta translations by clicking on the "Clone or download" button above. If you are a translator, read the sections below to see how to contribute to the translations.
3. Extract the zip and place the BepInEx folder inside your game folder (where the file "RoomGirl.exe" is).

## Contribution

Any help is appreciated. Regardless of your translation skill and Japanese knowledge you can still help with translations. Even if you have no experience, you can help by proofreading or using machine translation services such as Google Translate or [DeepL](https://www.deepl.com/translator) (we currently recommend to use [DeepL](https://www.deepl.com/translator)). In the case of machine translations, clean up the translation using sanity and a little logic.

Translation done purely by machines must be kept in the designated files (`zz_machineTranslation.txt` files). These should be considered placeholders until manual translations are available. The goal is to have everything manually translated.

### Basic operation and structure

Each translation line follows the pattern: 
```
original text=translated text
```
Example: 
```
悟飯=Food
``` 
Lines beginning with `//` are considered comments, i.e., they are not considered in the translation.

The translations are all inside the `Bepinex\Translation\en\Text` folder. They are then split into the following directories:
- `Main` - The main UI for the game.
- `CharacterMaker` - Items for the Character Maker.
- `H-Positions` - Names of sex positions
- `zz_HS2` - Temporary folder with old translations from HS2. Contains item names and H-Positions names. The goal is to transfer translations from this folder to the proper ones.

Coordinate with other translators on the [Illusion Soft Discord server](https://discord.gg/illusionsoft) #translation channel. To avoid translation conflicts please ask if anyone is working on a file. If you have any questions about the quality of your translations, ask for advice on the server.

### How to add or improve translations

- If you want to make a simple edit simply open the file in question and click edit. After you are done editing, commit the changes and start a pull request.
- If you have more translations to submit [fork the repository](https://help.github.com/articles/fork-a-repo/). This will make a copy of the original project in your account. Upload your changes to the fork into your account, and then [send a pull request](https://help.github.com/articles/about-pull-requests/) to the original project. Your pull request will be reviewed and accepted after a quality check (since nobody is playing Room Girl, we are accepting anything). Again, avoid raw machine translations. Proper capitalization, punctuation, and spelling is a must.

## Text Translations

Texts use the `Text` directory. In this directory the first translation found for a given text is used every time that this same text is found. But sometimes the same word can have different meanings depending on where you are in the game, in this case you can use the "Scope Level" feature to tell which translation should be used in that part of the game.

### Scope Levels

To use scope levels, use the following structure:
```
#set level xxx
text=translation
text2=translation2
#unset level xxx
```
Where "xxx" represents the number of the desired scope level. Below is a table containing the known scope levels and their locations:

#### Known Scope Levels

| Level | Description           |
|------:|-----------------------|
| -1    | Global                |
|  3    | Title Screen          |
|  4    | Character Maker       |
|  5    | World Map             |
|  6    | ActionScene (Room UI) |
|  7    | Free H                |
|  8    | Network Check         |
|  9    | Uploader              |
|  10   | Downloader            |
|  11   | Nework Entry          |

## Tools

- [Release Tool](https://github.com/SpockBauru/TranslationToolsHS2#releasetoolhs2) - Tool that cleans up the translation files to remove any unnecessary untranslated parts.
- [Yomichan](https://foosoft.net/projects/yomichan/) - This browser plugin allows you to see the definition of Japanese words by putting your mouse over them in the browser and pressing shift.
- Dictionaries:
  - https://jisho.org/
  - http://www.romajidesu.com/
  
