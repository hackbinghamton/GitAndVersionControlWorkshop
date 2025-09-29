# Using Git Forges
As useful as version control is, we often want to share our code with others, or just store it in a safe place. A *forge* is a service to do exactly that. Many forges, even those based on Git, offer many more powerful features, like pull requests and issue management. Right now, we're just going to see how they're used. The choice of forge is yours (you might even host your own!), but we'll start with GitHub.

## Exercise
First, we'll need an account. Go to github.com and sign up for an account if you haven't already.

Once you have your account, log in to github.com. Let's create a new repository!
1. On your main page, click the `new` button
2. Fill out the details as you see fit. For the moment, let's create a public repository (careful what you put on the internet, kids!).
3. Now, use your terminal to navigate to a folder of your choice.
4. Run `git clone https://github.com/<your-username>/<your-repository>` to clone your own repository!

### Authentication
To push changes to your GitHub account, you'll need some sort of authentication to prove your identity. You have two options: one easier, one more standard.

Once you've chosen and set up one, try making a *private* repository and cloning it. Ask a friend to try as well—if all has gone well, you should be the only one with access!
#### using the github command line tool
GitHub has their own software package that you can use to authenticate—it ties into Git and whenever you try to do something restricted, it checks your credentials. This is generally the easier option, but requires another package.

You can install it as follows:
- Windows: `winget install --id GitHub.cli`
- MacOS (with Homebrew): `brew install gh`
- Linux: see [GitHub's documentation](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)

Once installed, run `gh auth login` to authenticate.
#### using ssh-keys
SSH keys are commonly used to log in to remote computers, but you can also use them with GitHub and other forges.

1. First, run `ssh-keygen` (be careful not to overwrite your existing keys if you have any!!). The default options should be fine on most devices.
2. Now, navigate to `~/.ssh`. The previous command should have produced two files, one with a `.pub` suffix, for *public*. Open this file.
3. On github.com, open your account settings (click on your profile picture).
4. Navigate to Access→SSH and GPG keys
5. Click `New SSH key`
6. Give your key a title (probably the name or type of your device). Make sure it is set to be an *Authentication Key*.
7. Now copy the content from your `.pub` file into the Key box
8. Click `Add SSH Key`

When you want to use a GitHub repository with ssh authentication, your commands will look a little different. Instead of using `https://github.com`, you will write `ssh://git@github.com`. The `ssh` part tells Git you want to communicate using the SSH protocol, and the `git@` part tells GitHub you are trying to access a git repository.

### Pushing and Pulling
Now that you've authenticated with GitHub, run `git clone` to clone your repository, as we've done before.
Let's make some changes:
1. Add a new file or edit an existing one. Make sure your changes are saved.
2. Use `git status`, `git add`, and `git commit -m "<your-message>"` to commit your changes to your local repository.
3. Now run `git pull`. You should see that your *upstream* repository—the one on GitHub—is *behind* your local one!
4. Run `git push`. If you have correctly authenticated and there are no conflicts, your changes should now be uploaded. Check them on github.com!
