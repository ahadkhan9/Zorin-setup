# 🛠️ Development Environment Backup

Complete list of installed developer tools and packages on Zorin OS.

## 📌 Runtime Versions

| Tool | Version |
|------|---------|
| Node.js | v20.5.0 |
| npm | 10.8.3 |
| Python | 3.10.12 |
| Java | OpenJDK 21.0.9 |
| Rust | (via rustup) |

---

## 🔧 PATH Configuration

```bash
# User binaries
~/bin
~/.local/bin
~/.cargo/bin

# NVM Node
~/.nvm/versions/node/v20.5.0/bin

# JetBrains
~/.local/share/JetBrains/Toolbox/scripts
/opt/JetBrains Rider-2024.3.3/bin

# .NET & SQL
~/.dotnet/tools
/opt/mssql-tools18/bin

# System
/usr/local/bin
/usr/bin
/snap/bin
```

---

## 📦 Global NPM Packages

```bash
npm install -g @anthropic-ai/claude-code
npm install -g @google/gemini-cli
npm install -g @mermaid-js/mermaid-cli
npm install -g http-server
npm install -g md-to-pdf
npm install -g tldr
npm install -g vercel
```

---

## 🦀 Cargo (Rust) Binaries

```bash
cargo install atuin     # Shell history
cargo install bat       # Better cat
cargo install broot     # File explorer
cargo install delta     # Git diff viewer
cargo install dust      # Disk usage
cargo install duf       # Disk free
cargo install eza       # Better ls
cargo install fd-find   # Better find
cargo install just      # Task runner
cargo install mcfly     # History search
cargo install procs     # Better ps
cargo install ripgrep   # Better grep
cargo install sd        # Better sed
cargo install starship  # Shell prompt
cargo install tokei     # Code stats
```

---

## 🐍 Python Packages (Key)

```bash
pip3 install autogen-agentchat autogen-core  # AI Agents
pip3 install awscli boto3                    # AWS
pip3 install beautifulsoup4 requests         # Web scraping
pip3 install docker                          # Docker SDK
pip3 install fastapi flask                   # Web frameworks
pip3 install google-generativeai             # Gemini API
pip3 install httpie httpx                    # HTTP clients
pip3 install huggingface-hub                 # ML models
pip3 install jupyter ipython                 # Interactive Python
pip3 install localstack                      # AWS local dev
pip3 install numpy pandas                    # Data science
pip3 install openai                          # OpenAI API
pip3 install opencv-python                   # Computer vision
pip3 install torch                           # PyTorch (CUDA)
```

Full list: 370+ packages

---

## 📱 Snap Packages

```bash
# IDEs
snap install android-studio --classic
snap install dbeaver-ce
snap install mysql-workbench-community

# Apps
snap install slack
snap install postman
snap install lazygit
```

---

## 📋 APT Packages (Developer)

```bash
# Build tools
sudo apt install build-essential cmake gcc-12-base

# Docker
sudo apt install docker.io

# Editors
sudo apt install code code-insiders cursor

# CLI Tools
sudo apt install btop htop fzf gh git httpie
sudo apt install cloudflare-warp cloudflared

# Languages
# (Node via NVM, Python via apt, Java via SDKMAN)
```

---

## 🔑 Environment Variables

```bash
# NVM
export NVM_DIR="$HOME/.nvm"

# SDKMAN
export SDKMAN_DIR="$HOME/.sdkman"

# Gemini API
export gemini_flash_api='YOUR_API_KEY'  # Move to ~/.secrets
```

---

## 💡 macOS Equivalents

| Linux Tool | macOS Install |
|------------|---------------|
| apt | `brew` |
| snap | `brew install --cask` |
| xdg-open | `open` |
| dolphin | `open .` (Finder) |
| bluetoothctl | System Preferences |
| nmcli | `networksetup` |

Most cargo/npm packages work identically on macOS!
