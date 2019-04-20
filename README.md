# Dotfiles Attempt

## Goals

- be minimal (and therefore fast), therefore don't use bloated plugin systems /
  frameworks (like oh-my-zsh, ...)
- understand (almost) everything

## Issues

- Currently hard coded file path linking to `subnixr/minimal`'s zshrc setup.

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
