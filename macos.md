## terminal

* Change the theme
  * Preferences -> Profiles -> Pro
  * Set as 'Default'

* Change the default login shell
  * Preferences -> General -> Shells open with
    * /bin/bash
    * /bin/zsh

* the terminal shell

```sh
$ echo $SHELL
```

## zsh

* zsh

```sh
$ .zshrc
```

## bash

* [difference](http://superuser.com/questions/244964/mac-os-x-bashrc-not-working/244990#244990)

```sh
$ .bash_profile
$ .bash_rc
```

* ~/.bash_profile

```sh
[ -r ~/.bashrc ] && source ~/.bashrc
```

* ~/.bash_rc

```sh

# terminal colors, http://stackoverflow.com/questions/1550288/mac-os-x-terminal-colors
export CLICOLOR=1
export LSCOLORS=gxfxbEaEBxxEhEhBaDaCaD

```

## System Preferences

* Keyboard
  * Shortcuts -> Spotlight -> Disable "Show Spotlight Search"

## Bluetooth Devices

* If the keyboard / mouse is lagging
  * https://www.macmeicloud.com/blog/2021/2/6/wireless-keyboard-lagging-on-your-mac-try-these-steps
  * hold the *Shift* + *Option* Button on your keyboard and click the Bluetooth icon.

## homebrew

* [Homebrew](https://brew.sh/), The missing package manager for macOS
  * ex. mongodb, nvm, wget, ..

```sh
# Install Homebrew
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

$ brew update
$ brew install
```

## Sublime 3

* make links

```sh
$ ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl
```

* package, XML
  * Command + Shift + P
  * type "Package Control: Install Package", then Enter
  * type "Indent XML", then Enter

* package, JSON
  * Command + Shift + P
  * type "Package Control: Install Package", then Enter
  * type "Pretty JSON", then Enter

* To Use, Selection -> Format
  * Auto Indent (Command K, Command F)
  * Indent XML
  * Indent JSon

## rename several files

[Ref](https://stackoverflow.com/questions/4787413/)

```sh
for f in * ; do mv -- "$f" "PRE_$f" ; done
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

## > /dev/null 2>&1

* [Ref](https://www.itread01.com/content/1545454986.html)

```sh
$ > /dev/null 2>&1
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

## display the file (binary)

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
