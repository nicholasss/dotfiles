# dotfiles
Using the methodology from the following article on how to manage dotfiles using the a 'bare' git repository. [Storing dotfiles with Git - This is the way](https://web.archive.org/web/20240307132655/https://engineeringwith.kalkayan.com/series/developer-experience/storing-dotfiles-with-git-this-is-the-way/).

## Setup
The following script will clone and source the dotfiles. Some applications may need to be reopened to take effect.
```bash
git clone --bare https://github.com/nicholasss/dotfiles.git ~/.dotfiles && source ~/.bashrc
```
