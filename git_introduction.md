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