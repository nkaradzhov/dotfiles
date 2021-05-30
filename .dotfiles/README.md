# Start from scratch

```bash
~ git init $HOME/.cfg

 # Allows you to send git commands to the .cfg repository from any location, even outside of the repository.
 # Make sure you add it to your permanent alias location e.g. ~/.zshrc
~ alias config='/usr/bin/git --git-dir=$HOME/.cfg/.git/ --work-tree=$HOME'

 # Ignore all non-tracked files, otherwise you will see a long list of all untracked files in $HOME
~ config config --local status.showUntrackedFiles no

 # Add relevant files and push them to a newly created repo
~ config add .vimrc + config commit -m "add .vimrc" + Set up a remote repository on GitHub or your Git server of choice + config push

```

# Setup new computer

```bash
~ git clone <remote-git-repo-url> $HOME/.cfg

 # Allows you to send git commands to the .cfg repository from any location, even outside of the repository.
 # Make sure you add it to your permanent alias location e.g. ~/.zshrc 
~ alias config='/usr/bin/git --git-dir=$HOME/.cfg/.git --work-tree=$HOME'

 # Ignore all non-tracked files, otherwise you will see a long list of all untracked files in $HOME
~ config config --local status.showUntrackedFiles no

 # This might fail with a message like:
 #
 #  error: The following untracked working tree files would be overwritten by checkout:
 #  .bashrc
 #
 # Back up the files if they're useful, delete them if they aren't. 
~ config checkout
```




Credits: https://www.ackama.com/blog/posts/the-best-way-to-store-your-dotfiles-a-bare-git-repository-explained