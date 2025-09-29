# What is Version Control?
You've likely already encountered a form of version control—in fact, if you've ever used Google Docs, you've already created dozens of stored versions of your documents! Summarily, version control is the practice of managing different *versions* of some sort of *data*. In computer science, we most often deal with *source code*: the files of text containing our high-level programming languages, but the use of version control is much broader. Most *wikis*, like Wikipedia, use version control to manage, compare, and revert changes made to their articles. These days, much text-processing software, like Google Docs, or Microsoft Word comes with version control by default, and authors often use version control to iterate on their manuscripts.
## Advantages of Version Control
- Reverting changes: Suppose you are working on some piece of software. You have it in a functional state, and then you, a friend, or a colleague makes some tweak that inadvertently causes a catastrophic bug. Without version control, you will be relying on you, your friend's, or your colleague's memory of what that breaking change was and where it was found! With a version control system in place, you can simply revert to the last known working version until your bug is fixed.
- Tracking bugs: Suppose a bug is introduced into your program as above, but goes undetected for some time. With version control, you can revisit old versions of your program until you find one that lacks the bug—and then look to see what the next change was!
- Backup: Though not necessarily a part of version control, many version control systems include or offer some sort of backup, so that you can recover your files even if your device is lost or damaged.
- Collaboration: On a large project with multiple contributors, you might want to have two people working on the same software at roughly the same time. Without version control, each contributor would make their own changes—but how, then, would you combine them? If both contributors changed different parts of the same file, whose file should be kept? Version control allows for *merging* different *branches* of the same project.

## Version Control Software
Version Control Software is not software that *uses* version control, but software that *does* version control—and by far the most common VCS is Git. Git is free and open source, and is used for countless projects, from academic research to the Linux kernel to countless software products.

There is other VCS, including proprietary software such as Azure DevOps or Perforce as well as competing open-source tools like Mercurial and Pijul, though none are as dominant as Git.
## Exercise
First read [this list](https://en.wikipedia.org/wiki/Version_control#Common_terminology). Don't worry, you don't need to know all of them!
Try to answer the following questions as best you can.
1. What is a *repository*?
2. When you *pull* a set of changes, which direction do they go?
3. Is *pulling* different from *cloning*?
