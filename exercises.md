# Exercises: Basics
An introduction to the UNIX shell, interactive Python and git repositories

## 1. Basic shell commands
Get familiar with UNIX shell and some basic bash commands. Have a look at the slides from this morning and identify commands that are new to you. Test them out! Check out the command's man page (on macOS and Linux you can simply do ```man COMMAND```. If you're on Windows you can check the [online man pages](https://linux.die.net/man/). Also many commands have `--help` option which will display some documentation (e.g. `git --help`). Here are a few tasks/commands you should definitely give a try:

#### a. Create a new local directory (e.g. `python-course`) 
using the commands ```cd``` and ```mkdir```
#### b. Create a new file inside this new local directory (e.g. `hello_world.py`) 
using the command ```touch``` or editors like ```emacs```, ```vim```, ```nano```, `atom`, `notepad` or whatever you prefer
#### c. Rename your file to something unique (e.g. `hello_world_benedikt.py`)
using the command `mv`
#### d. Make your simple python file print a statement (e.g. "Hello world") 
using your favourite editor
#### e. Execute your python script (e.g. `python hello_world_benedikt.py`).
#### f. Add the so called *shebang* to the first line of the python script: ```#!/usr/bin/env python```.
#### g. Make your script executable (x permission) 
using the command ```chmod```. You should now be able to execute your script like this: ```./hello_world_benedikt.py```

In many real-life scenarios, you might be using a remote computing cluster. So lets get familiar with some important commands related to remote systems. We created an account for you on our *davinci* cluster (davinci.icm.uu.se). The username is *python*, the password will be provided by the teachers. Now, some other useful commands for you to try

#### h. Login to the cluster using ```ssh```
#### i. Add your (local) public key (```~/.ssh/id_rsa.pub```) to the remote system (```~/.ssh/authorized_keys```). 
Have a look a the *SSH Tips and Tricks* slide from this morning. Now, logging in to the *davinci* cluster should be much easier.
#### j. Copy your (local) python script to davinci and execute it on davinci. 
Be aware that you share the same home directory with all the other course participants, so use a unique filename or create your own folder. 
#### k. Test the ```screen``` tool. 
Create a python script that runs for a long time (e.g. using time.sleep python function). Execute your script inside a screen session, than detach and completely log out of *davinci*. Now, when you log into *davinci* again, your screen session (and the python script inside) should still be running. 
#### l. If you cannot get enough of shell commands: 
checkout this tutorial: [https://swcarpentry.github.io/shell-novice/](https://swcarpentry.github.io/shell-novice/)

## 2. Working with git
In this part, we want you to get familiar with the most common *git* commands and learn how to use them. Some of the following tasks require you to have a *Github* account. So, if you don't already have one, you can create on here: [http://github.com/join](http://github.com/join). 

<!---
> In order for you to be able to ```push``` your changes to one of our remote repositories (e.g. [https://github.com/uu-python/participants](https://github.com/uu-python/participants)), we need to add you as a collaborator to our *Github* origanization. Therefore, come to the front and write you *Github* username on the whiteboard...
-->

Furthermore you will need to [upload your ssh public key to GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) or [generate an access token for authentication](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token).
The ssh key is used if you clone your repositories using ssh (e.g. `git clone git@github.com:uu-python/day1-basics.git`) and the access token is used if you clone your repository using https (e.g. `git clone https://github.com/uu-python/day1-basics.git`).
Now, some git tasks for you

#### a. Configure your local git environment
This becomes important as you start contributing to shared repositories (your code changes can be associated with your user account).
We'll follow the instructions on the *Setting up git*.
First the name and email (obviously replacing them with your information):

	git config --global user.name "Your Name"
	git config --global user.email "your.email@your.domain"

And finally select the editor (e.g. `notepad`, `vi`, `emacs`, `nano`, etc...) to be used when writing log messages:

	git config --global core.editor nano

#### b. On GitHub fork [https://github.com/uu-python/participants](https://github.com/uu-python/participants), and clone it.
If you need help check [https://help.github.com/en/articles/fork-a-repo](https://help.github.com/en/articles/fork-a-repo).
Note that you should clone the repository that was created *after* the fork, not the original repository!

#### c. Create your own file and push it to a remote repository
Using the clone of the forked repository, follow the instructions on the *Getting familiar with basic commands* slide (30) from this morning and use a unique filename.

#### d. Create a branch, change a file and merge your changes back into the master branch. 
Still using the same forked repository create a branch, change a file and merge your changes back into the master branch.
Some commands from the slide *Contribute to a collaborative project* shown this morning could be helpful.

#### e. Go to GitHub and create a pull request to have your changes incorporated in the *official* parent repository.
You can read more about pull requests here [https://help.github.com/en/articles/about-pull-requests](https://help.github.com/en/articles/about-pull-requests) and [https://help.github.com/en/articles/creating-a-pull-request-from-a-fork](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork).

#### f. Go through the lifecycle of the status of files
Have a look at the slide *The lifecycle of the status of your files* and create scenarios where you go from **Untracked**->**Staged**->**Unmodified**->**Untracked** and **Untracked**->**Staged**->**Unmodified**->**Modified**->**Staged**->**Unmodified**. Use the command ```git status``` in between the steps to monitor how the status of your file is changing.

#### g. Exercise remotes
- Create a github repository.
- To the cloned forked resitory you created in b., add the url of the new repository as a remote called `my_repository`.
- Push your changes to github: `git push my_repository master`
- Check on github that you have indeed pushed your changes.
- Now add https://github.com/uu-python/participants.git as a new remote called `parent` and fetch any changes from it.
- Merge the changes from `parent/master` to your local master branch (there may be a conflict - if so, resolve it).
- Push the new changes to your remote called `my_repository`.

#### h. If you cannot get enough of git commands:
checkout this tutorial/game: [https://github.com/Gazler/githug](https://github.com/Gazler/githug)

## 3. Interactive Python

Start ```jupyter notebook``` and open the notebook ```minimal.ipynb```. The notebook is based on the minimal Python script which has been provided prior to the course. Following the instructions in the notebook, you learn how you can quickly investigate a given problem, visualize and structure it. 

For this part, you need *jupyter* and the Python packages *numpy* and *matplotlib*. If they are not yet installed on your system, follow our instructions here: [https://github.com/uu-python/day0-installation](https://github.com/uu-python/day0-installation).
