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