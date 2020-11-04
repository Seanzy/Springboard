# Springboard

#
Practicing with git

First clone the repo from website by copying the link of the repo and typing into command line: 
git clone https://github.com/Seanzy/Springboard.git

This will download the repo folder to your local computer in the directory that you typed the command in. 

Then change directory into that newly downloaded repo, in this case, the folder is named "Springboard".

Then modify a file inside, such as README.md and save. Now type:
git add readme.md or git add . to add everything

Then type git commit -m "commit message", with an appropriate message of your own

git push

Learned git diff to compare files

11/3/20
To compare the state of your files with those in the staging area, you can use git diff -r HEAD. The -r flag means "compare to a particular revision", and HEAD is a shortcut meaning "the most recent commit".

You can restrict the results to a single file or directory using git diff -r HEAD path/to/file, where the path to the file is relative to where you are (for example, the path from the root directory of the repository).

We will explore other uses of -r and HEAD in the next chapter.

Git log for history of a file

git show <first 6 digits of hash>

git annotate <file>

git show with a commit ID shows the changes made in a particular commit. To see the changes between two commits, you can use git diff ID1..ID2, where ID1 and ID2 identify the two commits you're interested in, and the connector .. is a pair of dots. For example, git diff abc123..def456 shows the differences between the commits abc123 and def456, while git diff HEAD~1..HEAD~3 shows the differences between the state of the repository one commit in the past and its state three commits in the past.


Git can help you clean up files that you have told it you don't want. The command git clean -n will show you a list of files that are in the repository, but whose history Git is not currently tracking. A similar command git clean -f will then delete those files.

Use this command carefully: git clean only works on untracked files, so by definition, their history has not been saved. If you delete them with git clean -f, they're gone for good.

#
How can I see how Git is configured?
Like most complex pieces of software, Git allows you to change its default settings. To see what the settings are, you can use the command git config --list with one of three additional options:

--system: settings for every user on this computer.
--global: settings for every one of your projects.
--local: settings for one specific project.
Each level overrides the one above it, so local settings (per-project) take precedence over global settings (per-user), which in turn take precedence over system settings (for all users on the computer).

will this change get deleted? whoa yes it deleted everything after the last commit. 

