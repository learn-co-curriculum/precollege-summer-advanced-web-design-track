## Unit 1: Command Line - Lecture Notes

### SWBATs

Objective: Students will be able to navigate their system’s file structure using the CLI (command line interface) in terminal.

#### CLI
* Understand and explain what a terminal is and why we use it
* Navigate through directories using relative and absolute paths
* Use the cd command to move up and down directories
* Use the `ls` keyword to list items in a directory
* Remove a file and a directory by using `rm` and `rm -rf` keywords
* Move files and directories using the `mv` command


### Motivation / Why Should You Care?
Back in the day (the 1980s!), computers only had a terminal to control them. Later on, Graphical User Interfaces (GUIs) were created to make computers more accessible (like for your computer-illiterate grandparents). Developers continue to use the terminal instead of the GUI because it speeds up development and allows for more granular control.

### Lesson Plan
***Any students that have done this lesson before should do the advanced [CLI Bash Scripting Lab](https://github.com/learn-co-curriculum/hs-advanced-cli) ***

You're going to learn about the command line by planning for a trip. 
+ Open your terminal. You’ll see a tilde: `~`. This means you’re in your user's home directory.
+ Enter `pwd`. Explain `pwd` means print working directory.
+ Let’s change directories. First check what directories are within the directory where you are standing by using `ls`.
+ Show students how to change directories by using the `cd <directory-name>` command. Change to `desktop` directory.
+ Students `mkdir development`.
+ Show students how to make a new directory in `development` called `trip`. Check and see that the directory was made by using `ls`.
+ Show students how to...
  + create directories for countries within the `trip` directory.
  + create directories for cities within the countries.
  + create text files for landmarks you want to visit in the cities directories by using `touch`. 
  + open the file in your text editor and add information about the landmarks.
  + remove a file that they longer want using `rm`.
  + remove an entire directory using `rm -rf`.
+ Accidentally place a file in the wrong directory, then show students how to move it with `mv`.
+ Students practice moving up the tree using `cd ..`.
+ Important: directories only know what’s directly inside of them.
+ Show students how to write out the relative path to the cities from the trip directory.
+ Show students how to write out the absolute path to different files and directories.
+ Interactive Practice - have students...
  + use `cd  ..` to move to the trip directory.
  + create one new country directory.
  + create two new city directories inside the new country directory.
  + create 3 things to see or do in each city.
  + on your whiteboard, draw out the tree for each directory and file inside the trip directory.

### Conclusion / So What?
+ As we learn to build complicated applications, being able to swiftly navigate your computer using the command line will make your life much easier. The command line will be important not just for navigation, but you'll also use it to do things like boot the local server for your web apps, write scripts to automate tasks, and execute other important functions on your computer.

### Hints and Hurdles
+ Navigating your computer from the command line is a lot about muscle memory. It's important that students get a lot of repetition in with these commands.
+ In [Lab: Find The Missing Pets]( https://github.com/learn-co-curriculum/find-missing-pet), instructor should complete one or two examples before releasing students.

### Additional Media
+ It might be fun for the class to play around with these [CLI easter eggs](https://github.com/learn-co-curriculum/hs-cli-cultural-piece).
