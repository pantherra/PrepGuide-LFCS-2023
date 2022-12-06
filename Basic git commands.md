Visual git cheatsheet
https://ndpsoftware.com/git-cheatsheet.html#loc=index;
Github training cheatsheet
https://training.github.com/downloads/github-git-cheat-sheet/

##Configure tooling

Configure user information for all local repositories

$ git config --global user.name "[name]"

Sets the name you want attached to your commit transactions

$ git config --global user.email "[email address]"

Sets the email you want attached to your commit transactions

$ git config --global color.ui auto

Enables helpful colorization of command line output

##Create repositories

A new repository can either be created locally, or an existing repository can be cloned. When a repository was initialized locally, 
you have to push it to GitHub afterwards.

$ git init

The git init command turns an existing directory into a new Git repository inside the folder you are running this command. 
After using the git init command, link the local repository to an empty GitHub repository using the following command:

$ git remote add origin [url]

Specifies the remote repository for your local repository. The url points to a repository on GitHub.

$ git clone [url]

Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits

##Make changes

Browse and inspect the evolution of project files

$ git log

Lists version history for the current branch

$ git log --follow [file]

Lists version history for a file, beyond renames (works only for a single file)

$ git diff [first-branch]...[second-branch]

Shows content differences between two branches

$ git show [commit]

Outputs metadata and content changes of the specified commit

$ git add [file]

Snapshots the file in preparation for versioning

$ git commit -m "[descriptive message]"

Records file snapshots permanently in version history

##Synchronize changes

Synchronize your local repository with the remote repository on GitHub.com

$ git fetch

Downloads all history from the remote tracking branches

$ git merge

Combines remote tracking branches into current local branch

$ git push

Uploads all local branch commits to GitHub

$ git pull

Updates your current local working branch with all new commits from the corresponding remote branch on GitHub. git pull is a combination of git fetch and git merge

##Branches

Branches are an important part of working with Git. Any commits you make will be made on the branch you’re currently “checked out” to. Use git status to see which branch that is.

$ git branch [branch-name]

Creates a new branch

$ git switch -c [branch-name]

Switches to the specified branch and updates the working directory

$ git merge [branch]

Combines the specified branch’s history into the current branch. This is usually done in pull requests, but is an important Git operation.

$ git branch -d [branch-name]

Deletes the specified branch

##Redo commits

Erase mistakes and craft replacement history

$ git reset [commit]

Undoes all commits after [commit], preserving changes locally

$ git reset --hard [commit]

Discards all history and changes back to the specified commit
