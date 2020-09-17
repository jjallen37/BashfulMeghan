# Bash Lesson

1. Intro
2. iTerm2 and VsCode!
3. Terminal Basics
5. Git


## Tools
- iTerm2 - Terminal, but with tabs and nifty stuff.  
https://iterm2.com/

- VS Code - A great text/code editor which can display this file well. https://code.visualstudio.com/
  - Open this file in VSCode
  - Press CMD + Shift + P 
  - Type "Markdown"
  - Select "Markdown: Open Preview to the side"
  - This file will show up prety on the right and refresh as you type. It should look basically the same as the GitHub page.
  - For more information on Markdown files (https://www.markdownguide.org/)


## Terminal Basics

- Q: What is a terminal?   
  - A: Underneath all of the stuff you see on your computer (your desktop + background, apps you open, your wifi menu, etc) at it's core your computer is really just a filesystem + commands.

Think of commands as being like a java method. It has a name, parameters (sometimes), and it does something. For example:
```
            Name      Parameter      Action
public void PrintText(String text) { System.out.println(text); }

// Called like this
PrintText("Hello, World"); // Output: Hello, World
```

The command line is essentially a simplified version of that. It is an named action that you execute. A command line version might look like this.

```
> PrintText "Hello, World"
Hello, World // Output in command prompt
```

Everything you will ever type in the terminal will be in this format.
```
<command_name> <optional command parameters>
```

### Moving Around

```
# Navigate to a folder
> cd <path>

# Navigate to the root folder (Your hard drive)
> cd /

# Navigate to the home folder 
> cd ~ 

# "~" => /Users/jallen
# Shorthand for this
> cd /Users/jallen

# Navigate up a directory
# That "../" means "up a folder
# That "../../" means "up two folders"
> cd ../
```

### Where Am I?

```
# Show me where I am (print working directory)
> pwd
/Users/jallen/Downloads/homework/keep_out

# In Mac, open the current folder in Finder
# That "." means "right here where I am"
> open .
*opens folder in finder*

# Show me the files and folders in the folder I'm in
> ls 
Dwayne.jpg Johnson/ TheRock.mp4 
```
 
So, thats actually pretty much it. 
- `cd` to move around, 
- `ls` to show files
- `pwd` to show where you are
- `open .` to change to finder and work like a normal person


### Wait! I don't know command X! (ex. "brew", "cd") 
The "man" command, the most sexist command in UNIX. Freaking manuals. Use this to get documentation on a command.
```
man <cmd>
```

Try typing:
```
man git 
```

## Git

"git" is a fancy way to save folders with history. Truthfully, plenty of developers don't bother to use git from the terminal. In this section we'll do it once to get the vocabulary down, then in the future I suggest using a program like SourceTree. Steps 4-8 would be easier. 

There are several tutorials on git that are better than this one, so I won't go too deep into how it works. Instead we will go through a typical work flow by having you edit this file and then upload a change to this project.

1. Clone this project. Like, the one this file is in. We're going to get meta with this.   
```git clone https://github.com/jjallen37/BashfulMeghan.git```  

Then go into it

```cd BashfulMeghan```  

2. Make your own branch.  
`git checkout -b typo_fix`

3. Open this file and correct this sentence:
> Meghan's least favorite song is Celebration by Kool & The Gang.

4. Check on your repo. (Easy in SourceTree)  
`git status`   
This will show you which files you have altered. It should show just this file.

5. See your changes. 
`git diff`  
This will show the changes you made

6. Prepare your file for saving by putting it in "staging".  
`git add readme.md`  

7. For sanity, verify you added the file.  
`git status`
This will show the same thing as before but will indicate your file is ready to save

8. Commit your change.  
`git commit -m "Your commit message"  


Nick Cannon wasn't here


9. Push your change to the remote repository (GitHub).  
`git push origin/typo_fix`

10. Go to GitHub and create a Merge Request

11. Get it merged.

12. Go back to the master branch.  
`git checkout master`

13. Pull the latest changes from GitHub.  
`git pull` or  
`git pull origin master`


