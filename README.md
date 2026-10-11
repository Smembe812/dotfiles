# Dotfiles

My minimalist system configuration managed with GNU Stow.

## Prerequisites

Before starting, make sure [**Homebrew**](https://brew.sh) is installed (`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`).

## Installation

Run these steps from your `~/dotfiles` directory:

### 1. Install Stow
Install GNU Stow first so you can manage the rest of the repository:
```bash
brew install stow
```

### 2. Link the configurations
Symlink the Homebrew configuration (`Brewfile`) to your home directory:
```bash
stow homebrew
```

### 3. Install all dependencies
Install all remaining formulas, casks, and applications:
```bash
brew bundle --global
```

## Maintenance

### Update the Brewfile
When you install new apps or packages, update your `Brewfile` tracked in your dotfiles package:
```bash
brew bundle dump --file=~/dotfiles/homebrew/Brewfile --force
```
