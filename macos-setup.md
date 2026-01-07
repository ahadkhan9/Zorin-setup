# 🍎 macOS Setup Guide

Setting up your Zorin OS configs on macOS.

## Prerequisites

### Install Homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Install Oh-My-Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install CLI Tools

```bash
# Essential tools
brew install starship atuin btop eza bat ripgrep fd fzf jq tldr

# Git & GitHub CLI
brew install git gh

# Node Version Manager
brew install nvm

# Optional: lazygit, delta, procs, dust, duf, zoxide
brew install lazygit git-delta procs dust duf zoxide
```

## Install Oh-My-Zsh Plugins

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

## Copy Configurations

```bash
# Clone your backup
git clone https://github.com/AhadK0/zorin-setup.git ~/zorin-setup
cd ~/zorin-setup

# Backup existing configs
[ -f ~/.zshrc ] && mv ~/.zshrc ~/.zshrc.backup
[ -f ~/.gitconfig ] && mv ~/.gitconfig ~/.gitconfig.backup

# Copy configs
cp shell/zshrc ~/.zshrc
cp git/gitconfig ~/.gitconfig
mkdir -p ~/.config
cp prompts/starship.toml ~/.config/starship.toml
mkdir -p ~/.config/atuin
cp tools/atuin-config.toml ~/.config/atuin/config.toml
mkdir -p ~/.config/btop
cp tools/btop.conf ~/.config/btop/btop.conf
cp data/url-shortcuts.txt ~/Desktop/url-shortcuts.txt
```

## macOS-Specific Changes

Edit `~/.zshrc` and make these changes:

### Replace `xdg-open` with `open`
```bash
# Find & replace in zshrc
sed -i '' 's/xdg-open/open/g' ~/.zshrc
```

### Comment out Linux-only sections
These features use Linux-specific tools:
- **Bluetooth controls** (bt function) - uses `bluetoothctl`
- **WiFi controls** (wifi function) - uses `nmcli`

### Update PATH for Homebrew
Add to top of zshrc:
```bash
eval "$(/opt/homebrew/bin/brew shellenv)"
```

## Verify Installation

```bash
# Reload shell
source ~/.zshrc

# Test commands
starship --version
atuin --version
eza --version
```

## GitHub Copilot CLI (Optional)

```bash
gh auth login
gh extension install github/gh-copilot
```

## 🎉 Done!

Your terminal should now have all your Zorin customizations working on macOS.
