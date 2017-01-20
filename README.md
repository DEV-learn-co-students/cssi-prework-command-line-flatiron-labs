
# Using the Command Line

## Overview
In order to access files and folders on our computer, you can either use a graphical display, called a GUI or a text-based tool called a command-line-interface. Instead of pointing and clicking with the GUI, developers can directly contol the computer through typing - which is faster and allows for more automation. In this lesson you will learn the basics commands used in the Terminal.

##Objectives
* Key Terms
* Terminal Overview
* Opening & Docking the Terminal
* The Command Line Prompt
* Listing Files and Folders
* Opening Files 


##Key Terms
* `Terminal` : A text-based tool that allows you to communicate with your computer. The user types a line of text into a simple prompt, and the computer runs that command. On OS X your terminal is an application appropriately called Terminal.
* `Graphical User Interface` : A graphical display that allows you to communicate with your computer through icons and other visual elements like pointers, folders



## Terminal Overview

When you open a file on your computer, you locate it in by navigating through the directories on your computer's file system using Finder. Even files on your Desktop that you click on are stored in your computer's file system, your hard drive.

We're used to navigating and operating on these files using our GUI, our Graphical User Interface, provided by OS X. But as we work learn to become developers we need a quicker, more flexible way to interact with our computer. Let's learn to navigate our computer using the Terminal Command Line Interface. You can choose to watch the video in the next section, read about the commands or do both. Just make sure you are practicing along with the instructions so that you start internalizing some of the commands.

The easiest way to open a terminal is through Spotlight by using COMMAND + SPACE (if you haven't changed the default shortcut), and typing "terminal". Terminal can also be found in the Applications folder in the Utilites subfolder. To keep Terminal in the Dock, you can right click it's icon in the Dock, hover over Options and select "Keep in Dock".

## Command Line Video

Watch the video below if you are unfamiliar with the command line. It will walk you through the basic commands that you will use day to day as you learn to code.

<iframe width="640" height="480" src="//www.youtube.com/embed/s5S_2BdrMJE?rel=0" frameborder="0" allowfullscreen></iframe>



## The Command Line Prompt

A Command Line prompt  is represented by:

```
[16:19:43] ~
// $
```

The first line, `[16:19:43] ~` is telling us the current time, so expect that part to be different for you, and our current working directory, `~`, which means our Home directory, the default directory for you. We'll explain that idea of a home directory or `~` in a moment.

The next line, `// $` is our command line prompt, where we can type instructions and commands for our computer to execute.

What can you do from a command line prompt? Everything and anything. A command line prompt is the most powerful interface in the world, from which every computer and piece of software can be created, controlled, molded, manipulated, and used.

### Working Directories

When you open a Terminal session, it is opened from a specific location, directory of your file system. A directory in the command line is like a folder in the GUI.  You can access the files withith your current working directory. You can also access other files and folders in other locations, as long as you know where those files exist relative to your current location, your current working directory.

### `pwd` - Print Working Directory

Let's run our first Command Line program, `pwd`, which stands for print working directory. This command is the the "You are Here" marker on a map, it shows us where we are within our file system.

When we type in a command, the computer will respond with output and then give you another prompt line so you can keep directing it with instructions.

Let's take a look at this process.  Type your command,  `pwd` into terminal and then press Enter to execute that command. You should see something like:

```
~ $ pwd
/Users/avi
~ $
```

From the home directory, `~`, the Terminal presented a prompt, `$`. The command `pwd`  was typed and executed by using the Enter key. The terminal responded with your current working directory: `/Users/avi`.Then it's waiting for a new command that we can type after the new prompt `$`.

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

## `mkdir` - Make a New Directory

To create a new directory (or folder) you'll want to use the `mkdir` command. Type `mkdir directory_name` replacing the directory_name with the name you'd like to call your directory. 

### Do this Now:
We're going to make a new directory called 'development' in our root folder that will hold on to all of our labs. Whenever you clone a repo from github, do it here so we can keep organized. Type `cd ~` to navigate to the root folder, and then `mkdir development` to create the directory. Type `ls` to confirm that it's there!

## `touch` - Make a New File

To create a new file you'll want to use the `touch` command. Type `touch file_name` replacing the file_name with the name you'd like to call your directory. For example, if I wanted to create a new index.html file, I'd type `touch index.html` 

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
