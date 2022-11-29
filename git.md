# Git Interview Questions and Answers

## What is difference between Git vs SVN?  
The main point in Git vs SVN debate boils down to this: Git is a distributed version control system (DVCS), whereas SVN is a centralized version control system.

## What's the difference between a pull request and a branch?
* A branch is just a separate version of the code.
* A pull request is when someone take the repository, makes their own branch, does some changes, then tries to merge that branch in (put their changes in the other person's code repository).

##  What is the difference between git pull and git fetch?
In the simplest terms, git pull does a git fetch followed by a git merge.
* When you use pull, Git tries to automatically do your work for you. It is context sensitive, so Git will merge any pulled commits into the branch you are currently working in. pull automatically merges the commits without letting you review them first. If you don’t closely manage your branches, you may run into frequent conflicts.
* When you fetch, Git gathers any commits from the target branch that do not exist in your current branch and stores them in your local repository. However, it does not merge them with your current branch. This is particularly useful if you need to keep your repository up to date, but are working on something that might break if you update your files. To integrate the commits into your master branch, you use merge.

## What is Git fork? What is difference between fork, branch and clone?
* A fork is a remote, server-side copy of a repository, distinct from the original. A fork isn't a Git concept really, it's more a political/social idea.
* A clone is not a fork; a clone is a local copy of some remote repository. When you clone, you are actually copying the entire source repository, including all the history and branches.
* A branch is a mechanism to handle the changes within a single repository in order to eventually merge them with the rest of code. A branch is something that is within a repository. Conceptually, it represents a thread of development.
## What benefits come with using GIT?
* Data replication and redundancy are both possible.
* It is a service with high availability.
* There can only be one Git directory per repository.
* Excellent network and disc performance are achieved.
* On any project, collaboration is very simple.
## What’s the difference between Git and GitHub?
Git | GitHub

Git is a software | GitHub is a service

Git can be installed locally on the system | GitHub is hosted on the web

Provides a desktop interface called git GUI | Provides a desktop interface called GitHub Desktop.

It does not support user management features | Provides built-in user management

## How is Git different from Subversion (SVN)?
GIT | SVN

Git is a distributed decentralized version control system | SVN is a centralized version control system.

Git stores content in the form of metadata. | SVN stored data in the form of files.

The master contains the latest stable release. | In SVN, the trunk directory has the latest stable release

The contents of Git are hashed using the SHA-1 hash algorithm. | SVN doesn’t support hashed contents.
## Name a few Git commands with their function.
* Git config - Configure the username and email address
* Git add - Add one or more files to the staging area
* Git diff - View the changes made to the file
* Git init - Initialize an empty Git repository
* Git commit - Commit changes to head but not to the remote repository
## What are the advantages of using Git?
* Faster release cycles
* Easy team collaboration
* Widespread acceptance
* Maintains the integrity of source code
## Difference between git fetch and git pull.
Git Fetch | Git Pull

The Git fetch command only downloads new data from a remote repository. | Git pull updates the current HEAD branch with the latest changes from the remote server.

It does not integrate any of these new data into your working files. | Downloads new data and integrate it with the current working files.

Command - git fetch origin | git fetch --all

Tries to merge remote changes with your local ones. | Command - git pull origin master
## How do you resolve conflicts in Git?
Here are the steps that will help you resolve conflicts in Git:
* Identify the files responsible for the conflicts.
* Implement the desired changes to the files
* Add the files using the git add command.
* The last step is to commit the changes in the file with the help of the git commit command.
## What is the functionality of git ls-tree?
The git ls-tree command is used to list the contents of a tree object.
## What is the process to revert a commit that has already been pushed and made public?
There are two processes through which you can revert a commit:

1. Remove or fix the bad file in a new commit and push it to the remote repository. Then commit it to the remote repository using:

git commit –m “commit message”

2. Create a new commit to undo all the changes that were made in the bad commit. Use the following command:

git revert <commit id>
## What is Git stash?
Let’s say you're a developer and you want to switch branches to work on something else. The issue is you don’t want to make commits in uncompleted work, so you just want to get back to this point later. The solution here is the Git stash.

Git stash takes your modified tracked files and saves it on a stack of unfinished changes that you can reapply at any time. To go back to the work you can use the stash pop.
## What does the git reset --mixed and git merge --abort commands do?
git reset --mixed is used to undo changes made in the working directory and staging area.

git merge --abort helps stop the merge process and return back to the state before the merging began.


## What do you understand about the Staging area in Git?
The Staging Area in Git is when it starts to track and save the changes that occur in files. These saved changes reflect in the .git directory. Staging is an intermediate area that helps to format and review commits before their completion.
## What is Git Bisect and how do you use it?
The Git Bisect command performs a binary search to detect the commit which introduced a bug or regression in the project’s history.

Syntax: git bisect <subcommand> <options>
## How do you find a list of files that has been changed in a particular commit?
The command to get a list of files that has been changed in a particular commit is:

git diff-tree –r {commit hash}

-r flag allows the command to list individual files
commit hash lists all the files that were changed or added in the commit.

## What is the use of the git config command?
The git config command is used to set git configuration values on a global or local level. It alters the configuration options in your git installation. It is generally used to set your Git email, editor, and any aliases you want to use with the git command.

## What is the functionality of git clean command?
The git clean command removes the untracked files from the working directory.

## What is SubGit and why is it used?
SubGit is a tool that is used to migrate SVN to Git. It transforms the SVN repositories to Git and allows you to work on both systems concurrently. It auto-syncs the SVN with Git.

## If you recover a deleted branch, what work is restored?
The files that were stashed and saved in the stashed index can be recovered. The files that were untracked will be lost. Hence, it's always a good idea to stage and commit your work or stash them.
 
## Explain these commands one by one– git status, git log, git diff, git revert <commit>,  git reset <file>.
* Git status - It shows the current status of the working directory and the staging area.
* Git revert<commit> -  It is used for undoing changes to a repository's commit history.
* Git log- It is a key tool for reviewing and reading the history of everything that happens to a repository.
* Git diff- It is a multi-purpose Git command that performs a diff function on Git data sources when executed.
* Git reset<file>- it is used to unstage a file.

## What exactly is tagging in Git?
Tagging enables developers to mark all significant checkpoints as their projects progress.

## What exactly is forking in Git?
It is a repository duplicate and forking allows one to experiment with changes without being concerned about the original project.

## How to change any older commit messages?
You can change the most recent commit message with the ```git commit —amend``` command.

## How to handle huge binary files in Git?
Git LFS is a Git extension for dealing with large and binary files in a separate Git repository.

## Will you make a new commit or amend an existing one?
The git commit —amend command allows you to easily modify the most recent commit.

## What do you mean by branching strategy?
It is employed by a software development team while writing and managing code with a version control system.

## Difference between head, working tree, and index.
They are all names for various branches. Even Though a single git repository can track an arbitrary number of branches, the working tree is only associated with one of them, and HEAD points to that branch.
## What are Git Hooks?
They are scripts that are executed automatically whenever a specific event occurs in a Git repository.
## What is Git stash vs Git stash pop?
Git stash pop removes the (topmost, by default) stash when applied, whereas git stash apply keeps it in the stash list for future use.

## What exactly is git cherry-pick?
A command typically used to move specific commits from one branch of a repository to another.

## State the difference between “git remote” and “got clone”?
“Git remote” allows you to create an entry in the git configuration which specify a URL.

“Git clone” lets you create a new git repository by letting you copy it from the  current URL.

## Difference between “pull request” and “branch”?
“Pull request” is done when you feel like changing the developer’s change to another person's code branch. And “Branch” is just a separate version of code.

## What is a detached head?
Detach head refers to that the currently checked repository is not in the local branc
## What are some of the drawbacks of Git?
One of the main drawbacks is that it can be difficult to learn and use, especially for those who are not familiar with version control systems.
And Git is not always reliable and can sometimes be slow.
## What’s the difference between reverting and resetting?
* Reverting
  * The revert command in Git is used to create a new commit that undoes the changes made in the previous commit. When you use this command, a new history is added to the project; the existing history is not modified.
* Resetting
  * Git reset is a command that is used to undo the local changes that have been made to a Git repository. Git reset operates on the following: commit history, the staging index, and the working directory.

## What is git cherry-pick?

Cherry picking in git means to choose a commit from one branch and apply it onto another.

This is in contrast with other ways such as merge and rebase which normally applies many commits onto a another branch.

Make sure you are on the branch you want apply the commit to. git checkout master Execute the following:

git cherry-pick <commit-hash>
## How to revert previous commit in git?

To revert to a previous commit, ignoring any changes:

git reset — hard HEAD

where HEAD is the last commit in your current branch
## How to rebase master in git? Difference between rebase and merge. How to squash or fixup commits?

Rebasing is the process of moving a branch to a new base commit.

The golden rule of git rebase is to never use it on public branches. … The only way to synchronize the two master branches is to merge them back together, resulting in an extra merge commit and two sets of commits that contain the same changes.

## Branching strategies Pros and Cons — Feature, Release branching, Git flow, Lean Git flow

Pro: By keeping latest deployed version in trunk, small fixes can be rolled out quickly without extensive testing of the latest development version.

Pro: Developers can work more freely in tighter iterations without stepping on eachother’s feet.

Pro: if you have many branches you’ll be pushed to adopt a modern DVCS (my experience is with Mercurial but I hear git or Bazaar are also good) rather than stay with a traditional centralized system (like, say, svn).

Pro: Branches can be used to facilitate ‘what-if’ scenario’s in trying out new code. At the end a decision can be made to merge the new feature or to abandon it.

Con: Having too many branches in the air at the same time and you start forgetting where things where commited, where changes have been made etc.

Con: someone has to manage the branch(es) and keep on top of things. In most teams this falls by the way-side.

## What does a commit object contain?
Commit object contains the following components, you should mention all the three points presented below:

A set of files, representing the state of a project at a given point of time
Reference to parent commit objects
An SHA-1 name, a 40 character string that uniquely identifies the commit object
## How will you know in Git if a branch has already been merged into master?
The answer is pretty direct.

To know if a branch has been merged into master or not you can use the below commands:

git branch --merged – It lists the branches that have been merged into the current branch.
git branch --no-merged – It lists the branches that have not been merged.
##
##



































