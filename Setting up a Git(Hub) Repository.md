## Time to setup a Version Control System!
Setting up VCS with VSC is actually pretty simple (even if I have made this guide rather wordy) (since they basically provide it out of the box) and will **highly** benefit you in the long-run. Not only with modding, but with general coding, no matter what/where you code.

If you don't want to share your mod with anyone that's fine, you can make your repo private. But I still recomment having a repo. It will:
* Let you revert to an earlier state of your mod in case you horribly screw something up
* Let you share your code with people in #modding fairly easiy if you need help debugging
* Keep your data backed up in case some disaster happens
* Build good programming habits

 We'll be using Git + GitHub.

Official Documentation for extra help:
https://code.visualstudio.com/docs/editor/versioncontrol

---
I'll split this into VSC and VS/Rider seperately, but first, some thing you'll have to do for both:

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
3. Name it something nice like OSFE-YourModName or some such
4. Make it public or private as you wish. Keep in mind that making it private will prevent you from sharing your code on github with others if you want help.
5. We'll manually add a .gitignore cause this project is a little unique.
6. Add a lisence, if you wish. MIT is a good for mods, and translates to "everyone can use this but it has to be MIT too". 
