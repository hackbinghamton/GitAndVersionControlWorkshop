# Advanced Git Operations
Now that we have some basic version control, let's see what else Git can do...

## Branching
Create or clone a git repository on your device. Run `git status` and take a closer look.
On the first line, you should see `On branch main`. A single git repository can have multiple branches: you might use them for experimental features, refactors of your code, or for different stages of development. Many repositories have a `live` branch and a `testing` branch, so that you can screen risky changes from reaching your audience or clients.

We can use `git branch <branch-name>` to create a new branch, but if you check `git status`, you'll see that you are still `on branch main`. To actually switch to a branch, we use `git checkout <branch-name>`. Combine these operations with `git checkout -b <branch-name>`.

You can make changes and commits on this new branch just as you could before. You can switch back to `main` with `git checkout main`.

If at some point you want to copy the changes from one branch to another, you first `checkout` the branch you want to modify. Then you can run `git merge <source-branch>`.
Try switching back and forth between two branches and making a few commits. Then try to `merge` one with the other. What happens?

Git isn't always able to automatically merge branches—sometimes two or more sets of changes conflict with each other. In that case, Git will prompt you to manually edit the problematic files and keep the changes you want.

## Uploading a repository
Sometimes you'll want to create a repository locally and only later upload it to a forge. Make sure you've authenticated with your forge—the following example uses GitHub
Run `git init` in a local repository.
Then run `git remote add origin https://github.com/<your-username>/<repository-name>`. A *remote* is a repository that is not in a *local* folder.
Now try running `git push`. Unless you've edited your configuration, this won't work. Instead, try `git push --set-upstream origin main`.

## Ignoring files
Often we will have files in our repository that we never want to track: temporary files, swap files, or compiled executable files.
To tell Git to ignore these files, we put their names in a file called `.gitignore` Try it out!

We can also ignore patterns and directories: adding `*.swp` to your `.gitignore` will cause Git to ignore *any* file ending in `swp`, and if you have a directory called `build`, you can add `build` to your ignore list.
