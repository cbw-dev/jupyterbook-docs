(command-line)= 
# Command Line for Newbies

## Introduction to the Command Line

This is for those who have no (or extremely little) experience with the command line.

Using the command line, you can use text commands to interact with your computer's operating system. For us, we will be using it to move around our folders and to [git clone](git-clone) our workshop into our computer, so we can work on it using RStudio!

```{note}
You should be comfortable navigating through your folders when using the Jupyter Book Template
```

### Terminal, Command Prompt and Windows PowerShell

<!-- I DO NOT KNOW HOW EXACTLY ACCURATE MY COMMENTS ON "UNIX-BASED" ARE -->

We can use the command line using certain tools and applications. Terminal is a Unix-based (meaning Linux and macOS computer already have it) application that allows you to access the command line. Similarly, Command Prompt (CMD) and Windows PowerShell give access to the command line on Windows computers. However, Terminal, Command Prompt and Windows PowerShell differ in what commands are accepted. The same commands we give to Terminal may not work in Command Prompt and/or Windows PowerShell.

> Note: Windows PowerShell tends to be more advanced than Command Prompt, and often can accept more commands that are accepted by Terminal than Command Prompt.

### Common Commands (for us)

<!-- Consider making this explanation a video -->

We won't need to know that many commands, but for easy navigation and understanding, here is what you (generally) need:

:::: {.greenbox data-latex=""}
**Note:**

Commands are written below as headers, with an explanation provided beneath.

They follow the format: "[Linux Command] OR "[Windows Command]"
::::

###### pwd OR echo %cd% {.unnumbered}

"pwd" stands for "print working directory". It is a command that works in **Linux** and **Windows PowerShell**. The equivalent in **Command Prompt** is "echo %cd%". For example, below our output is where in my folders the current .Rmd file that makes up this website is:

```{bash}
pwd
```

###### ls OR dir {.unnumbered}

"ls" is a command that works in **Linux** and **Windows PowerShell**. It's short for "list" and outputs all the files and folders in the directory (folder) you are currently in. (Note: this code only shows 4 files to save space!)

```{bash, results='hide'}
ls
```

<!-- to save space, only output the first 4 lines -->

```{bash, echo=FALSE}
ls | head -n 4
```

A similar command in **Command Prompt** is `dir` (short for "directory"), which also outputs the files and folders in your current directory (along with timestamps)!

###### cd {.unnumbered}

"cd" stands for "change directory". The command produces no output, but it allows you to go to a different directory than the one you're currently in. For example,

```{bash}
pwd # recall: pwd tells us where we currently are
cd img # img is a folder in bookdown-docs
echo "now switching directories" # outputs the following string
pwd
```

> **Tip**:<br>Typing "cd" and then hitting the `tab` key will give you the available directories you can go to from where you are, or what you have currently typed in. If there is only one option, hitting `tab` will fill in your command with that option. (This works when typing in any file location into your command line, not only using "cd"). On macOS, the terminal will give you a list if there are multiple options. On Windows, both Command Prompt and Windows Powershell will fill in potential options, and you can hit tab multiple times untill you find your desired file destination.

**File Location Shorthands** When referring to file addresses, there are helpful shorthands! Here's a summary: - `.` = Current Directory - `..` = Parent Directory - `~` = Home Directory

Here's an example (recall, cd produces no output!):

```{bash}
pwd
echo -e # creates a line

echo "Current Directory Example"
cd .
pwd
echo -e

echo "Parent Directory Example"
cd ..
pwd
echo -e

echo "Home Directory Example"
cd ~
pwd
```

###### mkdir {.unnumbered}

"mkdir [directory address]" stands for "make directory". Essentially, mkdir will make an empty directory (folder) at a specified location. For example: `mkdir test` would create a folder named "test" in our current directory. The following commands do the same thing. Note: `mkdir ./test` does the same thing.

###### rmdir {.unnumbered}

"rmdir [directory address]" removes an *empty* directory. For example, `rmdir test` would delete the directory we just made!

###### rmdir -r OR rmdir /s {.unnumbered}

"rmdir -r [directory address]" (Terminal & Windows PowerShell) and "rmdir /s [directory address]" removes a directory recursively, meaning it deletes all the contents of the folder as we all as the folder in itself. Be careful, you can not restore a directory you removed using "rmdir"!

###### Up [⬆] and Down [⬇] Arrows {.unnumbered}

One of the most useful tips for using the command line is to use your up [↑] and down [↓] arrow keys. Using the up [↑] key gives you the previous commands you typed, and the down [↓] arrow returns you to your earlier commands.