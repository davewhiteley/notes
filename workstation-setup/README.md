[Back to home](../README.md)

---

# Workstation Setup

Configuring and maintaining individual machines for software development and related tasks.

## macOS machines

### Homebrew

Website: https://brew.sh/

The Homebrew package manager can be used to programatically install applications and utilities.

#### Getting Started with Homebrew

Homebrew can be installed using the script provided on their home page.

Once installed you may want to begin using **bundles** - manifests of packages to install programatically, as opposed to piecemeal. Create a new file at `~/Brewfile` and add items as desired - see: [Brewfile](./Brewfile) for examples. Note that these are just a starting point - you will likely want to exclude some of these and add others to suit your needs.

#### Install All Packages in Your Brewfile

    cd ~
    brew bundle install
    
    # Or to use a specific file
    brew bundle --file=~/foo/Brewfile

#### Install a Single Package

    brew install foo

#### Dump the Manifest of Installed Packages

    cd ~
    brew bundle dump
    
    # Use the force flag if you don't mind overwriting the old Brewfile
    brew bundle dump --force

#### Prune Old Packages Not Present in Your Brewfile

    cd ~
    brew bundle cleanup # Use the --force flag if necessary
