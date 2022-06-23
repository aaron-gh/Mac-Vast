# 1 Introduction

## 1.1 What is this?

This is a soundpack for the mud Vast Horizon, written for tintin++. A soundpack consists of a set of script files (.tin files in this case) and sound files. Using a combination of code and witchcraft, incoming texts will trigger sounds, as well as shorten or remove some text.

## 1.2 system requirements

Tintin++ is a very extensive client, that runs on almost anything. However, this pack was written on, tested on, and used on a mac. It may work elsewhere, but I don't know.

The following dependencies are required:

* Homebrew
* tintin++
* sox
* lib-vorbis (if not automatically installed)

# 2 Installation

There are multiple ways to install this pack, depending on how you want to run it. I shall cover the 2 ways to install the pack that assume you do not have a "games" folder in your home directory.

The first way will be running directly from the cloned github repository. This will make updating very simple. All you need to do is pull the changes by typing:

git pull

after using your terminal to navigate to the directory you cloned the repository to.

The second way requires you copy all the files manually again, but may be preferred by less advanced users.

Note: There are 2 branches in this Github repository, Main and Dev. Main will absolutely be more stable, and is recommended. If you run dev, expect things to break a lot. Especially if you pull directly from the git repo. No support will be provided to dev users via in game means. If you have an issue, file it in github instead.

## 2.1 Running from github

For this entire process, I will assume you are using the default Mac OS shell, zsh.

First, install homebrew if not already installed:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

then install git, tintin++, and sox:

brew install git tintin sox

Navigate to the directory you would like to download the repository to using cd <path>.

Clone the Github repository:

git clone https://github.com/aaron-gh/mac-vast.git

Create a symlink (symbolic link) to the folder containing the repository's files with a command similar to the following. Make sure the destination is "~/games", without the quotes.

ln -s <repository-path> ~/games

Now, make a copy of the file called "custom.tin" and name it "vast.tin"

cp ~/games/world/bunkicenter.net/custom.tin ~/games/world/bunkicenter.net/vast.tin

All done, the pack is now installed.

To start the pack, from your home directory in terminal, type:

tt++ games/tt.tin

#2.2 Copying manually

For this entire process, I will assume you are using the default Mac OS shell, zsh.

First, install homebrew if not already installed:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

then install git, tintin++, and sox: (using this method, git is optional)

brew install git tintin sox

Download or clone the git repository:

If cloning, follow the steps in 2.1

If not, expand the "code" button, and select "download zip"

Make a folder in your home directory called games:

mkdir ~/games

copy everything from the folder the repository files are located in (this will be the folder you cloned to, or, if you downloaded the zip file, the extracted folder) to the games folder you just created. You can do this in the terminal, or any other way you like. I am just giving terminal instructions here.

cp -r <repository-path> ~/games

Rename "games/world/bunkicenter.net/custom.tin". to "vast.tin"

All done, the pack is now installed.

To start the pack, from your home directory in terminal, type:

tt++ games/tt.tin

# 3 Soundpack usage

## 3.1 Connecting to the world

After starting the pack, simply type:

connect vast

## 3.2 Recommended usage instructions

I recommend the use of the tdsr screen reader for Mac OS when using this soundpack on a Mac. However, where to obtain it, and how to install and configure it, is beyond the scope of this document.

## 3.3 Aliases and macros

I have provided several aliases and macros in this pack to allow for reloading, managing other worlds, and changing volume. They are::

* spreload: to be executed once logged into Vast Horizon, will instantly reload the soundpack. Useful for applying updates from git.
* addworld <host> <port> [character] [password]: To be ran before connecting to a world if you wish to add a new world. char and password are optional.
* delteworld <world>: deletes a world.
* connect <world>: connects to a world.
* F9: Check sound volume.
* F10: mute/unmute toggle for all sounds.
* F11: turn volume down. Please do not go below 0.0 (I haven't implemented a limit on this yet.)
* f12: Raise volume (Please don't go about 2.0, again, not limit yet.)

# 4 Credits

Thank you to the creator of the Macriani soundpack for Miriani, which I used as a learning tool.

Thank you to the respective creators of sounds used, permission was granted to Bunkicenter to use those sounds.

Thank you to the rest of the Bunkicenter staff, for putting up with my constant testing over the last few days.


# 5 Reporting issues

There are mutliple ways to report issues. Either via the "report" command in game, or though Github. The use of Github is preferd, as game reports should really only be used for game issues, not for issues with the soundpack, however you may use it if you wish.

Once again, if you are using the "Dev" branch **only** report issues through github.
