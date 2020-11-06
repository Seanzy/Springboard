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

How can I undo changes to staged files?
At the start of this chapter you saw that git reset will unstage files that you previously staged using git add. By combining git reset with git checkout, you can undo changes to a file that you staged changes to. The syntax is as follows.

git reset HEAD path/to/file
git checkout -- path/to/file
(You may be wondering why there are two commands for re-setting changes. The answer is that unstaging a file and undoing changes are both special cases of more powerful Git operations that you have not yet seen.)

How can I find out where a cloned repository originated?
When you a clone a repository, Git remembers where the original repository was. It does this by storing a remote in the new repository's configuration. A remote is like a browser bookmark with a name and a URL.

If you use an online git repository hosting service like GitHub or Bitbucket, a common task would be that you clone a repository from that site to work locally on your computer. Then the copy on the website is the remote.

If you are in a repository, you can list the names of its remotes using git remote.

If you want more information, you can use git remote -v (for "verbose"), which shows the remote's URLs. Note that "URLs" is plural: it's possible for a remote to have several URLs associated with it for different purposes, though in practice each remote is almost always paired with just one URL.

11/4/20 - 
Doing the git exercises from the https://gitexercises.fracz.com/exercise/master website. 
The commands were written for Linux so I converted to Windows below. The site was kind of confusing because it doesn't clearly tell you how to do the practice exercises. You're supposed to type in the information they request then go into your console / cmd and type in the rest. Here are the windows commands to be typed in:

git clone https://gitexercises.fracz.com/git/exercises.git
cd exercises
git config user.name "Your name here"
git config user.email "Your e-mail here"
configure.sh  
start.sh, not git start

Passing 4 exercises! I love this way of improving! Thank you Springboard for introducing me to this site. I stopped using the Github website to push my changes now! 

11/5/20 - attempted a codewars kata today but had computer issues with too many python processes running in the background. Completed more Springboard work, traded, and worked on my trading programs. Need to get many things automated. 

11/6/20 - Spoke with mentor today. 