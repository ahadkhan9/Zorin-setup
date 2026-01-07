# 🚀 Ahad's Zorin OS Setup

My comprehensive Zorin OS shell configuration backup for migration to macOS.

## 📦 What's Included

```
Setup/
├── shell/           # Shell configurations
│   ├── zshrc        # 2040 lines of custom zsh config
│   ├── bashrc       # Bash configuration
│   ├── profile      # Login shell config
│   ├── inputrc      # Readline settings
│   └── zshenv       # Zsh environment
├── git/
│   └── gitconfig    # Git identity & settings
├── prompts/
│   └── starship.toml # Catppuccin Mocha prompt theme
├── tools/
│   ├── atuin-config.toml # Shell history sync
│   └── btop.conf    # System monitor config
├── data/
│   ├── url-shortcuts.txt   # 50+ URL bookmarks
│   ├── apt-packages.txt    # 416 APT packages
│   ├── pip-packages.txt    # 370 Python packages
│   ├── cargo-binaries.txt  # 19 Rust CLI tools
│   ├── npm-global-packages.txt # 10 npm packages
│   └── snap-packages.txt   # 19 snap apps
├── dev-environment.md  # Full dev tools reference
└── macos-setup.md      # macOS installation guide
```

## ⚡ Key Features in zshrc

- **URL Shortcuts System** - `u leetcode`, `g rust tutorials`, `gw reddit llms`
- **LeetCode POTD** - `potd` opens daily problem
- **Project Navigation** - `proj add/list/jump` with fzf
- **Quick Notes** - `note "text"` for daily notes
- **Pomodoro Timer** - `pomo work/short/long`
- **System Dashboard** - `sysinfo`, `cpu`, `mem`, `disk`
- **Network Tools** - `myip`, `localip`, `ports`, `speedtest`
- **Bluetooth/WiFi** - `bt connect`, `wifi list` with fzf
- **AI Assistant** - `ai`, `aic`, `aix` (GitHub Copilot)
- **Modern CLI** - eza, bat, ripgrep, atuin, starship

## 🍎 macOS Setup

See [macos-setup.md](macos-setup.md) for installation instructions.

## 📝 Quick Restore (Linux)

```bash
# Clone repo
git clone https://github.com/AhadK0/zorin-setup.git ~/zorin-setup
cd ~/zorin-setup

# Symlink configs
ln -sf $(pwd)/shell/zshrc ~/.zshrc
ln -sf $(pwd)/git/gitconfig ~/.gitconfig
ln -sf $(pwd)/prompts/starship.toml ~/.config/starship.toml
```

## ⚠️ Notes

- Some Linux-specific commands (bluetoothctl, nmcli) marked with comments
- API keys should be moved to `~/.secrets` (not in repo)
