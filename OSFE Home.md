# Home

## Welcome to the default guide for making OSFE mods.
The Default Mod Base is an over-commented 'tutorial/start-from' mod for those wishing to make mods from more than a completely empty canvas, and less than a complicated, pre-existing mod with many parts. It also aims to explain/detail (near) every part of OSFE modding. It's also for those who just want to reference it's code while learning to mod OSFE from scratch (you can do that via the [Community Google Doc](https://docs.google.com/document/d/1UUzJ9vVBsSVATHjzDGdZrsVPzNhf8Iy_PfPWfkghUZI), and by referenceing the `OSFE_Data/StreamingAssets/Data` folder, as well as other mods).

## Making Mods
I want to prephase this guide by saying that, generally speaking, there are 2 types of mods you can be making in OSFE. While a lot of mods will inevitably use both methods together, the types are entirely based on whether you use the original built-in modding tools (XML and Lua), or C# ([Harmony](https://harmony.pardeike.net/)). 

### Lua Mods:
If you just want to make a character/spells/artifact mod that uses mechanics already existing in the game (with some leeway), then you're in luck. The game provides built-in mod support via XML and Lua. The game loads every Hero, Monster, Spell, Artifact and Effect through said XML and Lua too, meaning:
1. We have a full reference of how any effect/item that exists in the basegame would be modded;
2. If an existing spell/artifact/etc. does something, you can do it too, and it's as simple as copy-pasting!

### C# Mods:
Alas, not everything is provided via the original modding tools. If you want to go beyond what they give you and to make more complicated changes, such as, for exmaple, changing the battle mechanics or adding new brands, you will need to use C#. 
Luckily, the Dev of this game is incredible and puts in an amazing effort to improve the modding community (and the general state of the game too!). As such, we have Harmony included with the game! (Currently on the beta branch).
Harmony allows us to create "patches" - methods that will be inserted into the game's existing methods and ran when they run. With this power, can edit/do almost anything (albeit some things might require a lot more effort than others).

Once you are ready to start, you can proceed to Step 1: Setting up!
***

## List of Links:
(Don't worry, this is just for quick reference if you need it, you don't need to open all of them right now. All links provided when needed.)

* OSFE Offical Discord: https://discord.gg/osfe (find us in #modding!)

* The OSFE Workshop: https://steamcommunity.com/app/960690/workshop/

* The Community Modding Google Doc: https://docs.google.com/document/d/1UUzJ9vVBsSVATHjzDGdZrsVPzNhf8Iy_PfPWfkghUZI

* Harmony Documentation: [https://harmony.pardeike.net/](https://harmony.pardeike.net/ "https://harmony.pardeike.net/")

* Visual Studio and Visual Studio Code: https://visualstudio.microsoft.com/ 

* DotPeek: https://www.jetbrains.com/decompiler/
<!--stackedit_data:
eyJwcm9wZXJ0aWVzIjoidGl0bGU6IE9TRkUgTW9kZGluZ1xuYX
V0aG9yOiBHcmVtaW91c1xuIiwiaGlzdG9yeSI6WzE3Nzg5NDM1
NzEsLTE1MjQ5MzEzOTddfQ==
-->