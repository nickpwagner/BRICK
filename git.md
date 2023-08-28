___
# GIT
Links: [[Programming]]
Status: #🌳 
Tags: [[Python]] [[Version Control]] [[Markdown]]
<!--- Created on: 2023.08.26, 14:37 --->

- distributed version control system used for tracking changes in source code
- branching and merging allows multiple people to collaborate on a project simultaneously
- promotes organized development workflows
___

# Configuration

| What             | How                                                |
| ---------------- | -------------------------------------------------- |
| Store name       | `git config --global user.name "<name>"`             |
| Store email      | `git config --global user.email "<email>"`           |
| Read name        | `git config user.name`                             |
| Read email       | `git config user.email`                            |
| Save globally    | `git config --global credential.helper store`      |
| Uncommit command | `git config --global alias.uncommit 'reset HEAD^'` |

# General

| What                                     | How                                                                         |
| ---------------------------------------- |:--------------------------------------------------------------------------- |
| Clone repository                         | `git clone <repo>`                                                          |
| Get local status                         | `git status`                                                                |
| Updates local history                    | `git fetch --all`                                                           |
| Reset branch to origin                   | `git reset --hard origin/<bname>`                                           |
| Stage local files for commit             | `git add <fname>` <br /> `git add .`                                        |
| Remove staged file for commit            | `git rm --cached <fname>` <br /> `git restore --staged <fname>` **v2.23+**  |
| Commit to local branch                   | `git commit -m <message>`                                                   |
| Revert local commit                      | `git uncommit` **after configured**                                         |
| Push changes from local branch to remote | `git push`                                                                  |
| Push changes to remote and as new branch | `git push --set-upstream origin <bname>`                                    |
| Create branch                            | `git checkout -b <bname>`                                                   |
| Select branch                            | `git checkout <bname>` <br /> `git checkout master`                         |
| Delete branch                            | `git branch --delete <bname>`                                               |
| List local branches                      | `git branch`                                                                |
| List remote branches                     | `git branch -r`                                                             |
| Stash local changes (temporarily)        | `git stash save "<sname>"`                                                  |
| List all stashes                         | `git stash list`                                                            |
| Apply specific stash                     | `git stash apply` **if only one** <br /> `stash apply stash@{list_index}`   |
| Apply most recent stash and remove       | `git stash pop`                                                             |
| Remove last stash                        | `git stash drop` **most recent** <br /> `git stash drop stash@{list_index}` |

# Diff

| What                            | How                                                                                                                                                                             |
| ------------------------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Working directory - Last commit | `git diff`                                                                                                                                                                      |
| Staged changes - Last commit    | `git diff --cached`                                                                                                                                                             |
| WD and SC - Last Commit         | `git diff HEAD`                                                                                                                                                                 |
| Commit1 - Commit2               | `git diff <commit1> <commit2>` <br /> ` --name-only ` *only file names* <br /> ` --name-status` *only file names and status* <br /> `--color-words` *word-diff (not line-diff)* |

# Ignore

| What                          | How                                        |
| ----------------------------- | ------------------------------------------ |
| Create                        | `touch .gitignore`                         |
| Write via terminal            | `echo "file" >> .gitignore`                |
| Show hidden files in explorer | `ls -a`                                    |
| Ignore file specifically      | `/path/text.txt`                           |
| Ignore files by name          | `NAME` <br /> `NAME*` *name starting with* |
| Ignore files by folder        | `/dir`                                     |
| Ignore files by type          | `*.txt`                                    |
| Exclude file from ignore      | `!text.txt`                                |

# Special Use Cases

## Merge branch into main
```bash
git checkout master
git merge branchname
git push
```

## Create new repository from local project
```bash
git add .
git commit -m "…"
git remote add origin [copied web address]
git push --set-upstream origin master (--force)
```

## Revert main to previous commit 
### With trace in history
``` bash
# option 1:
git revert --no-commit <commit_id>..HEAD  # reverts everything to <commit_id>
# option 2:
git revert HEAD~3                         # reverts the last three commits
# then:
git commit
```



# References
- [Official Website](https://git-scm.com/)
- [Cheat Sheet](https://ndpsoftware.com/git-cheatsheet.html#loc=local_repo)