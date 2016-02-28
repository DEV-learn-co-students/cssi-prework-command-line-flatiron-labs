
# Using the Command Line

## Overview
In order to access files and folders on our computer, you can either use a graphical display, called a GUI or a text-based tool called a command-line-interface. Instead of pointing and clicking with the GUI, developers can directly contol the computer through typing - which is faster and allows for more automation. In this lesson you will learn the basics commands used in the Terminal.

##Objectives
* Key Terms
* Working Directories
* Listing Files and Folders
* Opening Files 


##Key Terms
* `Terminal` : A text-based tool that allows you to communicate with your computer. The user types a line of text into a simple prompt, and the computer runs that command. On OS X your terminal is an application appropriately called Terminal.
* `Graphical User Interface` : A graphical display that allows you to communicate with your computer through icons and other visual elements like pointers, folders



## Terminal Overview

When you open a file on your computer, you locate it in by navigating through the directories on your computer's file system using Finder. Even files on your Desktop that you click on are stored in your computer's file system, your hard drive.

When you open an application from your Finder or Desktop, it always happens from the context of a "Working Directory" - the directory of your computer you were in when you executed the program. When you click on a file on your Desktop or Open an application from Your Dock or Applications directory, you are still opening a file in a directory. The Dock and Desktop are just abstractions for that directory to make them easy to access.

We're used to navigating and operating on these files using our GUI, our Graphical User Interface, provided by OS X. Our Terminal provides us with a Command Line Interface to navigate and operate on the files and folders of our computer, just like the GUI. As programmers, the Terminal is our workbench, not the GUI.

Let's learn to navigate our computer using the Terminal Command Line Interface. You can choose to watch the video in the next section, read about the commands or do both. Just make sure you are practicing along with the instructions so that you start internalizing some of the commands.

## Command Line Video

Watch the video below if you are unfamiliar with the command line. It will walk you through the basic commands that you will use day to day as you learn to code.

<iframe width="640" height="480" src="//www.youtube.com/embed/s5S_2BdrMJE?rel=0" frameborder="0" allowfullscreen></iframe>

## Working Directories

When you open a Terminal session, you are placed within a directory of your file system. Whatever programs execute or work you do in your Terminal, like when you click on things in your GUI, that action happens in the context of a "Working Directory."

A "Working Directory" just means wherever on your computer's hard drive you are when you execute a program, again, whether through clicking on an icon in your GUI or running a command in your Terminal like `learn hello`. You did that from somewhere. We call that somewhere, wherever you currently are, a "Working Directory".

Open a Terminal and you'll be at your Command Line prompt, where your computer is waiting for instructions.

### What's a Command Line Prompt

Our Command Line prompt, and maybe yours if you configured your environment through Learn, is represented by:

```
[16:19:43] ~
// $
```

The first line, `[16:19:43] ~` is telling us the current time, so expect that part to be different for you, and our current working directory, `~`, which means our Home directory, the default directory for you. We'll explain that idea of a home directory or `~` in a moment.

The next line, `// $` is our command line prompt, where we can type instructions and commands for our computer to execute.

What can you do from a command line prompt? Everything and anything. A command line prompt is the most powerful interface in the world, from which every computer and piece of software can be created, controlled, molded, manipulated, and used.

### `pwd` - Print Working Directory

Let's run our second Command Line program (our first was when you ran `learn hello`).

Type `pwd` from your prompt. You should see something like:

```
~ $ pwd
/Users/avi
~ $
```

From my home directory, `~`, my Terminal presented me a prompt, `$`. I typed `pwd` and pressed Enter on my keyboard. My terminal responded with `/Users/avi` and returned me to my home directory, `~` and gave me a new prompt, `$`.

That's the standard procedure when you execute anything in Terminal, you enter a command from a prompt in a working directory, see output, and are returned to a new prompt in your working directory.

The `pwd` command is an acronym for "Print Working Directory." The `pwd` command prints the working directory of your Terminal session, the folder you are currently "in."

Knowing what directory you are working within is crucial when using your Terminal. You are opening files and running programs that live in directories and you need to make sure you're in the right directory for your task.

You never need to guess, if you're ever curious where you are or need to confirm you are where you think you are, type `pwd`.

#### `~` - Your Home Directory

When you open a new Terminal session, you start in a default location in your file system called your Home Directory. When you use your computer, you are logged in under a user account, you're familiar with this as OS X asks you for your user's password occasionally.

Every user on your computer is given a "Home Directory" for their files. Your operating system, OS X, uses this "Home Directory" to keep your files private from other users that might share your computer.

On OS X, user home directories are stored within a folder `Users` in the root, or top level, main directory, of your harddrive, represented by `/`.

'/' means the main directory of your hard drive. Every file and folder on your computer lives somewhere inside of `/`.

`/Users` is the main `Users` directory in OS X. Within `/Users`, there is a folder for your username, the name of the account you use to login to your computer. My username is `avi` so my home directory is: `/Users/avi`. Yours will be different and you can see it by opening a new Terminal session and typing `pwd`.

The `~` (tilde) character is just a shortcut for your home directory, whatever it may be. Whenever you see your working directory or a file system path with a `~`, you're home.

There's no place like `~`.
![No Place Like Home](http://learn-co-videos.s3.amazonaws.com/learn-co-orientation/no-place-like-home.gif)

## `ls` - Listing Files in a Directory

Within a directory, one thing you're probably curious about is "what files are in this directory?". You can list files within your working directory by executing `ls`:

```
~ $ ls
Applications  Development   Desktop
Documents     Downloads     Public        		    
```

When we type `ls` in Terminal, we're asking our Terminal to list the files and folders in the current working directory.

In my home directory, `~` (which is really `/Users/avi`), I have 6 directories, `Applications`, `Development`, `Desktop`, `Documents`, `Downloads`, and `Public`. You probably have more.

## `cd` - Changing Directories

When you open a new Terminal session, you'll be in a working directory, probably your home directory, `~`. But how do we move around to other directories and change our working directory? You can use the `cd` command, which stands for Change Directory.

From your home directory, try:

```
~ $ cd Desktop
~/Desktop $
```

From within `~`, our home directory, at our prompt `$`, we type `cd Desktop`. Our terminal will change the directory and enter our `Desktop` folder and our prompt will now indicate that our working directory is `~/Desktop`. Your prompt might look a little different but you'll be in your `Desktop` directory. Confirm with: `$ pwd` (remember don't actually type `$`). `pwd` should output something like: `/Users/avi/Desktop`, the full path to your Desktop directory.

Once your working directory is your desktop, try `ls` and have your Terminal list any files that are on your desktop.

### `..` and `.`

How do you move from `Desktop` back up to your home directory? You can always move out of the current folder and back into the parent folder by typing `cd ..`. Just like `~` is a shortcut for home directory, `..` is a shortcut that always means "the directory above" or the "parent directory" of the current. Your file system is a tree like structure, with directories being inside other directories:

```
├── Users
    ├── avi
       └── Desktop
```

`Desktop` is within `avi` which is within `Users` which is at the top of my hard drive, the root, `/`. The path to my desktop is: `/Users/avi/Desktop`. From within `Desktop`, you would refer to the parent directory, `avi` as `..`.

In the same manner that `..` means the directory above, the shortcut `.` means the current directory. You'll see why being able to refer to your current directory as `.` is helpful in a minute.

### cd `~`

You can also change directory back to your home directory from anywhere via `cd ~`. Remember that `~` is a shortcut that means home so if you type `cd ~` you are telling your terminal to change the working directory to your home directory.

## `open ` - Opening Folders and Files

When you're in Terminal, sometimes it is useful to open the current directory you're in, your working directory, in Finder. You can do this with `open .`. That will pop open the OS X Finder view of the directory you are in.

## Opening Folders and Files in Atom Text Editor

`open . -a "Atom"` or `open my_file.py -a "Atom"`

If you want to open an entire directory in Atom, try `open . -a "Atom"`. The `-` sign is a flag, a way to include an option. In this case the `-a` flag is used to optionally specify which **a**pplication to open the directory or file in.


#Tips and Tricks:
+ If you start typing a directory name or file name you can click `Tab` and the command line will automatically fill in the rest of the directory/file name. If you click `Tab` twice it will show you all of the directories/files inside your current directory.
+ Navigating your computer from the command line is a lot about muscle memory. The more practice you have the faster you will get!

#Conclusion
As you learn to build complicated applications, being able to swiftly navigate your computer using the command line will make your life much easier. The command line will be important not just for navigation, but you'll also use it to do things like boot the local server for your web apps, write scripts to automate tasks, and execute other important functions on your computer.
