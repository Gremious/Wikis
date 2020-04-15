If you know what you're doing:

 * Get VSC and Dotpeek for Lua/XML modding.
 * Get VS or JetBrains Rider (Free if you're a student) for C# (Harmony) Modding.
 * `OSFE Install Location\OSFE_Data\StreamingAssets` is the modding
   folder.
 * All in-game items are in `StreamingAssets\Data` in xml/lua format, so you can reference any spell/artifact/hero/etc. in the game from there.
 * If you put a folder in `StreamingAssets\Mods`, then put a file in there that has a name matching any of the files from the `Data` folder, the game will load it as a mod and append it to said file. The folder name becomes the mod name, sans spaces.
 * For more references, the game also has an ExampleMods folder with a character (Lea). She also features a very nice aseprite file for referencing sizes/animation frame durations/etc.
 * If you put a .dll file matching the mod name with a valid Harmony patch, the game will load it and apply the patch itself. You don't have to create a patcher. 
* To load your mod, just press the Mods button in the main menu and press Install Mods on the left. It won't appear in the list as it's not a workshop mod, but the console in the Mods Menu will likely show you some confirmation.
* We don't have a dev console or anything like that, so create a dummy character and give it your modded items/spells in the starting loadout to test them out, or overwrite the existing character loadouts.
