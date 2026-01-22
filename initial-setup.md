# Workstation-Setup


* Run upgrade:

```
sudo apt-get update
sudo apt-get upgrade
```
* Increase file watcher numbers. This is needed for gulp and Intellij IDEA.
```
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
```

## Install fish

```
sudo apt install fish
```

## Install Google Chrome
Download the 64-bit *.deb file from https://www.google.com/chrome/browser/desktop/. Then install using the the following command:

```
cd ~/Downloads
sudo dpkg -i <deb_file_name>.deb
sudo apt-get install -f
rm <deb_file_name>.deb
```

## Install Better Terminal

```
sudo apt-get install terminator
```

## Install Visual Studio Code

Visual Studio Code is simple IDE with powerful language specific extensions. 
Download the 64-bit *.deb file from [its website](https://code.visualstudio.com/download) and install it.

```
cd ~/Downloads/
sudo dpkg -i <file>.deb
rm <file>.deb
```

## Install Postman
install from App center

## Configure Alias

### Bash

```
nano ~/.bashrc

alias gg="git gui"
alias gs="git status"
alias gm="git fetch origin --prune --tags -f;git checkout master;git pull origin master"
alias gmn="git fetch origin --prune --tags -f;git checkout main;git pull origin main"
alias gp="git add .;git commit -a -s -m wip;git push origin HEAD"
alias g2h="git push origin HEAD"
alias gr="git reset --hard HEAD"
alias gmv="go mod tidy; go mod vendor"
alias ga="git add .;git commit --amend --no-edit -a -s"
alias gcp="git cherry-pick"
alias gch="git checkout"
alias gl="git log --oneline -5"
```

### Fish

```
nano ~/.config/fish/config.fish

alias gg 'git gui'
alias gs 'git status'
alias gm 'git fetch origin --prune --tags -f;git checkout master;git pull origin master'
alias gmn 'git fetch origin --prune --tags -f;git checkout main;git pull origin main'
alias gp 'git add .;git commit -a -s -m wip;git push origin HEAD'
alias g2h 'git push origin HEAD'
alias gr 'git reset --hard HEAD'
alias gmv 'go mod tidy; go mod vendor'
alias ga 'git add .;git commit --amend --no-edit -a -s'
alias gcp 'git cherry-pick'
alias gch 'git checkout'
alias gl 'git log --oneline -5'
