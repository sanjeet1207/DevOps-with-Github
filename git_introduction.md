- To make git know who is committing

- `git config --global user.name "Sanjeet"`
- `git config --global user.email sanjeetk1207@gmail.com`

After successful execution of above steps, Git will know who the user is 
we get the details using ` git config --list` 

user.name = "Sanjeet"
user.email = "sanjeetk1207@gmail.com" 

There will be situation where you just modified a file for correcting spelling.
In this case you may not want to have a separate commit. 

`git commit --amend --no-edit`

Let consider a situation where you deleted content of a file and you also committed it. 
And now you want to get the file with content that it had previously.
let's say removed the content of index.html
`git reset --hard HEAD^`
`git checkout index.html`
`git checkout -- index.html`

To revert back the exact change that we did in the last commit.

`git revert --no-edit HEAD`



To revert to a specific commit that we did in the past.
`git checkout 0b5f1ff .`

Terminology
- Working tree
- Repository or repo
- Hash
- Object
    - blob object
    - tree object
    - commit object
    - tag object
- Commit
- Branch
- Remote
- Commands, subcommands and options
    - `git reset --hard`


To check git version
git --version


Git Basic Commands
`git status` displays the state of the working tree.It lets you see which changes are currently being tracked by Git.

`git add` is used to stage changes to prepared for a commit. All changes in files that have been added but not yet committed are sotred in the 'staging area'

`git commit` Committing changes means you put a copy in the repository as new version.

`git log` command allows you to see information about previous commits.

`git help` command is used to get information about all the commands related to git.

Note: Each command come with its own help page.
like    `git commit --help`


use of `-a` command
git commit -a -m "message of commit"
The `-a` option adds all the files you modified since your last commit.It won't add new files.


`git diff` command shows all the changes that haven't been staged.(added to git Index)

To compare the working tree with last commit. Use
`git diff HEAD`

`git log --oneline` gives more concise listing of the log

`git log -nX` where X is integer 
X = 1 corresponds to last commit
X = 2 corresponds to previous of last commit


`git commit --amend --no-edit`  the --no-edit option tells the Git to make the change without changing the commit message.
We can use `--amend` option to edit a commit message,to add a files that were accidentally left out of the commit or remove files that were added by mistake.

To recover deleted files `git checkout`
this command updates files in the working tree to match the version in the index or in the specified tree.
`git checkout -- <filename>` by default it get file from the index.
The `--`  in the argument list servers to separate the commit from the list of file paths. 

`checkout` is also used to switch branch.

Recover files: git reset
`rm index.html`
`git reset HEAD index.html`
`git checkout -- index.html`


revert a commit
After you have committed the changes, you need to use a different strategy to undo them. In this case we use `git revert` to revert to our previous commit.It works by making another commit that cancels out the first commit.


### Collaborate with Git
- Clone a repository
- push changes to a remote repository
- stash changes
- pull changes from other users to update a repository

Clone a repository
`git clone` command is used to clone/copy a repository.
It accepts SSH path
    git clone git@example.com:alice/Cats

Remote repositories (git pull)
When we clone a repository, it creates a reference to the original repo that's called a remote using the name `origin`. It sets up the cloned repo so that the cloned repo will pull from, or retrieve data from, the remote repository. 
`git pull` command is very efficient because it copies only new commits and objects and then it checks them into your working tree.

Create pull requests (git request-pull)
We submit a pull request to ask you to pull their changes into the main code base.
`git request-pull -p origin/main .`

main branch on the origin remote is referred as origin/main
























#### Branching and merging in Git
- Learn how branches work in Git
- Create new branches and switch between branches
- Merge branches together
- Learn basic techniques for resolving merge conflicts


