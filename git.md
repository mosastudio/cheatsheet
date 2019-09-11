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
