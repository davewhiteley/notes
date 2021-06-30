[Back to home](../README.md)

---

# Workstation Setup

Configuring and maintaining individual machines used for software development and related tasks.

## macOS machines

### Homebrew

The Homebrew package manager can be used to programatically install applications and utilities.

Create a new file at `~/Brewfile` and add items as desired (see: [Brewfile](./Brewfile) for examples).

Install items from your Brewfile by running:

    cd ~
    brew bundle install
    
    # Or to use a specific file
    brew bundle --file=~/foo/Brewfile

If you've installed new items not yet in your Brewfile, you can write them by running:

    cd ~
    brew bundle dump
    
    # Use the force flag if you don't mind overwriting the old Brewfile
    brew bundle dump --force

If you want to prune old items not present in your Brewfile:

    brew bundle --force cleanup
