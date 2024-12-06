# dotfiles
Using the methodology from the following article on how to manage dotfiles using the a 'bare' git repository. [Storing dotfiles with Git - This is the way](https://web.archive.org/web/20240307132655/https://engineeringwith.kalkayan.com/series/developer-experience/storing-dotfiles-with-git-this-is-the-way/).

## Requirements
For use of alacritty:
- Must have "JetBrains Mono Nerd Font" installed.

**These are currently intended for a Manjaro Linux system. Use caution if you are not using this distribution.**

## Setup
The following script will clone and source the dotfiles. Some applications may need to be reopened to take effect.
```bash
git clone --bare https://github.com/nicholasss/dotfiles.git ~/.dotfiles && source ~/.bashrc
```
In order to work with the dotfiles from the home directory, the following alias will need to be used. I have shortened the alias from the original `dotfiles` to to `dfs`.
```bash
alias dfs="/usr/bin/git --git-dir=$HOME/.dotfiles --work-tree=$HOME" 
```
Lastly, you will want to stop showing untracked files with the following command.
```bash
dfs config status.showUntrackedFiles no
```

If the files are not showing up, and you are not afraid of messing up your configuration, you can reset the git repo to the current HEAD.
```bash
dfs reset --hard HEAD
```
