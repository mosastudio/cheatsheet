## Clone with SSH, GitHub

* [Connecting to GitHub with SSH](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)
  * Concepts
  * [Generating a new SSH key and adding it to the ssh-agent](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
  * [Adding a new SSH key to your GitHub account](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
  
```
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

$ pbcopy < ~/.ssh/id_rsa.pub

# GitHub -> Profile -> Settings -> SSH and GPG keys -> New SSH Key

$ git clone git@github.com:{username}/{repository}.git
```

## Revert a remote commit

* [Ref](https://gist.github.com/gunjanpatel/18f9e4d1eb609597c50c2118e416e6a6)
* Create a new commit, undo everything. (the bad commit will be still there)
```sh
$ git revert {commit_id}'
```
* Delete the last commit
```sh
$ git reset HEAD^ --hard    # reset the branch to the parent of the current commit
$ git push origin -f        # force-push it to the remote.
```

## diff, apply

```sh
$ git diff > ~/xxxx.diff
$ git apply ~/xxxx.diff
```

## .gitkeep

* [Ref](https://stackoverflow.com/questions/7229885/what-are-the-differences-between-gitignore-and-gitkeep)
