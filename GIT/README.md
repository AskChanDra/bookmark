#GIT Helfull Tips and Tricks

#### Cheatsheet

#### SSH 

- Generating a new SSH key
```bash
ssh-keygen -t rsa -b 4096 -C "email@example.com"
```

- Check the files in your .ssh directory, if they exist
```bash
$ ls -al ~/.ssh
```

- Copy SSH fiels to clipboard
```bash
clip <~/.ssh/id_rsa.pub
```

- Add SSH key to Github Account :`https://github.com/settings/keys`
  - 1. Settings -> SSH - New SSH
  - 2. Add New SSH key copied.
  
  - Adding  SSH key to the ssh-agent :
  ```bash
  ssh-add ~/.ssh/id_rsa
  ```
  
  - Using without Github Desktop e.g. Windows CMD / git bash :
  ```bash
  eval $(ssh-agnet -s)
  ssh-add `/.ssh/id_rsa
  ```  


#### Push a new local branch to a remote Git repository and track it too

- Create a new branch:
```bash
git checkout -b feature_branch_name
```
- Edit, add and commit your files
- Push your branch to the remote repository:

```bash
git push -u origin feature_branch_name
```

#### For Multiple User : Create a SSH config file

```bash
Host bitbucket.org
    HostName bitbucket.org
    User git
    IdentityFile ~/.ssh/id_rsa_bitbucket

Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_github
 ```
 
 #### Testing your SSH connection

```bash
ssh -T git@github.com
```



#### Change GIT Origin URL

```bash
git remote set-url origin https://github.com/USERNAME/REPOSITORY.git
```

#### Untrack Already added files to Repo

1. clean your repo

```bash
git rm -r --cached .
```

2. Re add everything

```bash
git add .
```

3. Commit

```bash
git commit -m ".gitignore fix"
```

- Ref : http://www.codeblocq.com/2016/01/Untrack-files-already-added-to-git-repository-based-on-gitignore/

## Links

- GIT Cheatsheet by [hofmannsven](https://github.com/hofmannsven): https://gist.github.com/hofmannsven/6814451
- Related Setup: https://gist.github.com/hofmannsven/6814278
- Related Pro Tips: https://ochronus.com/git-tips-from-the-trenches/
- Interactive Beginners Tutorial: http://try.github.io/
- Git Cheatsheet by GitHub: https://github.github.com/training-kit/downloads/github-git-cheat-sheet/
