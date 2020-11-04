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