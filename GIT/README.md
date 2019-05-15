#GIT Helfull links

#### Cheatsheet

##### Push a new local branch to a remote Git repository and track it too

- Create a new branch:
```bash
git checkout -b feature_branch_name
```
- Edit, add and commit your files
- Push your branch to the remote repository:

```bash
git push -u origin feature_branch_name
```




###### Change GIT Origin URL

```bash
git remote set-url origin https://github.com/USERNAME/REPOSITORY.git
```

###### Untrack Already added files to Repo

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
