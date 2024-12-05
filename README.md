# Git

- Version Control System tool that helps to track changes in code. Major uses

- Track the history
- Collaborate

# Git Commands

- init - used to create a new git repo **git init**.
- add : adds new or changed files in your working directory to the git staging area **git add filename**.
- commit : it is the record of the changes **git commit -m "some message"**.
- push : upload local repo content to remote repo **git push origin branchname**.
- clone : clone a repository in local Machine **git clone linktoremoterepository**.
- Origin : default repository name in the remote github.
- **git remote add origin link** -- meaning we are adding new remote repostiory named origin
- **git remote -v** -- to verify which remote repository are we talking about.
- **git branch** -- to check the branch.
  -- **git push -u origin main** -- -u means we are setting the upstream for the project meaning if we are working on a large scale project then once we set upstream we dont have to mention about origin we can simply do **git push**.
- **git checkout branchname** - to navigate to the branchname.
- **git checkout newbranchname** - to create a new branch.
- **git branch -d branchname** - to delete branch.

### Merging Commands

Suppose we created a new branch and added a new feature in that branch and now we want to merge that feature to our main branch then we have following ways to merge:

- firstly, we may compare commits, branches, files and more using **git diff branchname** command.

-- Secondly, we may use github . We create a _PR(Pull Request) : which lets you tell others about the changes you 've pushed to a branch in a repository on a GitHub_.

- When ever we want the changes in our remote repository in local repo we use _git pull origin main_.

- **git pull origin main** : used to fetch and download content from a remote repo and immediately update the local repo to match that content.

### Resolving MergeConflicts

Merge Conflicts is an event that takes place when git is unable to automatically resolve differences in code between two commits._git merge otherbranchname_.

### Undoing Changes

- case 1: staged changes
- _git reset filename_
- case 2: committed changes(for one commit)
- _git reset HEAD~1_
- case 3: for multiple committed changes
- git reset hash
- for removing it from our localrepo _git reset --hard hashvalue_.

### Fork

A fork is a new repository that shares code visibility settings with the original "upstream" repository.
Fork is a rough copy

### Origin vs Upstream

| (Origin)            | (Upstream)                          |
| ------------------- | ----------------------------------- |
| Orign is a remote   | Upstream is a main repository where |
| repository where    | we keep the latest update of the    |
| our code is stored. | original repositorywhich helps in   |
|                     | collaboration and contribution      |

### Pull vs fetch

| (Pull)                 | (Fetch)                           |
| ---------------------- | --------------------------------- |
| When we use the pull   | When we use the fetch command, it |
| command, it downloads  | just downloads the changes from   |
| as well as applies     | the remote repository to your     |
| those changes from the | local repository but doesn't      |
| remote repository to   | apply those changes to your code. |
| your local repository. |                                   |

### Merge vs Rebase

| (Merge)                    | (Rebase)                      |
| -------------------------- | ----------------------------- |
| When we need to apply the  | Rebase moves the changes in a |
| changes of other branches  | branch to the latest commit   |
| to the working branch, we  | point.It changes the order of |
| we use command \*git merge | commit. It merges the history |
| branchname\*.              | into a single timeline.       |
