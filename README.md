# Programming Guide

Help for my first programming experience. Start with [Work to do?](#work-to-do) and use the [Tools](#tools) section when you need a tool for a task.

There's also a [presentation](https://marcvanandel.github.io/programming-guide/) for presenting the [general knowledge](#general-knowledge) below.

If you just want to learn programming, try **[Hedy](https://hedycode.com/)**.
This is a really fun and easy way to get you into learning how to write code.<!-- two spaces at the end are on purpose -->  
_Tip: select your own language if English is not your native language!_


## Table of Contents

This repo contains multiple parts:

- [Knowledge](Knowledge.md)
  - [Basics](Knowledge.md#basics)
  - [Programming Language Characteristics](Knowledge.md#programming-language-characteristics)
- [Tools](#tools)
- [Work to do](#work-to-do)

## Work to do

1. Create your own [GitHub](#github) account
2. Create a new repository: Go to your GitHub profile and select 'New'
   This will be your first program you'll write. Choose a fancy name like 'my-cool-progam'
3. Next step is 'cloning your repo' (repo is short for repository). This will download the online repository in GitHub to your local filesystem  - see [git](#git)
   1. Open the [GitHub Desktop](#git)
   2. Clone your 'my-cool-program' repo into an easy to find location on your system (e.g. C:\projects)
4. Open your files (in your repo) in [VSCode](#vscode) by using the GitHub Desktop button

> // TODO JavaScript, HTML and CSS starters
> 
> [JavaScript introduction video](https://youtu.be/W6NZfCO5SIk)

## General Knowledge

## Tools

What do I need? (use Ctrl+click to open links)

### Git

Tool #1: [git](https://git-scm.com/) for version control of your local files; you'll need this a lot :wink:

This is a very basic tool ... and because we'll be using GitHub as well (see tool #2) we'll use the GitHub Desktop version of git.

- Download the [GitHub Desktop](https://desktop.github.com/) - this is an easy and visual tool to interact with GitHub
- Install with all defaults
- Check out these instruction videos [part 1](https://youtu.be/9GKpbI1siow) and [part 2](https://youtu.be/n-p1RUmdl9M)

### GitHub

Tool #2: [GitHub.com](https://github.com/) for hosting your files online including the version history of all your files. By doing so you also have a backup of all your files _and_ you can share your changes with others. This is also used to publish your software releases.

Create your own [GitHub account](https://github.com/login).

### VSCode

Tool #3: [VSCode](https://code.visualstudio.com/) (or Visual Studio Code)

This is your editor to edit your files. You also will use this for your 'git actions' and synchronization with GitHub

Tip: once you're familiar with the [terminal](#terminal) it will (probably) be possible to open VSCode from the current directory with the `code` command:

```bash
# open current directory in VSCode
code .

# open 'my-cool-program' in VSCode
code my-cool-program
```

### Markdown

Tool #4: [Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

This is a format to create documentation like this guide. Files have `.md` extension (last part of the filename). In GitHub these Markdown files will be shown as webpages with links and formatting like bulletpoints and headers. Knowing this tool will help you document your own journey in developing your applications.

### NodeJS

Tool #5: [NodeJS](https://nodejs.org/en/)

NodeJS is heavily used as the 'build engine' (see [code-build-run](#code-build-run)) and can also be used to run a webserver (see [client-server](#client-server) and more specific [browser-server](#browser-server)).

NodeJS needs to be installed on your local machine and is accessible from a [terminal](#terminal).
Once installed you can check your installation by checking the version currently in use:

```bash
node --version
```

and 

```bash
npm --version
```

`npm` is the Node Package Manager.

### Terminal

This is already available in a few sorts on your machine.

**Windows**

In case you have a Windows machine (developers slang for computer) you'll have a 'Command Prompt' and a 'Windows PowerShell' terminal.

- Hit 'Start' and type 'cmd' to start the 'Command Prompt' - this is 'the old and long time available Windows terminal'
- Hit 'Start' and type 'powershell' to start the 'Windows PowerShell' terminal - this is 'the new and powerful terminal'

**Linux**

Linux is a different OS than Windows and contains a 'Bash' or 'Shell' terminal ... or any of the other and many terminal options available.
For Windows users a Linux environment is available via the [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install), WSL in short.
For most users the [Ubuntu Linux distribution for WSL](https://ubuntu.com/wsl) will be convenient as a WSL environment.
Once installed and available you'll need to install the git and NodeJS tools yourself (but the Linux ecosystem is very helpful in getting this done easily!!)

## Contribution

This repo is edited with [VSCode](#vscode) and uses a [PlantUML plugin](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml) to generate the containing images.
The sources can be found in `src/` and generation is (for now) executed manually on a local machine.
After generation the new images need to be moved to the `img/` folder.
