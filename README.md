Following this guide:

https://www.atlassian.com/git/tutorials/dotfiles

Using `dotfiles` as my command.

## To install

Add this to .zshrc/.bashrc etc:
```
alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
```

Clone the repo:
```
git clone --bare https://github.com/jonas-scholz123/dotfiles.git $HOME/.dotfiles
```

Check out the actual repo content:
```
dotfiles checkout
```
(If you have problems, remove existing config files first.)


Finally, make sure no untracked files are shown/added to commits.
```
dotfiles config --local status.showUntrackedFiles no
```


## To use
Just use git commands but using the `dotfiles` alias, e.g.
```
dotfiles add .zed/settings.json
dotfiles commit -m "Add zed settings"
dotfiles push
```
