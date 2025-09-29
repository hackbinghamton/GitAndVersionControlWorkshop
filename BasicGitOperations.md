# Basic Git Operations
Now that you have Git installed, lets learn how it works!
## Prerequisites
You'll need to know how to open a terminal and use a couple commands:
- `ls` (`dir` on Windows) will list the files and folders in your current directory
- `cd` will change your current directory
    - Use `cd ..` to navigate "up" one level
- `mkdir` will make a new folder
## Operations
`git init`: Creates a new git repository in your current folder
`git clone <repository> [<directory>]`: Copies the repository from `<repository>`. If you pass a second argument `[<directory>]`, your new version will be created in that folder.
`git status`: Lists information about any git repositories in your current folder (or in a parent folder).
`git add <file>`: Takes a file (or directory), and puts any changes to that file into "staging". Staging stores your changes separately, but does not make them part of the permanent record.
`git reset [<file>]`: removes all changes from staging, or removes a specific file from staging.
`git commit [-m <message>]`: Commits any changes in staging to a permanent record. If you don't include a message as your flag, Git will automatically open your default text editor so you can write one.
## Exercise
Let's do a couple experiments to see this in action:
1. First, open up your terminal.
2. Navigate to a folder of your choice with the `cd` command.
3. Now make a new folder (let's call it `myfolder`) with `mkdir` and `cd` into it.
4. Type `git status` and press enter. What happens?

Git stores its information in a hidden directory `.git`. A folder on its own isn't a git repository, but we can put a git repository into a folder. Let's see how:
1. Run `git init`
    - You might get a hint about the default branch name. Don't worry about this for know, but know that `main` is usually preferred.
2. Now run `git status` again. Is the output any different?
3. Run `ls .git/`. What do you see?
4. Lets make some changes! Make a new file in your repository—if you can, use the command line, but you can also use your file explorer and text editor.
5. Run `git status`. You should see your new file there. What heading is it under?

Git only tracks files that you tell it to. All other changes will be ignored—so be careful!
Now let's `add` a file:
1. Run `git add <your-file-name>`, then run `git status`. What changed?
2. Make a change to your file: add "Hello world!" to its content. Now run `git status` again. How many versions of your file are there?
3. Repeat step 1!

At this point, your file is in *staging*: Git is keeping an eye on it, but hasn't committed it to memory. If you add a file by mistake, use `reset` to remove it from staging
1. Run `git reset`, then `git status`

Now let's make our first commit!
1. Use `git add` to add some changes to staging.
2. Now try to run `git commit -m "Hello world!"`. What happens?

Git includes information about each commit's author—this is crucial when managing a repository with multiple contributors! By default, your name and email won't be set. You can choose any name and email—they don't even have to be real—but you will have to choose something. Follow Git's instructions to configure your name and email.

Once that's done, try the last step again! If all goes well, you've just made your first commit!

There's one last thing to cover in this workshop. Let's learn how to use `git clone`:
1. Go back to the folder containing your personal repository.
2. run `git clone https://github.com/hackbinghamton/PythonWorkshop`

You've just made a copy of our Python for Everyone workshop! You can clone repositories from lots of sources—most often a *forge* like GitHub. But remember that the repository you just created *can also be cloned*!
1. Run `git clone myfolder/ mynewfolder`

That wraps it up for the first lesson!
