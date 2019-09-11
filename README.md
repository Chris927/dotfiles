# Dotfiles Attempt

## Goals

- be minimal (and therefore fast), therefore don't use bloated plugin systems /
  frameworks (like oh-my-zsh, ...)
- understand (almost) everything

## Issues

- Currently hard coded file path linking to `subnixr/minimal`'s zshrc setup.

## Prerequisites

Install dependencies via [brew](https://brew.sh/):

```
brew install zsh tmux fasd
```

Under "System Preferences > Users & Groups", change your login shell to `/usr/local/bin/zsh`.

Install iterm2?

Clone this repo (and its dependency) to the currently fixed location:

```
mkdir ~/Documents/config
git clone https://github.com/Chris927/dotfiles ~/Documents/config/dotfiles
git clone https://github.com/subnixr/minimal ~/Documents/config/minimal
```

Link files:

```bash
ln -s ~/Documents/config/dotfiles/dot-zshrc ~/.zshrc
ln -s ~/Documents/config/dotfiles/dot-gitignore ~/.gitignore
ln -s ~/Documents/config/dotfiles/dot-gitconfig ~/.gitconfig
ln -s ~/Documents/config/dotfiles/dot-vimrc ~/.vimrc
ln -s ~/Documents/config/dotfiles/tmux.conf ~/.tmux.conf
```


## Notes

### Docker/Compose/Machine

To get autocompletion, link the relevant scripts:

```
ln -s /Applications/Docker.app/Contents/Resources/etc/docker.zsh-completion \
     /usr/local/share/zsh/site-functions/_docker
ln -s /Applications/Docker.app/Contents/Resources/etc/docker-machine.zsh-completion \
     /usr/local/share/zsh/site-functions/_docker-machine
ln -s /Applications/Docker.app/Contents/Resources/etc/docker-compose.zsh-completion \
     /usr/local/share/zsh/site-functions/_docker-compose
```

... and reload: `exec $SHELL -l`

[credit](https://medium.com/@MicoDer/docker-zsh-autocomplete-and-denter-on-macos-easy-tutorial-630c46836652)

- 
