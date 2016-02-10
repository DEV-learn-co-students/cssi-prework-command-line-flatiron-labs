#Terminal Basics

Back in the day (the 1980s!), computers only had a terminal to control them. The terminal is a text-only way to communicate with your computer. Later on, Graphical User Interfaces (GUIs) were created to make computers more accessible and intuitive for those who weren't as computer savvy. Developers continue to use the terminal instead of the GUI because once you get the hang of it, the terminal is quick and provides a lot of features.

##Key Terms
* `Terminal` : A text-based tool that allows you to communicate with your computer. The user types a line of text into a simple prompt, and the computer runs that command. On OS X your terminal is an application appropriately called Terminal. <br>
* `Graphical User Interface` : A graphical display that allows you to communicate with your computer through icons and other visual elements like pointers, folders


##Opening and Docking the Terminal

You will be using the Terminal to access and edit files, move between directories (folders) and complete your labs. Follow the two steps below to open and dock the terminal.
+  Opening- On a Mac, access Spotlight Search by clicking the magnifying glass in the upper right navigation bar or by pressing Command + Space. Then search for terminal and press Enter.
+  Docking - Once the terminal is open, find it's icon in the dock. Right click on the icon, click Options and then Keep in Dock. Now you can access it from the Dock whenever you need it. 


##Terminal Basics
Watch the video below to understand how to use basic terminal commands
<video controls width="100%">
  <source src="//flatiron-videos.s3.amazonaws.com/ironboard/command-line-basics.mp4" type="video/mp4" >
</video>

##Terminal Cheat Sheet
+ ` ~`: user's home directory, on most Macs this will be `Users\username`
+ `.` - current directory
+ `..` - parent directory, the directory that the current directory is contained in
+ `pwd`: print working directory - it tells us where we are.
+ `ls`: check what directories and files are inside the current directory
+ `cd <directory-name>`: change directory
+ `mkdir <directory-name>`: make a new directory.
+ `touch <file-name.extention>`: create a file
+ `rm <file-name>`: remove a file
+ `mv <file to move> <final destination>`: move a file to a new destination. You have to be in the same directory as the file you are moving. Also you have to list the path of directories in order to move the file to the final destination
+ `cd ..` to move up one directory.
+ `cd ../..` to bring you up two parent directories


# Around the World Command Line Practice 

If you think you might want some practice, you can follow the code-along below to use some of the commands you've learned about thus far. 

* Enter `pwd` : This shows your staring point, Users/yourname
* Enter `ls` : check what files and directories are within your current direcotry
* Enter `cd Desktop` : change to the Desktop directory.
* Enter `mkdir around-the-world` : make a new directory with the name "around-the-world". For fun, check out your Mac's desktop - you should see the directory (folder) that you just created
* Enter `cd around-the-world`: change directories into around-the-world (Desktop/around-the-world). This would be the same thing as double-clicking into the folder on your Desktop.
* Enter `mkdir France` : creates a directory called France inside of around-the-world 
* Enter `cd France` : change directories into France (Desktop/around-the-world/France)
* Enter `mkdir Paris` : create a directory called Paris inside of France 
* Enter `cd Paris` : change directories into Paris
* Enter `pwd` : Look to see how the path shows the parent directory and subdirectories from left to right
* Enter `touch eiffel_tower.txt` : to create a text file called eiffel_tower in the Paris directory
* Enter `touch berlin_wall.txt` : to create a text file called berlin_wall in Paris directory
* Enter `touch pyramids.txt` : to create a text file called pyramids in Paris directory
* Enter `ls` : to see the three files you just created, which are all inside of the Paris directory. But only one belongs here!
* Enter `rm berlin_wall.txt` : To remove the berlin_wall file, which doesn't belong in Paris. (Type `ls` to confirm you only have two files left)
* Enter `mv pyramids.txt ~/Desktop/around-the-world` : To move the pyramids text file to the around-the-world directory. The tilde `~` is the home directory.
* Enter `cd ..` to move up the tree of directories. `cd ../..` will bring you up two parent directories. Do this until you are back in the around-the-world directory. You can check this by typing `pwd` and getting something like `/Users/nanselmo/Desktop/around-the-world`


# Challenge:
1. Create a directory called "Egypt" inside the "around-the-world" directory
2. Create a directory called "Cairo" inside the "Egypt" directory
3. Create two new files, sphinx.txt and mummy.txt
4. Delete the mummy.txt file
3. Move "pyramids.txt" into the "Cairo" directory. 


#Tips and tricks:
+ If you start typing a directory name or file name, you can press `Tab` and the command line will automatically fill in the rest of the directory/file name. 
+ If you press `Tab` twice it will show you all of the directories/files inside your current directory.
+ Use the up arrow to access commands you've written before. This will save a lot of time!
+ Navigating your computer from the command line is a lot about muscle memory. The more practice you have the faster you will get!

#Conclusion
As we learn to build complicated applications, being able to swiftly navigate your computer using the command line will make your life much easier. The command line will be important not just for navigation, but you'll also use it to do things like boot the local server for your web apps, write scripts to automate tasks, and execute other important functions on your computer.



