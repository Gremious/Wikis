## Time to setup a Version Control System!
Setting up VCS is actually pretty simple (even if I have made this guide rather wordy) and will **highly** benefit you in the long-run. Not only with modding, but with general coding, no matter what/where you code.

If you don't want to share your mod with anyone that's fine, you can make your repo private. But I still recomment having a repo. It will:
* Let you revert to an earlier state of your mod in case you horribly screw something up
* Let you share your code with people in #modding fairly easiy if you need help debugging
* Keep your data backed up in case some disaster happens
* Build good programming habits

 We'll be using Git + GitHub.

Official Documentation for extra help:
https://code.visualstudio.com/docs/editor/versioncontrol

---
I'll split this into VSC, VS and Rider seperately, however, please note that you'll only need to do 1 of these! In terms of easiness, I say it goes Rider ->  VS -> VSC.
But first, some things you'll have to do for any of them:

#### Step 0: Create a GitHub account

If you don't have one already, go ahead and create a GitHub Account ([https://github.com/join](https://github.com/join)).
#### Step 1: Download and Install git
We can't use git if we don't have it, so hop on over the the [git website](https://git-scm.com/downloads) and download the latest version for your OS.

You can leave every setting at default and just press next until you hit install, however, please take a note of 2 things:

1. Make sure that this setting is selected when you reach it:
 
![enter image description here](https://i.imgur.com/2ZgFtvt.png)

2. Note the installation path, as we'll need it later (only needed for c# mods).

You can also select a different text editor for git related files (like notepad++ or whatever you like to use) if you want, when you reach that setting.

### VSC

#### Step 0: Create a GitHub repository
1. Press the plus button at the top right, and press New repository
![enter image description here](https://i.imgur.com/DvfST3I.png)
2. Name it something nice like OSFE-YourModName or some such
3. Make it public or private as you wish. Keep in mind that making it private will prevent you from sharing your code on github with others if you want help.
4. We'll manually add a .gitignore cause this project is a little unique.
5. Add a lisence, if you wish. MIT is a good for mods, and translates to "everyone can use this but it has to be MIT too". 

In VSC, open the Source Control tab on the left (3 dots connected via lines). (If you don't see some of the tabs you need, just right-click the tab bar).

![enter image description here](https://i.imgur.com/fkp4jfN.png)
Press Initialize Repository and select **your mod folder**.
Don't commit anything just yet as you likely have a lot of junk files.
Grab the .gitignore file from this repo (https://github.com/Gremious/OSFE-DefaultMod/blob/master/.gitignore). If you've already downloaded this repo, just copy it over to your mod folder. If not, press the "Raw" button to open all the text, copy it, and create a new file in your mod folder and name it ".gitignore".

![enter image description here](https://i.imgur.com/UJqpwhR.png)
And just paste it in and save.

Now, we need to link your local git repo with GitHub.
Go back to the Source Control tab, press Ctrl+Shift+P and search for "Add Remote"
![enter image description here](https://i.imgur.com/UM85PM0.png)
For the remote name put "Origin". For the url, provide it with your GitHub repo url, i.e. https://github.com/YourUsername/OSFE-YourModName

Then add a commit message and press the commit button.

![enter image description here](https://i.imgur.com/FgotKuR.png)
If you're gonna be using the git GUI, I recommend ticking "Always" on the auto-stage-changes dialogue. Makes life easier.

![enter image description here](https://i.imgur.com/ceQbZaO.png)
If this is your first time using Git ever, you'll be faced with a window asking you to give git your name/email. You can open the Learn More link it gives (https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) to read up more. In short, what you want to do is press ctrl+shift+p and search "new terminal" and open an integrated (or external, doesn't really matter) one. Then, type 

`git config --global user.name "John Doe"` (replacing John Doe with your username) 

And then 

`git config --global user.email johndoe@example.com`(replacing johndoe@example.com with your email).

Finally, you can press the commit button (or type `git commit -am "Initial Commit"` in the terminal if it's open in your mod directory) and commit! 

Then press the `...` button and press Push (or `git push` in the terminal) and push your changes to GitHub!

![enter image description here](https://i.imgur.com/hN2t0hA.png)
If you don't have a branch on GitHub, it'll ask you to create one, just press ok, login, and you're good to go! If it asks, running `git fetch` periodically is ok and will notify you if your local version is behind or something.


### Rider


