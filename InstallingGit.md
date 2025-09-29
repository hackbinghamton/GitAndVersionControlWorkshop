# Installing Git
We'll now look at how to install Git on your device. Git is most versatile on the command line, so we'll be using our terminals.
## Prerequisites
- A Mac, Windows, or Linux device (preferred)
- A terminal
- Familiarity with basic command-line operations like `ls` and `cd` (preferred)
## Windows
There are a few ways to install Git on Windows, and the best will depend on your use case. Here we use the most Unix-like method, using the Windows Package Manager.

First, check if you already have the Windows Package Manager:
1. Open Powershell or Windows Terminal
2. type `winget --version`. If this works, you can skip the next step! If you get an error, you need to install the Package Manager.

Install the Windows Package Manager:
1. Go to the Microsoft Store
2. Search and install App Installer

Now we can use Windows Package Manager to install Git:
1. Open Powershell or Windows Terminal
2. type `winget install -e --id Git.Git`
3. Open a new shell (or close and re-open your current one) and type `git --version` to confirm that everything worked!

## MacOS
First, check if you already have Git:
1. First open Terminal
2. type `git --version`. If the executable is not found, you still need to install Git.

The most Unix-like way to install Git is to use the Homebrew package manager:
1. Go to https://brew.sh/
2. Open Terminal
3. Copy the line from Brew into your Terminal window and press enter

Now that you have Homebrew, use it to install git:
1. open a new shell in Terminal
2. type `brew install git`
3. Open a new shell (or close and re-open your current one) and type `git --version` to confirm that everything worked!

## Linux
How you will install git depends on your *distribution*.

For Debian-based distros like Ubuntu and Pop!\_OS:
1. Open a terminal window
2. type `sudo apt install git-all` and press enter
3. Open a new shell (or close and re-open your current one) and type `git --version` to confirm that everything worked!

For distributions that use RPMs, like Fedora and RHEL:
1. Open a terminal window
2. Type `sudo dnf install git-all` and press enter.
3. Open a new shell (or close and re-open your current one) and type `git --version` to confirm that everything worked!
