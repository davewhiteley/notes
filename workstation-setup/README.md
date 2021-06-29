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
    brew bundle
