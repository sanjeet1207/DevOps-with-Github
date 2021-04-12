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


To revert back the exact change that we did in the last commit.

`git revert --no-edit HEAD`