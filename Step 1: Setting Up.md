# Step 1: Setting up an IDE and the Default Mod Base.

Depending on whether you're doing Lua or C# mods you'll need different apps. So I'll go through settings up environments for both. As with any project, and especially with modding, I would

### highly

recommend getting a dedicated modding/coding folder rather than using your desktop or so. If you want to make a mod, you will end up needing to have dedicated folders for art files, your own code, other mods' source code, etc. Now, OSFE already gives a dedicated "modding" folder that we could use, which provides a lot of the data that we're going to reference.
It's in `Eden Install Location\One Step From Eden\OSFE_Data\StreamingAssets`, and I will be using that folder for the setup. 
Of course, you could always copy those files over to a place you like and work there, maybe even symlink em over if you wish. If you know what makes you comfortable, your dev environment is up to you.

## Lua Mods:   

### Settings up an IDE (VSC)
For Lua modding you'll pribably have a repo and be editing different file types in 1 folder, while refering to files outside of it constantly. For this reason I will personally recommend using Visual Studio Code. It's great for managing multiple file extentions, multiple locations simultaniously, and editing things that don't necessarily have a big IDE.
Keep in mind that **Visual Studio Code is NOT Visual Studio**. They are two very different applications. So:
Grab VSC from [here](https://code.visualstudio.com/), Install it in a nice place where you keep your programs, and start it up.

Press the extention (4 squares) button on the left side and instal the following ones:
* Lua extention - Just search "lua". I personally use the one by sumneko, but if it for some reason doesn't work for you, they one by keyring works just as well. 
* XML extension - just search "xml". The one by Josh Johnson is nice, and provides a cool tree-view of your xml. The one by Red Hat is also nice. I actually have them both installed though I'm not sure if that actually contributes anything. But now I don't have to figure that out.
* Honestly you can just browse through the top if you see anything you like. VSC is suuuper customizable, but everything else is optional.

On your computer, create the `\OSFE_Data\StreamingAssets\Mods`  folder if it doesn't exist, then create a new folder inside it. This will be where you put your new mod. What you name it will also be registered as the name of your mod.

In VSC, go to File -> Open folder, and open the newly created mod folder.

![enter image description here](https://i.imgur.com/pQ4J2bs.png)

Then go to File -> Add Folder to Workspace and `OSFE_Data\StreamingAssets\Data`. Do the same for `OSFE_Data\StreamingAssets\ExampleMods`.

![enter image description here](https://i.imgur.com/kf5MhTT.png)

Cool, if you open up the explorer pane on the left, you should now be able to work on your mod while referencing the basegame data fairly easily. You can drag and drop the folders to re-arrange them. 

Now just go to file -> Save Workspace As, and save it somewhere like your mod's folder. VSC will auto-load your last workspace at the start, but if you have multiple mods, workspaces are a nice way to manage them.

You're done with VSC! Next step: Git Repo!
 
## C# Mods
For C# you have 2 options for IDEs.
Visual Studio Community Edition (Free always) or JetBrains Rider (free only if you have a student email). I personally recommend Rider, but obviously not everyone has access to it, and ether works fine.

Regardless, first you'll need to get and install Visual Studio 4.5.2 from here:
https://www.microsoft.com/en-gb/download/details.aspx?id=42643

Let's start with
### Visual Studio:
1. Get it from here and Install it: 
https://visualstudio.microsoft.com/
![enter image description here](https://i.imgur.com/XYyirar.png)
2. Click "Create a New Project"

3. Type "dll" in the search box and select Class Library (.NET Framwork) with C# (third option).

![enter image description here](https://i.imgur.com/ueH3phR.png)
* You can put it in your mods folder, especially since we'll be setting up a git repository later and it'll be nice to sync your C# as well.

* Make the solution name the same as your mod name.

* Select `.NET Framework 4.5.2` as your framework.

4. This should load up a project. (This is probably a good time to go find that dark theme setting.) Next, we need to add unity, harmony, and our game as libraries/referneces to be able to use them in code. On the right side, in the Solution Explorer, right-click "References" and select "Add Reference...".
 ![enter image description here](https://i.imgur.com/YZEqPwN.png)
  On the bottom right, press the "Browse" button and find `Your OSFE Install Location\OSFE_Data\Managed`. Then, select `0Harmony.dll`, `Assembly-CSharp.dll` and `UnityEngine.dll`  (You can ctrl-click them or add them 1 by 1). You can add other libraries/referneces like this when your code calls for it. Press ok and then you are good to go! 

But, let's do some quick quality of life adjustments:
Expands the Reference tab, select a reference you just added (say, 0Harmony) and then, below, in the properties tab, set Copy Local to be False. Do this for all the other references that it's True for (should be just the 3 you added).

![enter image description here](https://i.imgur.com/cXxvb2V.png)
Then, right-click on the Library name (Not the solution above!) and select properties.
 
![enter image description here](https://i.imgur.com/1UkBw8C.png)
Then, on the left side select "Build", and on the bottom - Output path. For the output path, select your mod folder.

![enter image description here](https://i.imgur.com/54VyEHA.png)
What this will will do is make it so that whenever we build our C# mod (patch), it'll just put the .dll inside the mod folder without anything extra, so we can instantly start the game and test it out!
