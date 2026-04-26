# dotfiles

Personal dotfiles managed with [GNU Stow](https://www.gnu.org/software/stow/).

## Prerequisites

Install GNU Stow:

```bash
# macOS
brew install stow

# Debian/Ubuntu
sudo apt install stow
```

## Installation

Clone the repo into your home directory:

```bash
git clone https://github.com/hjoliveira/dotfiles.git ~/dotfiles
```

Then navigate into the repo and use `stow` to symlink the packages you want:

```bash
cd ~/dotfiles

# Stow individual packages
stow git
stow zsh

# Or stow everything at once
stow */
```

Stow will create symlinks in `~` pointing to the files inside each package directory. For example, `~/dotfiles/git/.gitconfig` becomes `~/.gitconfig`.

## Removing a package

To remove the symlinks for a package, use the `-D` flag:

```bash
stow -D git
```
