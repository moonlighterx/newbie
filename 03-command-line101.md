# Command Line 101

Before we start programming, you need to be comfortable finding files and folders on your computer (as mentioned in Computer Basics 101).   Most people are usually fine finding files and folders the normal way, using the Start Bar then searching for the Home directory and clicking around until they find their Programming folder.

Sometimes you'll hear programmers call this "normal" way of finding files and folders, the "graphical user interface" way of finding things, aka "GUI way".  

In the world of programming however, most programmers do things the "Terminal" or "Command Line" way.  

Rather than using your Start bar or Dock to look for files and folders with a mouse, you will interface with a simple application called a terminal, shell or command prompt. (For simplicity we'll call this application a command line or shell).

The command line usually looks like a rectangular sized window that often has black and white colors (or black and green for people who love the movie The Matrix).  You can customize the colors if you wish by opening up the preferences (we'll talk about this later).

## Your First Mission

Locate the Command Line application on your computer.  For Windows, go to Start and look for `Command Prompt`.   For Mac, look for the Application under Applications > Utilities > `Terminal.app`.  For Linux, you can also look through your Start Bar and find a Terminal or Command Prompt in your Utilities folder.

### Good So Far?

When I first opened the Terminal app on my boss' Mac, it was all white with gray small font.  He looked visually displeased by it, and even more displeased when I told him that he might need to use it to do some web development for a project we were working on together.  He gave me a look of "No thanks" and told me to instead do the project (he no longer wanted to work on it despite knowing how to do some web development).

I realize I can teach you this thing later in the course, but after a lot of careful consideration, I think you would be at an EXTREME disadvantage if we didn't learn command line now.  The reason is that modern web development has so many workflows that start with the command line.  In my boss' time (and even my early days of web development), we could just write everything out into a simple HTML file and update our websites by dragging and dropping the file to the server; however nowadays that is no longer the case with most businesses.   Sure a lot of small businesses still manually update their websites through drag and drop, and that can work for a very small website -- but if you remember -- programming is all about efficiency.   We want to build things for scale and in the case of web development, build websites that can manage themselves.  

### What Is The Command Line?

Glad to see you are still with me.  

The command line is an application that lets you access all your files and folders by just typing keyboard commands.  You no longer see any pretty graphics, rather after each command, the command line drops you wherever you want to go, and you need to type further commands to navigate.

So for example, let's say I wanted to access my `Home` folder and see what was inside.  I could type the following commands with my Mac:

```
cd /Users/vijay/
ls
```

This would take me to the folder at "Root drive" > "Users" > "vijay".  The `ls` command would list all the files and folders that were inside.

If you are on Windows, you could use the following commands (replace YourName with your folder name):

```
cd C:\Users\YourName
dir
```

You'll notice that Windows uses `\` backslashes, while Mac/Linux use `/` forward slashes to separate folders.  Additionally on Windows we need to type `C:` drive or whatever drive name first before we can get to the next folder.  Mac and Linux just start with `/`.  This is because in Mac and Linux, the top drive or `C:` drive is just called the "root directory", so there is no need to name it.   Finally, in Mac and Linux, we use `ls` to list out items, while Windows tells us to use `dir` (`ls`) doesn't work.

### Why So Many Differences Between Windows and Mac?

In a word, competition.  For a long time, both these companies wanted to do things their own way and lock customers down into proprietary workflows.  However, thankfully due to open source, we were able to escape proprietary workflows, thanks to Linux, which eventually Apple began to adopt as well into the operating system OSX.   Microsoft dragged its feet for years before finally embracing the Linux standard as well.  Sometimes you'll hear Linux standard referred to as UNIX standard, since Linux was coded by Linus Torvalds as a way to have a free version of UNIX which was owned by AT&T at the time.  Technically all the commands we use to navigate a computer in the Linux way are based off the old way of doing it in a UNIX system.

The Linux standard of typing commands like `ls` and using `/` forward-slashes has now become the de-facto way to work with files and folders, especially when doing programming and web development.   Microsoft realized this and so now they support Linux commands too, if you prefer them.

For our course, we are going to use the Linux/UNIX standard to work through our files and folders.  If you are on Windows, you can be sure your machine supports this standard by downloading and installing an app called **Git SCM**.  You will want to also want to make sure you enable Unix Style Commands for Command Prompt, so that you can work from Command Prompt with the same commands we use.  (Otherwise you'll have to use another app called Git Bash which tends to be less useful).

### Now That We Are All On The Same Page

Let's finish up this chapter by introducing some more commands.

`ls` - List all files and folders in my present folder (directory)
`cd` - Change directory (by itself returns us to root folder)
`cd /Users/<homefolder>` - Whenever you see `<>`, replace that with your file/folder.  Here we are changing directory to the home folder under the path/address `/Users/<homefolder>`
`cd ..` - Go back one folder 
`pwd` - Show me the present working directory (folder I'm in)
`mkdir <myFolder>` - Make a directory called `myFolder` (Again any name you want).
`touch <myFile>.<extension>` - Create a file called `myFile.ext` (`myFile.txt`).

We'll learn more commands with time, but for now these are the basics.  At this point you should be able to navigate a little bit between files and folders on your computer and see what's inside.  You can also make directories and new files without having to leave the command line, which you might note is useful -- as you get skilled, you can make new files and folders just through this app, rather than do it manually with your mouse and keyboard.   You'll also be able to delete files and folders just as fast.  

Eventually you'll write commands in **script** files that do a lot of this "grunt work" even faster, so you can just hit one command in your command line and let your computer do the manual labor of creating a new folder and all the necessary project files needed to create and launch a simple website boilerplate in seconds.  

Combining what we learn here with another app called Git (used for tracking a web project), you'll have the power to create new web projects fast, make changes, keep track of changes made, approve changes then later send entire websites to be cloned on other computers (called servers) that host your website in matter of minutes.   It's really fascinating stuff, and the more you get better with this workflow, the easier you'll find it is to work on websites.   

However, before we do all that, we have enough knowledge to now begin writing our first lines of code.  Let's get programming!






