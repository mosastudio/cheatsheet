## bash

* [difference](http://superuser.com/questions/244964/mac-os-x-bashrc-not-working/244990#244990)

```sh
$ .bash_profile
$ .bash_rc
```

### ~/.bash_profile

```sh
[ -r ~/.bashrc ] && source ~/.bashrc
```

### ~/.bash_rc

```sh

# terminal colors, http://stackoverflow.com/questions/1550288/mac-os-x-terminal-colors
export CLICOLOR=1
export LSCOLORS=gxfxbEaEBxxEhEhBaDaCaD

```

## homebrew

* [Homebrew](https://brew.sh/), The missing package manager for macOS
  * ex. mongodb, nvm, wget, ..

```sh
# Install Homebrew
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

$ brea update
$ brew install
```

## make links

```sh
$ ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl
```

## find, grep

```sh
# recursively search all files for a string
# -i    ignore case
# -r    recursive
# -n    show the line number
# -I    Ignore binary files.
$ grep -irn "keyword” .
$ grep -irI "keyword" .

# find a file with a name
$ find . | grep -irn "filename"
$ find . | grep -irI "filename"

# list all the files with certain extensions
$ find . -iregex '.*\(mp4\)'

# Find all files in the current directory and its subdirectories, with the extensions
# Ref. https://askubuntu.com/questions/1110866/find-all-files-in-the-current-directory-and-its-subdirectories-with-the-extensio
$ ls -l -R | grep -i '\.\(jpg\|gif\|png\|jpeg\)$'

# Sort files alphabetically before processing
# Ref. https://askubuntu.com/questions/662339/sort-files-alphabetically-before-processing
$ find . -type f -print0 | sort -z | xargs -0 -L 1
```

## loading

```sh
# top: display information about processes

# sorted by pid (default)
$ top

# sorted by CPU usage
$ top -o cpu

# sorted by memory usage
$ top -o mem



# dump traffic on a network
$ sudo tcpdump



# display free disk space
$ df

```

## display the file

```sh
# display the first 32 bytes
$ od -t x1 -N 32 'filename.ext'
```

## change the default app to open .txt files

* control + click a .txt file
* Get info
* Open with
* select an app
* press "Change All..."

## Sidecar

* [Enable Sidecar on older macOS devices](http://dev.zeppel.eu/luca/SidecarCorePatch)
* Another app with similar func, [Duet](https://apps.apple.com/tw/app/duet-display/id935754064)
